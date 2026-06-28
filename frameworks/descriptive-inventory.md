# Descriptive Inventory

**The Insurgent's Descriptive Inventory** allows setting fully custom descriptions for any inventory content viewed in menus.

### What does it do?

The vanilla game generates descriptions dynamically for equipment, but with severe limitations: if a weapon has more than one element only the first is shown, more than 3 status effects collapse into "various status effects", elemental potency and metal value are never displayed, and so on. These issues become even more visible when using mods that modify equipment.

This mod replaces the dynamic descriptions with fully custom ones:

- Complete control over text styling: coloring, scaling, formatting, and other visual elements.
- Texts are no longer limited to 256 characters.
- Works for all inventory content types: items, equipment, loot, magicks, technicks, gambits, key items, and bazaar goods.
- A spreadsheet is available to help keep descriptions in sync with stat changes.

{% hint style="warning" %}
**Important:** Since descriptions are now static, any time you modify a content's stats you must also update its description manually, otherwise the player will see outdated information.
{% endhint %}

All parameters are loaded from `{game}/x64/scripts/config/TheInsurgentsDescriptiveInventoryConfig/{language}.lua`.

{% hint style="info" %}
**Note:** The **[Dynamic Description](dynamic-description.md)** framework integrates with this mod to generate real-time descriptions based on live battlepack data, solving the static text limitation.
{% endhint %}

{% hint style="info" %}
**Download & Documentation**

<a href="https://www.nexusmods.com/finalfantasy12/mods/319" class="button primary" data-icon="external-link-alt">Go to Official Mod Page</a>
{% endhint %}
