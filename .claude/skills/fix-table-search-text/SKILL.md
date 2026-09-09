---
name: fix-table-search-text
description: >
  Verify (and, if needed, regenerate) the patch-package fix for a bug in
  @quartz-community/description that fuses adjacent table-cell text with
  no separator when building the search/description plain-text index —
  e.g. a card name like "Rengar" in a table row becomes glued to the
  previous cell as "219Rengar", making it unsearchable. Use when asked to
  check the search-index table fix, after upgrading
  @quartz-community/description, if `npm ci`/`npm install` prints a
  patch-package warning, or if sitewide search stops finding card names
  that only appear inside a Cards/*.md table. Triggers: search doesn't
  find cards, table text fused, patch-package failed, description plugin
  upgrade, Rengar search bug, contentIndex text concatenated.
---

# Fix: table cell text fused in search index

## The bug

`@quartz-community/description`'s `htmlPlugins` transform builds the plain
text used for both the meta description AND the sitewide search index
(`file.data.text`) by flattening the page's HTML tree with a vendored copy
of `hast-util-to-string`. That library's `all()` function joins sibling
nodes with `result.join("")` — an empty string. That's fine for normal
prose (the spaces between words already exist as literal text), but a
markdown table's `<td>` cells have **no whitespace between them** in the
underlying HTML — the visual gap is CSS padding, not a text node. So
`OGN.md`/`UNL.md`/`VEN.md`/`SFD.md` (each one big table) get their cell
values concatenated with zero separator: `...UNL-024/219Rengar - Unseen...`
— "Rengar" is stuck to "219" as one token, so searching the literal card
name never matches. Confirmed by inspecting `public/static/contentIndex.json`
after a build; not a config or content mistake.

Traced to: `node_modules/@quartz-community/description/dist/index.js`,
the `all(node)` function (originally lines ~14-21).

## The fix

Patched via **patch-package**, not a hand-edit to `node_modules` (which
`npm ci` would wipe). The patch lives at
`patches/@quartz-community+description+<version>.patch` and reapplies
automatically via the root `package.json`'s `"postinstall": "patch-package"`
script — **normally nothing needs to be done manually**, this skill exists
for when that automatic path breaks.

The fix changes `all()`'s `return result.join("")` to a smarter join that
only inserts a space between two adjacent flattened chunks when *neither*
side already ends/starts with whitespace — this separates fused table
cells without adding extra spaces to normal prose (where the boundary
whitespace already exists in the source text nodes):

```js
function all(node) {
  let index = -1;
  const result = [];
  while (++index < node.children.length) {
    result[index] = one(node.children[index]);
  }
  return result.reduce((acc, cur) => {
    if (!acc) return cur;
    if (!cur) return acc;
    const needsSpace = !/\s$/.test(acc) && !/^\s/.test(cur);
    return acc + (needsSpace ? " " : "") + cur;
  }, "");
}
```

## Step 1 — Check if it's already applied and working

```bash
grep -n "needsSpace" node_modules/@quartz-community/description/dist/index.js
```

A hit means the patch is live. If `npm ci`/`npm install` ran cleanly with
no `patch-package` error in its output, this will always be true — the
postinstall hook already handled it. Nothing more to do.

## Step 2 — Only if the patch failed to apply

This happens if `@quartz-community/description` gets upgraded to a new
version whose `dist/index.js` no longer matches the patch's expected
context (patch-package will print `Failed to apply patch` during install,
not fail silently). To regenerate:

1. Re-apply the fix by hand: open
   `node_modules/@quartz-community/description/dist/index.js`, find the
   `function all(node) { ... }` block (it may have shifted lines or the
   surrounding bundle output changed slightly), and replace its
   `return result.join("");` with the `reduce`-based version above.
2. Delete the stale patch file (its filename embeds the old version):
   ```bash
   rm patches/@quartz-community+description+*.patch
   ```
3. Regenerate it against the new version:
   ```bash
   npx patch-package @quartz-community/description
   ```
4. Verify end to end:
   ```bash
   rm -rf node_modules && npm ci   # confirms the new patch auto-applies
   npx quartz build
   python3 -c "
   import json
   d = json.load(open('public/static/contentIndex.json'))
   c = d['cards/unl']['content']
   i = c.find('Rengar')
   print(repr(c[max(0,i-40):i+40]))
   "
   ```
   Expect to see `Rengar` surrounded by spaces (e.g.
   `UNL-024/219 Rengar - Unseen Rare Unit`), not glued to the preceding
   number (`219Rengar`).

## If patch-package itself is what's missing

`patch-package` is a `devDependency` and the `postinstall` script is what
wires it in. If either got removed:

```bash
npm install --save-dev patch-package
```
and confirm `package.json`'s `scripts` has `"postinstall": "patch-package"`
alongside the existing `"prebuild": "npm run install-plugins"` entry.
