# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repo is

This is a fork of [Quartz v5](https://quartz.jzhao.xyz/) (`@jackyzha0/quartz`, a static site generator for Obsidian vaults) used to publish an Obsidian vault of **Riftbound TCG** card-collection data — a binder inventory, a missing-cards/wishlist list, and rules/patch-note references — as a browsable site on GitHub Pages (`riftbound.lyso.dev`).

**`content/` is the actual Obsidian vault root** (its `.obsidian/` config folder lives there), and also Quartz's content dir — the two are the same directory by design. Direct edits to files under `content/` are expected and fine: Claude is authorized to edit vault content there and publish it (`npx quartz sync` — see the `riftbound-publish` Claude Code skill) without asking each time, mirroring what the Obsidian sync plugin itself does (commits titled `Quartz sync: <date>` in the git log are it, or a prior Claude run). When asked to update binder/wishlist contents specifically, prefer the repo-independent `riftbound-card-list` and `riftbound-price-check` Claude Code skills (they know the checklist format and TCGplayer-lookup conventions used in `content/Cards/*.md` and `content/Missing Cards.md`) over freehand edits — read an existing entry there first to match the format.

Everything under `quartz/`, `docs/`, and the root config files is the Quartz engine/template itself, largely unmodified from upstream aside from `quartz.config.yaml` (site config + enabled plugin list) and the GitHub Pages deploy workflow.

## Commands

```bash
npm ci                          # install deps (see Known gotchas below)
npm run check                   # tsc --noEmit + prettier --check — run before considering a change done
npm run format                  # prettier --write
npm test                        # tsx --test — runs all *.test.ts/*.test.js via node's test runner
npx tsx --test path/to/x.test.ts  # run a single test file
npm run install-plugins         # (also runs automatically as a `prebuild` hook) resolves the
                                 # `plugins:` list in quartz.config.yaml — currently all entries are
                                 # ordinary npm packages already in package.json, so this is mostly a
                                 # no-op unless quartz.config.yaml gains a git-sourced plugin
npx quartz build                # production build to public/
npx quartz build --serve -d docs  # local dev server (also `npm run docs`)
npx quartz build --bundleInfo -d docs  # what CI runs to sanity-check the build + bundle size
```

## Architecture

**Plugin marketplace, not hardcoded plugin arrays.** Unlike classic Quartz (plugins listed as TS imports in `quartz.config.ts`), this fork resolves plugins declaratively: `quartz.config.yaml`'s `plugins:` array lists each plugin by `source:` (an npm package name, e.g. `@quartz-community/favicon`, or a git repo spec), `enabled:`, `options:`, and — for UI components — a `layout:` block (`position`, `priority`, `group`, `condition`). `quartz.ts` calls `loadQuartzConfig()` / `loadQuartzLayout()` (`quartz/plugins/loader/config-loader.ts`), which reads that YAML and assembles the actual plugin/layout objects at build time. `quartz/plugins/loader/gitLoader.ts` + `install-plugins.ts` handle fetching any non-npm (git-sourced) plugins into `.quartz/plugins` (gitignored) — not needed today since every configured plugin here resolves to a real npm package already pinned in `package.json`.

To enable/disable a feature or reorder page layout, edit `quartz.config.yaml` — don't hand-edit generated layout wiring.

**Deploy.** `.github/workflows/deploy.yml` builds on push to `v5` and publishes `public/` to GitHub Pages via the standard Pages artifact/deploy actions — this is the workflow that actually matters for this fork. `.github/workflows/ci.yaml` and `deploy-v5.yaml` are upstream Quartz's own CI/Cloudflare-preview workflows and are gated on `github.repository == 'jackyzha0/quartz'`, so they no-op on this fork; don't rely on them for anything.

**Content root** is `content/` (Quartz's default vault dir, unset elsewhere — see `ignorePatterns` in `quartz.config.yaml` for what's excluded from the build within it, e.g. `.obsidian`, `private`, `templates`, `Unprocessed`).

## Inventory workflow

Each set has a full bulk-inventory checklist (`content/Cards/OGN.md`, `UNL.md`, `VEN.md`, `SFD.md`) — one row per card, a blank/user-filled **Qty** column, no pricing. `content/Unprocessed/` is a staging area so the user doesn't have to hand-edit those tables every time something happens to their collection:

- `content/Unprocessed/Traded.md` and `Pulled.md` — normal synced tables the user fills in as trades/pack-openings happen.
- `content/Unprocessed/Sold.md` is a stub — the real cash-sale table is `content/private/Sold.md`, which is **gitignored and never synced** (financial data, kept local-only since the GitHub repo is public). Never move sale data into a synced file.

When the user asks to **"process the Unprocessed folder"** (or similar — "process the trades", "process what I pulled"):
1. For each filled-in row in `Traded.md`: decrement the given card's Qty (and increment the received card's Qty) in the relevant `content/Cards/<SET>.md` table — match by the `SET-NUM/total` code, not just name (cards can repeat across printings).
2. For each filled-in row in `Pulled.md`: increment the pulled card's Qty in its set file, and append a line to `content/Acquisition Log.md`.
3. For each filled-in row in `content/private/Sold.md`: decrement the sold card's Qty in its set file (and in `Binder.md` if it was tracked there as an owned single).
4. After applying, clear the processed table back to just its header row (don't leave stale processed rows sitting around) — this applies to `content/private/Sold.md` too, even though it's never synced.
5. Sync only the normal content (`npx quartz sync` already won't touch `private/` since it's gitignored — no special handling needed there beyond making sure edits actually landed in the file).

## Known gotchas

- **`sharp` install fails with a `node-gyp` error** on machines with a system-level `libvips` (e.g. Arch/pacman installs it as a dependency of other apps). `sharp`'s installer detects the global libvips via `pkg-config` and deliberately tries to build from source against it instead of using its bundled prebuilt binary — which then fails since `sharp` doesn't ship `node-gyp` as a real dependency. Fix: `SHARP_IGNORE_GLOBAL_LIBVIPS=1` in the environment before `npm ci`/`npm install`.
- **npm's install-scripts allowlist**: this repo's `package.json` has an `allowScripts` block (npm 11+ feature) explicitly allowlisting the packages that need to run install/postinstall scripts (`sharp`, `esbuild`, `@parcel/watcher`). Adding a new dependency with a native/install script will make `npm ci` warn and skip that script until you run `npm install-scripts approve <pkg>`.
- **Sitewide search can't find text inside `Cards/*.md` tables** — `@quartz-community/description` flattens page HTML for the search index with zero separator between elements, so adjacent `<td>` cells fuse into one token (e.g. a card name glues to the previous cell's number: `219Rengar`). Patched via `patch-package` (`patches/@quartz-community+description+*.patch`, auto-applied by the `postinstall` script) — see the `fix-table-search-text` skill (`.claude/skills/fix-table-search-text/`) if the patch ever fails to apply after a dependency upgrade.
