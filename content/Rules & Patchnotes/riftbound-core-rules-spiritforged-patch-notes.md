# Riftbound Core Rules: Spiritforged Patch Notes

> **Published:** 2025-12-05  
> **Source:** https://playriftbound.com/en-us/news/rules-and-releases/riftbound-core-rules-spiritforged-patch-notes/  
> **Effective Date:** December 12, 2025

---

Welcome to the Patch Notes for *Riftbound*, *Spiritforged* edition. This update to the Core Rules supports the *Spiritforged* expansion. Included are system clarifications, fixes to a few logical errors, and the new rules required to play with the mechanics in *Spiritforged*.

### What This Is

The primary purpose of this rules update is to ensure all new cards in *Spiritforged* work when released in China on December 12. Some clarifications or housekeeping tasks were left undone to meet that goal. This is what patch notes will typically look like: system updates, clarity, and new rules focused primarily on new cards and mechanics, and secondarily on fixing known issues.

**Important distinction:** These updates serve only some of the purposes of typical patch notes. We change rules to make new cards work and to work toward systemic stability — not to balance card power. Any errata issued is for clarity and error correction, not power adjustment.

Rather than taking effect immediately, these rules have an **effective date of December 12, 2025** to ensure the Chinese *Spiritforged* release is fully supported, while other regions have time to absorb changes without impacting major tournaments.

---

## Patch Notes

### Spiritforged Addition: Attachment, Attached, and Detached

Cards can now *attach* to other cards.

- **Attach** is a verb — the act of one card being linked to another.
- **Attached** is the state of being linked.
- **Detach** is the opposite verb; there is no opposite "detached" state (everything isn't constantly "detached," it's just *not attached*).

Cards that attach have a unique new frame. Players are encouraged to overlay the card to represent how attached cards append their abilities to the card on top.

The special attachment frame includes a **Might Bonus** — a number that modulates the Might of the card on top.

While a card is *attached*, its rules text becomes *inactive* (defined below).

- **NEW SYSTEM:** Attachment, Attached, and Top-Most Card State added
- **NEW SYSTEM:** Effect Text added to Parts of a Card
- **NEW SYSTEM:** Might Bonus added to Parts of a Card
- **NEW RULE:** New rules added to layers to account for attachments and might bonuses
- **NEW RULE:** Attach action added
- **NEW RULE:** Detach action added

---

### Spiritforged Addition: Inactive Text

To support the *attached* state, the concept of text being *inactive* has been defined.

- *Inactive* text is text that is **ignored**.
- By default, certain sections of the new attachment frame — the *effect text* and *might bonus* — are *inactive* while the card is **not** attached.
- When a card with these sections becomes *attached*, that section stops being *inactive*, and its *rules text* becomes *inactive* instead.

While *inactive* text has no effect on the game, it **does still exist**. Other effects can still check on it. Example: a card with *Temporary* still **has** *Temporary* even if it is *inactive* and won't trigger. A hypothetical effect that says "Destroy a card with *Temporary*" could still choose something with an *inactive Temporary* keyword.

- **NEW SYSTEM:** Inactive Rules System Added *(Inactive but not forgotten)*
- **NEW RULE:** Exceptions to *Inactive* rules added

---

### Spiritforged Addition: Equip

*Equip* is the keyword for the new *Equipment* card type.

- Pay the *Equip* cost, choose a unit you control, and *attach* the *Equipment* to that unit.
- You cannot use an *Equip* ability if the card is already *attached* to something (because its rules text becomes *inactive* when attached).
- If the unit carrying the equipment is killed or otherwise leaves the board, you keep the gear — *Equip* it to the next contender.

- **NEW RULE:** Equip keyword added *(Get suited up)*
- **NEW RULE:** Equipment tag referenced in various rules

---

### Spiritforged Addition: Quick-Draw

Some *Equipment* have the *Quick-Draw* keyword in addition to *Equip*.

- *Quick-Draw* lets you play (and consequently attach) *Equipment* straight from your hand at **Reaction** speed.
- *Quick-Draw* inherently contains *Reaction* as a nested part of it.
- *Quick-Draw* is also a **Play Effect** that attaches the played *Equipment* directly to a unit you control — no need to pay the *Equip* cost.
- *Quick-Draw* does **not** change when you can use an *Equipment's Equip* ability, only when you can play it from your hand.

- **NEW RULE:** Quick-Draw keyword added
- **NEW RULE:** Quick-Draw contains Reaction *(Lickity-split)*

---

### Spiritforged Addition: Weaponmaster

Some units have the *Weaponmaster* keyword.

- This is a **Play Effect** that chooses an *Equipment* you control, then lets you pay that *Equipment's Equip* cost, reduced by `[A]`, to attach it to the unit with *Weaponmaster*.
- It can even choose *Equipment* that's already *attached* to a **different unit**. Since *inactive* text like *Equip* costs can still be referenced by other effects, *Weaponmaster* can check on that cost and reference it to determine the cost you need to pay.

- **NEW RULE:** Weaponmaster keyword added
- **NEW RULE:** Exceptions and clarifications added to *Inactive* *(check the Inactive section)*

---

### Spiritforged Addition: Repeat

A spell mechanic that lets you get the effect of your spell a second time.

- *Repeat* is an optional **additional cost**.
- When paid, lets you execute the effect of the spell one additional time.
- You can only pay this cost **once**.
- This still only counts as playing the spell once *(sorry, Ravenbloom Student)*.

- **NEW RULE:** Repeat as a keyword added *(It bears Repeating)*

---

### Control of Abilities

Added a rule to clarify the unlikely situation where control of an object changes while an ability originating from that object is on the chain. **Control of the ability will not change along with its originating object.**

- **NEW RULE:** Control of abilities on the chain is independent of the objects from which they originate

---

### Priority and Focus

Clarified the language around priority and focus:

- **Priority** is the singular and exclusive right to take discretionary actions. Only the player with priority may act.
- **Focus** is like a "home base." It is an additional permission and a tracking tool. Focus passes around to make sure everyone gets a turn to play *Actions* in showdowns, even as priority bounces around.
- There is no situation where more than one player can contest having authority to do something at the same time.

- **CLARIFIED:** Priority is the singular exclusive right to take discretionary actions during a closed state
- **NEW RULE:** Granting priority to a player either creates priority or removes it from a player that has it *(No sharing. Even if you hold hands.)*
- **NEW RULE:** Having focus without priority does not grant the right to take discretionary actions

---

### Deathknell

*Deathknell* worked before but was fuzzy and not logically consistent for many players. New steps have been added in Cleanups, Kill Instructions, and in the *Deathknell* keyword itself to capture intent. This was prompted by Svellsongur existing and requiring reliable *Deathknell* support.

> *Note: This is somehow a Kog'maw buff despite Deathknell being clarified.*

- **CLARIFIED:** Deathknell now works
- **NEW RULE:** New rules added to Cleanups to support Deathknell
- **NEW RULE:** New rules added to Kill action to support Deathknell
- **NEW RULE:** New rules added to Deathknell to support remembering state and information about the game object with Deathknell after it dies

---

### Cleanups

- **CLARIFIED:** Removal of *Contested* status is **not** a part of the Special Cleanup at the end of combat *(a previous formatting/numbering error made this unclear)*
- **NEW RULE:** Added rule for ceasing showdowns being staged
- **NEW RULE:** Added rule for ceasing combat being staged
- **CLARIFIED:** Various improvements and adjustments across cleanups and special cleanups

---

### Playing Units to Valid Locations

The rules previously specified that units could be played to any "valid location" but neglected to spell out which locations are valid.

- **NEW RULE:** By default, a player can play a unit to their **base** or to a **battlefield they control**
- **NEW RULE:** Specific cards may restrict or expand the list of valid locations *(Validating)*

---

### Double and Swap

Added both *double* and *swap* to the list of game actions. Simple English meaning isn't sufficient when these verbs are applied to numerical values for a limited duration.

> Note: Gearhead gets away with using the simple English meaning of double because it's not being used as a verb and doesn't have a duration — "gives double its Might bonus" = "gives twice its Might bonus."

- **NEW RULE:** Double added to the list of game actions
- **NEW RULE:** Swap added to the list of game actions

---

### General

- **CLARIFIED:** Various housekeeping and updates to language across the document, including adjusting or removing examples that are no longer accurate

---

## Related Articles

1. [Vendetta Rules FAQ and Clarifications](https://playriftbound.com/en-us/news/rules-and-releases/vendetta-rules-faq-and-clarifications) — 2026-08-14
2. [Unleashed Rules FAQ and Clarifications](https://playriftbound.com/en-us/news/rules-and-releases/unleashed-rules-faq-and-clarifications) — 2026-04-29
3. [Unleashed Errata Updates](https://playriftbound.com/en-us/news/rules-and-releases/unleashed-errata-updates) — 2026-04-03
4. [Riftbound Core Rules: Unleashed Patch Notes](https://playriftbound.com/en-us/news/rules-and-releases/riftbound-core-rules-unleashed-patch-notes) — 2026-03-30
5. [Tournament Rules, January Update](https://playriftbound.com/en-us/news/announcements/tournament-rules-january-update) — 2026-01-30
6. [Riftbound Spiritforged FAQ](https://playriftbound.com/en-us/news/rules-and-releases/riftbound-spiritforged-faq) — 2026-01-14
7. [Riftbound Spiritforged Errata](https://playriftbound.com/en-us/news/rules-and-releases/riftbound-spiritforged-errata) — 2026-01-14
8. [Riftbound: Origins Card Errata](https://playriftbound.com/en-us/news/rules-and-releases/riftbound-origins-card-errata) — 2025-10-28
9. [Riftbound Core Rules: Patch Notes (Origins)](https://playriftbound.com/en-us/news/rules-and-releases/riftbound-core-rules-patch-notes) — 2025-10-24
