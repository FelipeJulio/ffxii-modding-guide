# Battlepack Data Reference

**Battlepack Data Reference** is a full inventory of everything defined inside `battle_pack.bin`, the game file that holds nearly all battle-related data.

**Credits:** Xeavin

### What can you do with this?

`battle_pack.bin` is the single file that stores almost all of the game's battle data: actions, gear, statuses, menu structure, shops, maps, and more. This spreadsheet is the full inventory of what lives inside it, spread across 26 tabs. Every tab shares the same four columns: the identifier in hex, the same identifier in decimal, the name, and notes (which flag reserved or unused slots).

**Spreadsheet contents:** the tabs fall into two kinds.

- **Content ID tables** list actual game content by ID: actions (Cure, Blindna, Vox, and so on), equipment, magicks, technicks, gambits, key items, packages, rewards, mist, bazaar goods, prices, loot, and party members. These cover the same ID ranges documented in more detail in Inventory Contents.
- **Category and enum tables** are the smaller, fixed lookups the game and its menus use to group things: battle menu categories (Attack, Magicks, Technicks, Items, Summon, and more), elements (Fire, Lightning, Ice, Earth...), status effects (KO, Stone, Petrify, Sleep...), equipment categories, weapon stances, magick categories, license node categories, concurrences (the Mist combos), maps (every named area), shops, teleport destinations, and story-point flags.

One gotcha worth knowing: each tab uses its own ID numbering, local to that category. The IDs here do not line up with the shared content IDs in Inventory Contents, so treat every tab's numbers as belonging only to that tab.

{% hint style="info" %}
**Also in The Insurgent's Toolkit**
These tabs correspond to the numbered sections of `battle_pack.bin`. You can edit the same data live under Battlepack Editor, where each tab appears as its numbered section.
{% endhint %}

{% hint style="info" %}
**Access the spreadsheet**

<a href="https://onedrive.live.com/:x:/g/personal/553D7CDB377276FA/Qfp2cjfbfD0ggFWAAAAAAAAA6U_H6L8BJTkZYg" class="button primary" target="_blank" data-icon="external-link-alt">Open the Spreadsheet</a>
{% endhint %}

{% content-ref url="inventory-contents.md" %}
[inventory-contents.md](inventory-contents.md)
{% endcontent-ref %}
