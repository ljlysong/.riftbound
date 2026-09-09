# Core Rules: Vendetta Patch Notes

> **Published:** 2026-07-17  
> **Source:** https://playriftbound.com/en-us/news/announcements/core-rules-vendetta-patch-notes/  
> **Effective Date:** July 24, 2026

---

Welcome to the patch notes for *Riftbound: Vendetta*. Included are the new rules required to play with the mechanics in the *Vendetta* set, as well as fixes to many logical and procedural errors.

### Goals for This Update

**Primary goal:** Support the new cards in *Vendetta* when it releases to English & Chinese audiences **simultaneously**. Compared to the *Unleashed* rules update, more energy is focused on new rules and systems for *Vendetta* than updates to overall mechanics. Bug fixes and clarifications are still present but are a smaller focus.

**Secondary goal:** Share the reasoning behind changes so players understand why they are necessary and what cards or functions they support. Not all changed rules are included in this document — only significant ones that merited deeper community explanation. All changes described in the *Unleashed* FAQ have also been reproduced in the Core Rules Document and are included here for completeness.

> **Timing note:** This rules update is being released slightly early compared to previous cadence, based on player feedback from the *Unleashed* update. This gives judges and players plenty of time to read relevant rules before the first Pre-Rift events.

---

## Patch Notes

### Vendetta Addition: Empower, Empowered, Disempower

*Empower* is the tentpole mechanic of *Vendetta*. Units, gear, and legends can be empowered or disempowered.

- **Empowered** is a status that lasts indefinitely until the card leaves the board or is disempowered. The empowered status does nothing on its own but can be referenced by other effects.
- **Empower** is an activated ability with an associated cost. Pay the cost and your unit becomes empowered. You can only activate this ability if the unit **isn't already empowered**.
- **Empowered ability:** Cards with an *Empower* ability likely also have an *Empowered* ability — a dependent keyword whose condition is the card having the empowered state. While the card is empowered, the extra effect is active.
- **Disempower** is an instruction or cost that removes the empowered status from a card. You **cannot** disempower something that isn't empowered.

- **NEW RULE:** Empower keyword added
- **NEW RULE:** Empowered keyword added
- **NEW RULE:** Empower action added
- **NEW RULE:** Disempower action added
- **NEW RULE:** Empowered state added

---

### Vendetta Addition: Flow

The second key mechanic — allows players to play spells from their trash.

- *Flow* is a keyword that appears on **spells**.
- It is a **permission and an alternate cost**: by playing a spell for its Flow cost, you can play it from the trash, then banish it. One and done.
- Cards with Flow have a nifty symbol on their text box to indicate they have a function from your trash. This symbol will appear on more cards in the future when players should pay attention to a card in the trash.

- **NEW RULE:** Flow keyword added

---

### Vendetta Addition: Burn

Allows players to take cards directly from their Main Deck and put them in the trash.

- To **burn X**, a player takes X cards from the top of their Main Deck and puts them in their trash.
- Cards can **trigger when burned**, or when you burn a card.
- Effects can count the **number of cards burned in a turn**.
- Burning cards can bring you closer to burning out, but can also add valuable *flow* cards to your trash.

- **NEW RULE:** Burn action added

> *Danger and value go hand in hand.*

---

### Vendetta Addition: Skip

For the first time, a card allows a player to skip part of their turn. *Skip* is a **replacement effect** that replaces the named event or procedure of the turn with nothing. Anything that would occur as a result of that event or procedure doesn't happen instead.

- **NEW RULE:** Skip action added

> *Poof! It's gone. No triggers, no procedures, nada. Zip! Zilch!!*

---

### Vendetta Support: Naming Cards, Types, and Tags

*Vendetta* adds a card that instructs a player to name a card, in addition to the List from *Unleashed* that instructs a player to name a tag. Rules now define the function and process by which a player names a card, type, or tag.

- Naming a **card** is the most complex of the three and has special rules to give players flexibility.
- Naming a **type** or **tag** is simpler.

- **NEW RULE:** Naming cards, types, and tags added

---

### Vendetta Support: Ignoring Effects

A new class of effect added in *Vendetta*: the ability to **ignore certain abilities or effects**. The machinery of inactive text allows these effects to operate cleanly and should be fairly intuitive to players.

- **NEW RULE:** Ignoring effects added

---

### Vendetta Support: Untargetability

In *Unleashed* there was one card that could make a card unable to be chosen by enemy spells and abilities based on a condition. In *Vendetta*, several new such effects are introduced. A unit with this property is called **untargetable**.

- If a unit becomes untargetable **after** a spell or ability has already targeted it, the spell or ability will **mistarget on resolution**: any instructions related to that unit will be ignored.
  - This is the same principle as a unit being targeted by Void Seeker and moved to base in reaction — when Void Seeker resolves, instructions related to that unit are ignored because it's no longer at a battlefield as required.

- **NEW RULE:** Untargetability added

---

### Vendetta Support: Making New Choices

*Vendetta* adds the second card that allows a player to make new choices for a spell on the chain. Rules clarify the timing, legality, and nature of choices allowed to be remade.

- **NEW RULE:** Making new choices added

---

### Vendetta Support: Activated Ability Terminology

As of *Vendetta*, terminology for activated abilities in card text is shifting. Previously, cards used "used" to refer to activating an activated ability, causing confusion about how it differs from playing a card. *Vendetta* moves to the word **"play"** to refer to the act of activating an ability in card text. The Core Rules Document has been updated to refer to both uses.

- **NEW RULE:** "Use" and "play" supported for activated ability card text

---

### Vendetta Support: Cards with Multiple Types

*Vendetta* introduces Riftbound's **first card with multiple card types**. Rules clarify how cards with multiple types function.

- **NEW RULE:** Cards with multiple types added

---

### Vendetta Support: Replacement Effects and Combat Damage

*Prevent* becoming more prevalent set the stage for a closer look at how replacement effects interact with combat damage assignment.

**Problem:** 'Prevent' as a replacement effect could modify how combat damage is *assigned*, while any other replacement effect that interacts with damage only applied at the moment that damage was *dealt*. This led to very strange situations given how strict combat damage assignment rules have to be.

**Fix:** Any replacement effect that would modify damage dealt to units during combat damage is applied to **combat damage assignment** instead. Combat damage assignment rules have also been updated to remove inconsistencies.

> **Note:** This means combat damage assignment when a unit has a replacement effect that *increases* damage (like Lotus Trap) will become slightly more complicated, as players must incorporate those replacement effects into their assignment calculations. The team believes this slight added complexity is worth the increased intuitiveness of these effects having the same timing.

- **NEW RULE:** When assigning damage during the combat damage step, replacement effects that would apply to the resulting damage are considered to apply to the assignment instead

---

### Rules Update: Copying Tokens

**Token is no longer a supertype.** It being a supertype made several cards work in problematic ways and wasn't entirely intuitive. Now, regardless of how a token is manipulated, copied, or altered, it will maintain its tokenness. Cards cannot become tokens for any reason.

- **NEW RULE:** "Token" is an intrinsic category of Game Objects, in the same way "card" is
- **NEW RULE:** Token Game Objects cannot lose their token nature by any means
- **NEW RULE:** Card Game Objects cannot become tokens by any means

---

### Rules Update: (Resource) Payment Optional

A discrepancy was noticed: if an Energy or Power cost is instructed to be paid and a player has that resource in their rune pool, they do **not** have the choice to avoid paying it. However, if they don't have that resource, nothing can compel them to generate it — if they don't generate it, the action is ignored.

The difference between being compelled to spend a resource vs. generate one is relatively small, yet it created unintuitive differences depending on whether a player had "floating" Energy or Power.

**Fix:** Payment of Energy and Power is now **optional in all cases**, unifying these two scenarios.

**Scope of change:** Only affects cards like Diana, Lunari, Promising Future, and Cursed Sarcophagus that either instruct a player to pay Energy or Power, or instruct them to play a card without ignoring all of its costs. Regardless of whether a player has Energy or Power floating, they can choose either not to generate those resources or not to spend them.

> **This only applies to Energy and Power.** Any other cost can be compelled to be performed as long as the instructed player has the ability to do so.

- **NEW RULE:** When a player is instructed to Pay a resource, that player may remove that resource from their Rune Pool if it exists there. If they choose not to, the instruction is ignored.

---

### Rules Update: Costs on Multi-Domain Cards

It was strange that signature cards' power costs could be paid with power of any domain, since the power cost symbols have the colors of their domains. Players intuitively felt you should pay with only power of those domains.

**Fix:** Power cost rules updated for cards of multiple domains — you must pay for a signature card's power cost with power of that card's domains. If there is an `[A]` symbol in the card's text, that can still be paid with power of any domain.

- **CLARIFIED RULE:** A `[C]` shorthand on a card with multiple Domains is processed as any power of that card's Domains

---

### Rules Update: Applied Costs

A class of abilities that apply a cost to an action outside of playing a card (e.g., Mageseeker Investigator) were previously underdefined. These abilities now have a name: the costs applied by them are **applied costs**.

- **NEW RULE:** Applied costs added

---

### Rules Update: Deathknell and "When I Die" Alignment

The *Spiritforged* rules update changed Deathknell rules to allow them to use information from when its source was on the board. This was much needed but left other abilities that similarly triggered "When I die" lagging behind.

**Fix:** Any "When I die" triggered ability can now use information from **before its source died**.

- **NEW RULE:** Deathknell and "When I die" abilities aligned

---

### Rules Update: Gone Before Its Time

**Question:** What happens to a delayed ability if its trigger time passes or its duration is completed before the delayed ability is generated? Do you perform the action anyway? Or is it ignored?

**Answer:** If a Delayed Ability's duration has ended before it was generated, the Delayed Ability is **not generated** and any instructions related to it are ignored.

- **NEW RULE:** If a Delayed Ability's duration has ended before it was generated, the Delayed Ability is not generated and any instructions related to it are ignored

---

### Rules Update: Event Definition

With more instances of replacement effects replacing increasingly complex events, a clear definition of *event* is needed.

- **NEW RULE:** An event is the singular moment that results from a Game Action being performed or from a Game Object changing state

---

### Rules Update: New Replacement Effects

Three categories of card text that were previously undefined are now recognized as replacement effects:

1. **Abilities that describe how a unit enters** (or an action to be performed as a unit enters) are replacement effects — they replace the unit entering as normal with the unit entering in the appropriate state.
2. **Abilities that instruct a game action to occur "as" an event happens** are replacement effects that replace the stated event with that event **and also** the game action being performed.
3. **Abilities that instruct a player to "then banish it" or "then recycle it"** are replacement effects that are short for: "if it would leave the chain after becoming a finalized chain item, and leaving the chain wasn't instructed by its own execution, perform the specified game action instead."

- **NEW RULE:** New replacement effects added

---

### Rules Update: Battlefield Reuse

Specifically supports high-level competitive events that may run top-cut as **best-of-5**. Also addresses drawn games that could require four games in a best-of-3 match.

- **NEW RULE:** In a Best of 5 match, during games 4 and 5, players may present a battlefield that has been **removed from the game**
- **NEW RULE:** Players may only re-use a battlefield this way if they have already presented each of their battlefields at least once during the match, and present a battlefield **at most twice** in a given match
- **NEW RULE:** If no player won a game, the battlefields presented for that game may be **reused** in a subsequent game

---

### Contested Removal

Rules didn't state explicitly how contested status is removed from a battlefield if a showdown never occurs (e.g., a unit's move trigger moves it to a battlefield and the controller plays Flash targeting it, returning it to base before the showdown can open — without a rule, the battlefield is stuck in contested limbo).

**Fix:** Contested status is removed when the player who applied it doesn't have any units there.

- **NEW RULE:** In a cleanup, remove Contested status from each Battlefield without Units controlled by the player who applied Contested to that Battlefield and without a Showdown or Combat ongoing there
- **NEW RULE:** If as a result of the removal of Contested status there are Units at an uncontested Battlefield that their controller does not control, their controller applies Contested status to that Battlefield

---

### Targeting Clarification

First addition to the targeting disqualification list since it was codified in the second *Origins* rules update:

**New disqualification:** If a player, zone, or game object appears **only as a restriction or permission for a game action**, then it is not a target.

This means Thrill of the Hunt, Here to Help, and similar effects that instruct you to perform an action "to a battlefield" **don't target that battlefield**. The restriction or permission is applied to the resulting action and is not a decision made on finalization.

- **CLARIFIED RULE:** A player, zone, or game object isn't a target if it is included only as part of a targeting restriction for another choice or only as a restriction or permission for a game action

---

### Splitting Up

Split damage rules clarified — specifically what happens if the amount of damage being split is reduced between choosing targets and when the spell or ability resolves.

- **CLARIFIED RULE:** If, at resolution of the spell or effect, there are more Targets than available damage to divide, then the player who controls the effect dealing damage determines which Targets cease being Targets
- **NEW RULE:** That player cannot choose to have fewer Targets than they have damage to split when choosing which Targets cease being Targets

---

### 2v2 Rules Clarifications

- **CLARIFIED RULE:** Points are shared by a team in the 2v2 game mode
- **CLARIFIED RULE:** Battlefield control is checked during the **scoring step**. Battlefields controlled by a teammate during the scoring step of a player's beginning phase are ineligible to be scored by that player's team during that turn and count towards the final point rule.

---

### Hidden Targeting

The wording on the hidden targeting restriction wasn't clear about whether it applied to each targeting decision individually or all of them collectively.

**Fix:** Each choice is treated individually when applying the hidden targeting restriction.

- **CLARIFIED RULE:** The restriction on targets chosen by hidden spell and play effects is applied to **each target separately and individually**

---

### Trigger Condition and Effect

The *Unleashed* rules update brought major changes to how Triggered Abilities are parsed, and the *Unleashed* FAQ provided deeper explanation. That explanation has now been reproduced in the Core Rules Document.

**How triggered abilities are parsed:** Triggered abilities are split into two sections:
1. **First section** (not on the chain): the trigger condition, any extra conditional statement, the words "you may," and a cost within instructions (`[Do X] to [Do Y]`). These represent conditions, choices, and costs made before or as the chain item becomes a finalized item.
2. **The actual triggered ability:** what goes on the chain.

**Notable change from previous update:** The timing of when "you may" or "they may" choices are made when they appear as the first part of the effect of a triggered ability. Previously, decisions were made when the ability triggered (to support "once each turn" triggered abilities). Updated phrasing now allows the decision to be made **on finalization** instead.

> Intuition: Think of "once each turn" as referring not to the ability triggering once each turn, but to **playing the triggered ability to the chain as a finalized chain item** once each turn. If it never became a finalized chain item, you haven't "done" it.

- **CLARIFIED RULE:** Trigger condition and effect have been made more clear and given direct examples
- **CLARIFIED RULE:** Timing for "you may" or "they may" when it appears as the first part of the effect of a triggered ability has been changed to **finalization**

---

### "Play" Definitions

There are three uses of "play" in Riftbound:

| Context | Meaning |
|---|---|
| **Play as game action** — e.g., "You may play a unit to a battlefield you control" (Here to Help) | "Put the card or ability on the chain and queue it to be finalized" |
| **Play in triggered abilities** — e.g., "When you play me, draw 1" (Lecturing Yordle) | "Resolve" |
| **Play in any other context** — e.g., "I cost [1] less for each card you've played this turn" (Battering Ram) | "Finalize" |

> The team acknowledges the manifold use of "play" has been a sore spot. A major upcoming change to templating and card wording is planned that will make this significantly easier to understand.

- **CLARIFIED RULE:** Any triggered abilities that trigger when cards are played trigger when the act of playing the card has been completed by the **resolution** of the card
- **NEW RULE:** Non-triggered abilities that check cards being played do so by means of referencing whether said cards have been **Finalized**

---

### Oh Damage, My Damage

**Lethal Damage:** Previously referenced obliquely in three different sections and only actually named in one. This made changes to the definition (like Elder Dragon's passive ability) unclear as to which section might apply. The *Unleashed* FAQ clarified all three instances refer to the same concept, and modification to one modifies all of them. This is now reflected directly in the Core Rules Document.

**"Your damage":** Defined in the *Unleashed* FAQ as "damage you marked on units." Now added directly to the rules.

- **CLARIFIED RULE:** Lethal damage has been unified across the document
- **NEW RULE:** Game Effects may refer to a player's Damage. This means the Damage **marked by that player**.

---

### Battlefield Ability Control

From the *Unleashed* FAQ: the player who makes a choice for a triggered ability of a battlefield is the one who is responsible for that ability and puts it on the chain. Now reflected directly in the Core Rules Document.

- **NEW RULE:** If an Ability of a Battlefield indicates that a specific player makes a choice, that player is the Ability's controller. They take responsibility for adding it to the chain if applicable and make all choices required by the ability. They and only they control the ability, regardless of who controls the Battlefield.

---

### Counting Targets

From the *Unleashed* FAQ (specifically for cards like Repulse): clarification on what kinds of targets count and in what situations for effects that check the number of targets a spell has. Now addressed directly in the Core Rules Document.

- **NEW RULE:** If another spell or ability attempts to reference the number of game objects, players, or zones that a Finalized Chain Item targets, it will include any **mistargeted choices**, but **not** any targets that have changed to a non-board zone

---

### I'm Getting Activated

From the *Unleashed* FAQ: "activate" when appearing on card text was underdefined. Now defined.

- **NEW RULE:** Some effects may instruct a player to "activate" a named triggered ability. To do so, that player checks the condition of all of the specified effects, **as if they had fulfilled the named part of the condition**

---

### Accelerate

From the *Unleashed* FAQ: Accelerate is an ability made up of two parts — an optional additional cost, and a delayed replacement effect that is generated when you pay the cost. Now reflected in the rules themselves.

- **CLARIFIED RULE:** Paying the accelerate cost generates a delayed Replacement Effect. Even if the unit loses the accelerate keyword during the finalization process, as long as the cost was paid, that unit will still enter ready.

---

## Related Articles

1. [Riftbound at PAX West 2026](https://playriftbound.com/en-us/news/announcements/riftbound-at-pax-west-2026) — 2026-08-28
2. [Riftbound Preorder Drawing FAQ](https://playriftbound.com/en-us/news/announcements/product-drawing-faq/) — 2026-08-10
3. [August Merch Store Updates](https://playriftbound.com/en-us/news/announcements/august-merch-store-updates) — 2026-08-06
4. [Riftbound's Creators in 2027](https://playriftbound.com/en-us/news/announcements/riftbounds-creators-in-2027) — 2026-08-05
5. [August 2026 State of the Game](https://playriftbound.com/en-us/news/announcements/august-2026-state-of-the-game) — 2026-08-03
6. [Products and Sets into 2027](https://playriftbound.com/en-us/news/announcements/products-and-sets-into-2027) — 2026-08-03
7. [Vendetta Errata Updates](https://playriftbound.com/en-us/news/announcements/vendetta-errata-updates) — 2026-07-23
8. [Preparing for the Vendetta Pre-Rift](https://playriftbound.com/en-us/news/announcements/preparing-for-the-vendetta-pre-rift) — 2026-07-20
9. [Riftbound: Vendetta, Wild Rift, and You!](https://playriftbound.com/en-us/news/announcements/riftbound-vendetta-wild-rift-and-you) — 2026-07-17
