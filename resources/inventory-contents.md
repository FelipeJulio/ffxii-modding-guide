# Inventory Contents

**Inventory Contents** is the master ID list for every "content" the game can reference: items, equipment, magicks, technicks, gambit conditions, key items, quest packages, rewards, mist unlocks, bazaar goods, and gil amounts.

**Credits:** Xeavin, Eochaid

### What can you do with this?

The game uses one shared ID space for all of these categories, split into ranges (item IDs start at `0x0000`, equipment at `0x1000`, magicks at `0x3000`, and so on, all the way to gil sets at `0xE000`, which encode gil amounts linearly rather than naming an item). This sheet is the decoder ring for "Content ID X" wherever it shows up in other game data, loot tables, shop lists, action rewards, and more. It matches The Insurgent's Toolkit's Inventory Editor, which lets you add or remove any of these categories directly in a live save, either a single content by ID or an entire category at once.

{% hint style="warning" %}
The game's "Initial Inventory" data section (a separate battle_pack.bin section, not part of this sheet) documents starting-inventory data, but editing it has no effect on the game at all, any changes are overwritten anyway. It's likely a development leftover, not something worth pointing a mod at.
{% endhint %}

{% hint style="info" %}
**Access the spreadsheet**

<a href="https://onedrive.live.com/:x:/g/personal/553D7CDB377276FA/Qfp2cjfbfD0ggFWCAAAAAAAAOhIPm5hgWL8atA" class="button primary" target="_blank" data-icon="external-link-alt">Open the Spreadsheet</a>
{% endhint %}

{% content-ref url="battlepack-data-reference.md" %}
[battlepack-data-reference.md](battlepack-data-reference.md)
{% endcontent-ref %}
