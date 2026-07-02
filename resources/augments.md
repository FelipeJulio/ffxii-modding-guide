# Augments

**Augments** is an in-progress catalogue of every augment in the game.

**Credits:** Eochaid

### What can you do with this?

An augment is the passive ability granted by equipping certain accessories, or unlocked as a License Board node: things like Adrenaline, Spellbreaker, the various Lores, or a flat HP bonus. This sheet lists all 129 augments (IDs 0 to 128), one per row, with everything you need to identify and edit one.

For each augment you get:

- **What it does**, in plain language, plus the numeric parameter some augments use (the flat bonus for "HP +30", the percentage for "Potion Lore 3", and so on).
- **The accessory that grants it**, where one exists. Most augments here are License Board only, so this field is often blank.
- **The internal ability ID** (the 13000 to 13128 range). This is the number other game data uses to point at an augment, since gear and licenses reference augments by ID, not by name.
- **The in-game description text ID** (the 20480 range) and the description shown for it in menus.
- **Community alternate names** for augments that were never given a clear official name. Augment 33, for example, is variously called Null Aggro, Cloak, Subterfuge, Veil, or Shroud.

Many augments repeat the same effect at several power tiers, such as "Battle Lore" or "Magick Lore" at 30, 50, 70, and 100. Each tier is its own row with its own ID, because the game distinguishes them by number rather than by name.

{% hint style="info" %}
**Also in The Insurgent's Toolkit**
The same data can be edited live under Battlepack Editor > 58 : Augments, where you can do things like change how much HP an HP Lore grants or give an augment a timer.
{% endhint %}

{% hint style="info" %}
**Access the spreadsheet**

<a href="https://docs.google.com/spreadsheets/d/1IaG6MYV01C2IJW9dmk54Vgrvv1mN3ZvcSpPi5y0sCxc/edit" class="button primary" target="_blank" data-icon="external-link-alt">Open the Spreadsheet</a>
{% endhint %}

{% content-ref url="hp-augment-totals.md" %}
[hp-augment-totals.md](hp-augment-totals.md)
{% endcontent-ref %}
