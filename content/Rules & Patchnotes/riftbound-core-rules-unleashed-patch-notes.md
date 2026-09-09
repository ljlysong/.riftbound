# Riftbound Core Rules: Unleashed Patch Notes

> **Published:** 2026-03-30  
> **Source:** https://playriftbound.com/en-us/news/rules-and-releases/riftbound-core-rules-unleashed-patch-notes/  
> **China Effective Date:** April 8, 2026

---

Welcome to the Patch Notes for Riftbound, *Unleashed* edition. Included are system clarifications and expansions, fixes to many logical or procedural errors, and the new rules required to play with the mechanics in *Unleashed*.

### Three Key Goals

1. Support the new expansion's cards and mechanics with rules that explain how they function.
2. Provide clarity on rules changes and why we make them.
3. Shore up rules foundations that were unclear or in need of updating.

### Context for This Update

The *Spiritforged* rules update allowed some streamlining via reusing previously introduced systems. Some changes in this update address interactions introduced by *Spiritforged* cards that the rules were not equipped to handle. Many changes clarify how those interactions function and preemptively clarify interactions with *Unleashed* cards.

> **On balance:** Goals when changing rules are to make rules more intuitive for players and to set up future improvements. There are no plans to change rules to manage card power level. Some cards will receive functional changes, but that is not the goal. With each update, the hope is that fewer systems will be updated or changed in a functional way.

---

## Patch Notes

### Unleashed Addition: XP, Hunt, Level

*XP* is the marquee mechanic for *Unleashed*.

- **XP** is a resource that spells and abilities will add and spend (similar to energy, power, or buffs).
- **Hunt** is an ability that gives its controller 1 XP when a unit with Hunt conquers or holds. Higher Hunt Value = more XP gained.
- **Level** is a *dependent keyword* (see below) that becomes *active* when its controller has a certain amount of XP. `[Level 6]` means the dependent ability will be active when its controller has 6 XP.
- Some *Unleashed* booster packs include a token card in the token slot to help players track their XP.

- **NEW SYSTEM:** XP
- **NEW RULE:** Hunt as a keyword was added
- **NEW RULE:** Level as a keyword was added

---

### Unleashed Addition: [>] Symbols

To clarify how dependent and permissive keywords work, a new templating element is being introduced: **a small arrow (`[>]`)** pointing from the word backer of *dependent* and *permissive keywords*.

Keywords affected: *Reaction, Action, Deathknell, Level,* and *Legion* — these now come **before** the ability at the very start of the line. The arrowed backer indicates the ability that these keywords are associated with.

This solves longstanding *Legion* confusion: Does the *Legion* text only include the parts after the keyword? Can you activate the ability if you haven't played a card this turn?

Outside of card text, this symbol will be expressed as `[>]`.

- **NEW SYSTEM:** [>] Symbol added

---

### Unleashed Addition: Dependent Keywords, Updated Legion

A *dependent keyword* is made up of two parts:
1. The keyword itself (short for a condition)
2. The *dependent ability* that is *active* while the condition is fulfilled

So long as the condition is not fulfilled, the ability is *inactive* — the effect won't apply and can't be triggered or activated.

*Legion* already worked this way. *Legion* is being updated using the new dependent keyword rules.

- **NEW SYSTEM:** Dependent Keywords
- **CLARIFIED:** Legion is a dependent keyword

---

### Unleashed Addition: Ambush, Conditional Action and Reaction

The bot gank lives on. Units with *Ambush* have two passive abilities:
1. "I may be played to a battlefield where you control Units"
2. "I have [Reaction] as long as I'm being played to a battlefield where you control Units"

To support conditional *Reaction*, new rules clarify how and when cards with conditional permissive abilities can be played to the chain, and what happens if they lose those abilities while on the chain.

- **NEW RULE:** Ambush as a keyword was added
- **NEW RULE:** Conditional permissive abilities may only be fulfilled while the card or ability is on the chain. It can still be played or activated at the appropriate timing as long as doing so *could* fulfill the conditions.
- **NEW RULE:** If the chain item does not fulfill the conditions by "step 5: check legality," the actions taken while playing or activating the chain item are undone and it is returned to the zone it was played from.

---

### Rules Update: Winning the Game

Previously there were two conflicting rules for winning:
- Win if points equal the *Victory Score* during a cleanup
- Win immediately if points equal the *Victory Score* (without waiting for cleanup)

Resolution:

- **CLARIFIED:** A player wins if, during a cleanup, they have accrued points **≥ Victory Score** AND **greater than any opponent**. Both must be true.
- **NEW RULE:** If a player gains two or more points as a result of burn outs processed in sequence and fulfills the above conditions, they win **immediately** without waiting for a cleanup.

---

### Rules Update: Combats and Showdowns

The vast majority of players intuit that a showdown should be able to transition to a combat when units controlled by different players are present. Previously, the rules procedurally required the current showdown to end before a combat could begin.

New rules:

- A showdown opens as long as the battlefield is *contested* and there is a unit there whose controller doesn't control the battlefield.
- If units controlled by different players are at the battlefield → combat showdown.
- Otherwise → non-combat showdown.
- If a non-combat showdown is ongoing and a combat becomes staged at the same battlefield → the non-combat showdown becomes a combat showdown in the next cleanup.

- **NEW RULE:** Showdowns are staged at battlefields that are contested
- **NEW RULE:** Combats are staged at battlefields that are contested and have units controlled by different players
- **NEW RULE:** If the turn player would initiate a showdown at a battlefield where a combat is staged, it opens as a combat showdown
- **NEW RULE:** If the turn is in a showdown open state and combat is staged at a battlefield with an ongoing showdown, a cleanup will cause the showdown to become a combat showdown

---

### Rules Update: The Resolution Step of Combat

Updated the *Resolution Step* procedures using the new *HOT FEPR* system.

Revised sequence after combat:
1. **Combat Cleanup:** Units are healed; attacking units are recalled
2. **Determine winner/loser:** Player with remaining units wins; if units from both sides remain or no units at all → "no result"
3. **Conquest** (if applicable)
4. **Designations and expirations:** Players and units lose attacker/defender designation; "this combat" effects expire

- **CLARIFIED:** The Resolution Step has been reorganized

---

### Rules Update: "May" Triggered Abilities and Extra Conditions

**This is a significant change** — part of a larger upcoming development to templating and card layout.

- **Triggered abilities that say "may"** are now **optional to place on the chain**. The controller chooses whether to place the triggered ability on the chain when its trigger condition is fulfilled.
- **Triggered abilities with `[do X] to [do Y]`** (*costs within instructions*): the cost ("[do X]") is incurred when placing the triggered ability on the chain.

- **CLARIFIED:** If a triggered ability says "you may" as the first part of its effect, the controller chooses whether or not to place it on the chain when triggered
- **CLARIFIED:** If a triggered ability contains a cost within instructions, that cost is treated as the base cost of the triggered ability and must be paid to finalize the ability to the chain

---

### Replace

*Replace* is a game action. Cards in *Unleashed* prompted full rules for how objects are *replaced* and where the replaced objects go.

- Replaced objects go to the same zone that banished cards go.
- Whatever token replaces the object will **inherit all effects and statuses** that object had.
- Some effects may allow the replaced object to be *swapped back*.

- **NEW RULE:** Replace action added
- **NEW RULE:** Swapping back defined

---

### Create

When a token is *created*, it is immediately generated in the appropriate zone **without using the chain**. Added primarily to support the *replace* action (tokens have to come from somewhere).

- **NEW RULE:** Create action added

---

### Predict and Word Backers

Codifying the instruction "look at the top card of your main deck. You may recycle it" into the game action *Predict*.

**Predict:** Look at some number of cards from the top of your main deck, choose to *recycle* any number of them, and place the remaining ones back in any order of the predicting player's choosing.

As part of codification, word backers have been added to several game actions that frequently appear in card text (similar to keyword backers). Starting with *Unleashed* cards: backers for *Stun* and *Buff* join *Predict*.

- **NEW RULE:** Predict action added
- **NEW SYSTEM:** Action Word Backers added

---

### Copy Effects

First true *copy effect* appears in *Unleashed* (Svellsongur in *Spiritforged* was the precursor).

- **CLARIFIED:** Copy effects will copy the "copyable traits" of a game object — all printed or copied traits including Rules Text. Nothing appended or granted will be copied.
- **CLARIFIED:** Copy effects that copy only a specific set of traits will specify those traits.
- **NEW RULE:** When a game object or some of its traits become a copy of another, all copied traits become the game object's new copyable traits.
  - *If you copy a copy, the new copy becomes a copy of the originally copied object. Copy copy copy.*

---

### Spicy HOT FEPR

**HOT FEPR** = **H**andle **O**utstanding **T**asks; **F**inalize **E**xecute **P**ass **R**esolve

*Tasks* are the various procedures the game requires players to perform during their turn: cleanups, start of turn procedures, procedures of combat, end of turn procedures.

When tasks are *outstanding*, pause the *FEPR* process until those outstanding tasks have been handled, then perform the *FEPR* process on any pending chain items.

Note: Pending items on the chain are **no longer finalized during cleanups** (see Cleaned Up Cleanups below).

- **NEW SYSTEM:** HOT FEPR

---

### Cleaned Up Cleanups

Finalization was removed from the cleanup and made part of the HOT FEPR process (its presence in cleanup was a vestigial rule from before FEPR was introduced).

- **CLARIFIED:** Combat designations are removed or added **before** units die to marked damage in a normal cleanup
- **CLARIFIED:** A unit is "in combat" if it occupies a battlefield where combat is ongoing AND has an appropriate combat designation
- **CLARIFIED:** Finalization is no longer managed by the cleanup — happens after any outstanding tasks occur if there are pending items on the chain

---

### Loopy Expiration Step

Two changes:
1. The **End of Turn Phase** is renamed the **Ending Phase**.
2. The expiration step now properly loops.

Context: In *Spiritforged*, the first instance of a triggered ability triggering in the expiration step produced unintuitive results (e.g., "this turn" effects applied in reaction lasting until the next turn; damage applied in the expiration step carrying over).

Fix: If any items underwent the FEPR process during the Expiration Step, return to the start of the Expiration Step.

- **CLARIFIED:** The End of Turn Phase is now the **Ending Phase**
- **CLARIFIED:** The End of Turn Cleanup has been folded into the Expiration Step
- **NEW RULE:** If any items underwent the FEPR process during the Expiration Step, return to the start of the Expiration Step

---

### Replacement Effects

Several updates to resolve points of confusion (multiple simultaneous events, modified events, who controls a replacement effect, Soraka + equipped Guardian Angel):

- **CLARIFIED:** If multiple simultaneous events are able to be replaced by a replacement effect, the controller of the replacement effect decides the order in which it is applied
- **CLARIFIED:** Each replacement effect can only be applied in one sequence — one uninterrupted series of applications — when applied to simultaneous events
- **NEW RULE:** The controller of a replacement effect is the player who controls the **source** of the replacement effect
- **NEW RULE:** If an event replaced by a replacement effect would be modified by a game effect or game action, the replacement effect **inherits those modifications**

---

### Control of Battlefields

Fixed issues with battlefield control handling in cleanup (specifically bugs with Hostile Takeover and Stormbringer causing ambiguous states). Control is now locked by the presence of a **combat or showdown** at the battlefield instead of contested status.

Additionally: Control of a battlefield cannot be lost while there is an **item on the chain** (supports *Unleashed* cards).

- **CLARIFIED:** If a player has no units at a battlefield and the turn is in an open state, they lose control in the following cleanup, **unless there is a combat or showdown ongoing there**

---

### Responsibility for Game Actions

A player is *responsible* for a game action if they:
- Performed the game action, OR
- Were assigned responsibility (usually if responsible for a deal action attributed a kill action)

Responsibility is maintained even if they did not control the effect that instructed them to perform the action.

For a condition like "when you kill a unit with a spell," a player must be responsible for the kill action, control the spell that instructed it, and the spell itself must have attribution for the kill action.

- **NEW RULE:** Responsibility

---

### Linking

*Linked instructions* and *linked abilities* are instructions or abilities that reference or are referenced by another instruction or ability.

Important for spells granted the *repeat* keyword (e.g., repeated Hidden Blade) and abilities that reference other abilities.

- **NEW RULE:** Instructions that reference Game Objects affected by, or Game Actions performed in, other instructions are "linked instructions"
- **NEW RULE:** For a later linked instruction to execute, its earlier linked instruction must have executed. If the earlier was ignored, the later is also ignored.
- **NEW RULE:** If a game action in an earlier linked instruction was replaced, this will not affect the later linked instruction
- **NEW RULE:** Linked Abilities added

---

### Referents

Codifying a concept players already know: if a spell, triggered ability, or activated ability says "here," "my," "its," or similar referential word, that information is checked **when the spell or ability resolves**.

Exception: Some abilities reference the trigger condition in their text — those abilities check that information **when they trigger and are placed on the chain**, not on resolution.

- **NEW RULE:** Referents

---

### Additional Turn Effects

Settling the Time Warp debate.

- **NEW SYSTEM:** Additional Turns
- **CLARIFIED:** When an additional turn is created, it is owned by the player instructed to take it and inserted directly **after the current turn** into the repeating queue of turns
- **CLARIFIED:** Turn order remains unaffected by any additional turns
- **CLARIFIED:** After an additional turn is finished, it is removed from the queue

---

### Preventing Damage

Several cards instructed a player to "prevent" damage without defined rules for how it works. Prevent is now a game action and a delayed replacement effect — it creates a pool of prevented damage that acts as a shield on the affected units.

- **NEW RULE:** Prevent action added

---

### Discounts to Cost Components

Discounts that only affect a component of a cost will be applied when that component is added, before any other discounts are applied. This makes interactions like Vex and Ezreal (multiple discounts of different types applying to the same card) more intuitive.

- **CLARIFIED:** Discounts that only affect a specific component of a cost will apply as soon as that component is added to the total cost when finalizing a card or ability

---

### Main Phase Renamed

The **action phase** has been renamed the **main phase**.

Reason: The prevalence of terms with "action" (game actions, discretionary actions, limited actions, action keyword) muddled the meaning. The action keyword is the only of these printed on cards, and the naming conflation was particularly confusing.

- **CLARIFIED:** The action phase has been renamed the **main phase**

---

### Unique

*Unique* already existed on three cards in *Spiritforged* but never received a corresponding section in the keywords rules.

- **NEW RULE:** Unique as a keyword was added

---

### Backline

*Backline* is the keyword version of the ability on Caitlyn, Patrolling and Soraka, Wanderer requiring them to be assigned combat damage last.

Units with *Backline* must be assigned damage during the *Combat Damage Step* **after any other unit with the same controller that doesn't have *Backline***.

- **NEW RULE:** Backline as a keyword was added

---

### Attaching Again

Missing rule: an attached equipment could previously attach to the unit it's already attached to, which was unintuitive.

- **CLARIFIED:** Attaching a card to a new Top-Most Card will cause it to **Detach** from the card to which it is currently Attached
- **NEW RULE:** Attaching a card to its current Top-Most Card will not have any effect
- **NEW RULE:** If a Game Effect instructs a player to Attach a card to its current Top-Most Card, nothing additional happens

---

## Related Articles

1. [Vendetta Rules FAQ and Clarifications](https://playriftbound.com/en-us/news/rules-and-releases/vendetta-rules-faq-and-clarifications) — 2026-08-14
2. [Unleashed Rules FAQ and Clarifications](https://playriftbound.com/en-us/news/rules-and-releases/unleashed-rules-faq-and-clarifications) — 2026-04-29
3. [Unleashed Errata Updates](https://playriftbound.com/en-us/news/rules-and-releases/unleashed-errata-updates) — 2026-04-03
4. [Tournament Rules, January Update](https://playriftbound.com/en-us/news/announcements/tournament-rules-january-update) — 2026-01-30
5. [Riftbound Spiritforged FAQ](https://playriftbound.com/en-us/news/rules-and-releases/riftbound-spiritforged-faq) — 2026-01-14
6. [Riftbound Spiritforged Errata](https://playriftbound.com/en-us/news/rules-and-releases/riftbound-spiritforged-errata) — 2026-01-14
7. [Riftbound Core Rules: Spiritforged Patch Notes](https://playriftbound.com/en-us/news/rules-and-releases/riftbound-core-rules-spiritforged-patch-notes) — 2025-12-05
8. [Riftbound: Origins Card Errata](https://playriftbound.com/en-us/news/rules-and-releases/riftbound-origins-card-errata) — 2025-10-28
9. [Riftbound Core Rules: Patch Notes (Origins)](https://playriftbound.com/en-us/news/rules-and-releases/riftbound-core-rules-patch-notes) — 2025-10-24
