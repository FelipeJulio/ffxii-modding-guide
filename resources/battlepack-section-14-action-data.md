# Battlepack Section 14: Action Data

**Battlepack Section 14: Action Data** is a full decode of Section 14, the game data section that defines every action (Magick, Attack, Item, Technick) in the game.

**Credits:** Eochaid

### What can you do with this?

Section 14 defines every action in the game: every Magick, Attack, Item, and Technick. This spreadsheet is the full decode of it, covering Actions 0 to 181, and it is where an action's real behaviour lives: its targeting rules, charge time, MP or Mist cost, damage formula, elements, statuses, and dozens of AI and gambit flags.

**Spreadsheet contents:**

- **Actions:** the main decode. Each row starts with the action's raw 32-byte hex string, then breaks it into every field: targeting (range, area size, which target types are valid), the damage formula it links to, costs, combat math (power, multipliers, accuracy, elements, on-hit rate), status effects, AI and gambit behaviour, animation links, and dozens of boolean flags (can be reflected, can be evaded, blocked by immunity, and so on). It ends with per-byte columns so you can hand-edit the raw bytes directly.
- **Data:** the lookup tables the Actions tab references: element bitflags (Fire = 1, Lightning = 2, Ice = 4, and so on), item IDs, animation IDs, summoned entities, and the AI reaction categories.
- **Old Version:** an earlier, more human-readable decode of the same data, kept for cross-checking. A gentler read if the full byte-and-flag view is overwhelming.

The sheet also includes a binary calculator: paste a raw hex string and it decodes every field for you, handy for previewing a custom action before writing it back into the game. Each action's formula field links to the Action Formulas Reference, so you can trace exactly how its numbers resolve.

{% hint style="danger" %}
Some action IDs are hardcoded (Quickenings 208-225, Concurrences 226-241, Summons 262-274, plus Shades of Black, Steal, Revive, Dismiss, and Spawn) and will not behave the same even if all their data is copied elsewhere. Swapping a Magick for another Magick is generally fine, but swapping across types (a Technick for an Item, for example) may not be, so avoid it unless you know the specific action is safe.

A few other things to keep in mind: avoid reusing reserve action IDs 147-484, since some are referenced by unknown internal functions (111-123 and anything after 497 are safer). Because party members and foes share the same action table, changing an action's effect can break enemy AI that depends on it (if Esuna stops removing Slow, an AI conditioned on "if I have Slow, cast Esuna" can loop forever). Reusing a Required Content ID across more than one action breaks inventory sort order, and gambit page or order changes require a game restart to take effect. Before repurposing an action ID, check how many enemies use it in Enemy Action Groups, since a high reference count means the change will ripple further than you expect.
{% endhint %}

{% hint style="info" %}
**Also in The Insurgent's Toolkit**
This data is edited live under Battlepack Editor > 14 : Actions.
{% endhint %}

{% hint style="info" %}
**Access the spreadsheet**

<a href="https://docs.google.com/spreadsheets/d/1nm3f5DvkKvkMlcr1oknpgJwnk7Ud3sgXPaHKTcXbJMM/edit" class="button primary" target="_blank" data-icon="external-link-alt">Open the Spreadsheet</a>
{% endhint %}

{% content-ref url="action-formulas-reference.md" %}
[action-formulas-reference.md](action-formulas-reference.md)
{% endcontent-ref %}
