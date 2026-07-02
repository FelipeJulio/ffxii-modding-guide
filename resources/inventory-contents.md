# Inventory Contents

**Inventory Contents** is the master ID list for every "content" the game can reference: items, equipment, magicks, technicks, gambit conditions, key items, quest packages, rewards, mist unlocks, bazaar goods, and gil amounts.

**Credits:** Xeavin, Eochaid

### What can you do with this?

The game refers to almost everything by a "Content ID," and it uses one shared 16-bit ID space for every kind of content. That space is split into ranges by category: items start at `0x0000`, equipment at `0x1000`, magicks at `0x3000`, and so on. This sheet is the decoder ring: whenever another piece of game data (a loot table, a shop list, an action reward) points to "Content ID X," this is where you look up what X actually is.

**Spreadsheet contents:** each tab covers one ID range and shares the same columns (identifier in hex, identifier in decimal, name, and notes).

- **Items** (`0x0000`): consumables and usable items (Potion, Ether, Phoenix Down, status cures).
- **Equipment** (`0x1000`): every weapon, shield, and piece of armor, with a Model column linking to its model ID.
- **Loot** (`0x2000`): loot-range content, including some unused reserve slots.
- **Magicks** (`0x3000`): every spell.
- **Technicks** (`0x4000`): every technick (First Aid, Steal, Charge, Libra, and so on).
- **Gambits** (`0x6000`): the gambit target and condition strings shown in the Gambit menu, not the gambit abilities themselves.
- **Key Items** (`0x8000`): quest key items, largely area maps.
- **Packages** (`0x9000`): quest and hunt identifiers.
- **Rewards** (`0xA000`): reward slots.
- **Mist** (`0xB000`): chocobo and airship travel unlocks.
- **Bazaar Goods** (`0xC000`): the named mist and quickening-style abilities.
- **Prices** (`0xD000`): bazaar exchange set names.
- **Gil Sets** (`0xE000`): gil amounts, encoded linearly rather than naming an item (for example, `0xE000 + 0x01F4` is 500 gil).

{% hint style="info" %}
**Also in The Insurgent's Toolkit**
The Toolkit's Inventory Editor operates on this same category list. It can add or remove either a single content by ID (which this sheet resolves for you) or an entire category at once, live in a running game.
{% endhint %}

{% hint style="warning" %}
The game has a separate "Initial Inventory" data section that looks like it sets your starting inventory, but editing it has no effect: the game overwrites any changes. It is most likely a development leftover, not something worth pointing a mod at.
{% endhint %}

{% hint style="info" %}
**Access the spreadsheet**

<a href="https://onedrive.live.com/:x:/g/personal/553D7CDB377276FA/Qfp2cjfbfD0ggFWCAAAAAAAAOhIPm5hgWL8atA" class="button primary" target="_blank" data-icon="external-link-alt">Open the Spreadsheet</a>
{% endhint %}

{% content-ref url="battlepack-data-reference.md" %}
[battlepack-data-reference.md](battlepack-data-reference.md)
{% endcontent-ref %}
