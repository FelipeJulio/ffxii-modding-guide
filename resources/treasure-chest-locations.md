# Treasure Chest Locations

**Treasure Chest Locations** is the full list of every treasure chest in the game, its exact location, and its loot table.

**Credits:** Eochaid, Xeavin, ffgriever

### What can you do with this?

Nearly 2,000 treasure chests exist in the game, and this sheet documents every one of them, with the raw bytes and the decoded values side by side.

**Spreadsheet contents:**

- **Chest Data:** the main table, one row per chest. Each row gives the source file and area the chest belongs to, its map coordinates, its spawn chance, and any story-flag conditions that control whether it appears. Its loot is where the Diamond Armlet matters: a chest rolls one of two tables depending on whether the player has a Diamond Armlet equipped, so each row lists both the normal item and gil and the Diamond Armlet item and gil. The raw hex bytes for every field sit alongside the decoded values, for when you want to hand-edit chest data directly.
- **Inventory:** a simple reference list of item names and their content IDs, the source the item-name fields in Chest Data are drawn from.

{% hint style="info" %}
**Also in The Insurgent's Toolkit**
Chests are edited through the EBP Editor (listed there as "Treasures"), which works on whichever `.ebp` file is loaded in memory. Use it for small in-place tweaks; for a larger overhaul across many chests, the community-preferred tool is the FF12 VM Script Decompiler. Check the Locations sheet if you need to know which `.ebp` file an area uses.
{% endhint %}

{% hint style="info" %}
**Access the spreadsheet**

<a href="https://docs.google.com/spreadsheets/d/1ZSwmTg18JVqgRNb0StEaBtPJAKKtV4DMiS9PNWL4Q8I/edit" class="button primary" target="_blank" data-icon="external-link-alt">Open the Spreadsheet</a>
{% endhint %}

{% content-ref url="inventory-contents.md" %}
[inventory-contents.md](inventory-contents.md)
{% endcontent-ref %}

{% content-ref url="locations.md" %}
[locations.md](locations.md)
{% endcontent-ref %}
