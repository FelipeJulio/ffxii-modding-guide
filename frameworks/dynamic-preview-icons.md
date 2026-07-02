# Dynamic Preview Icons

**Dynamic Preview Icons** fully reworks the preview icon system for inventory content in Final Fantasy XII.

**Credits:** Xeavin

### What does it do?

In the vanilla game, preview icons (shown in the equipment menu when selecting weapons, armor, accessories, etc.) are stored in compressed image packs with a fixed resolution of 64×96. Each pack contains up to 64 icons sharing a single 256-color palette, severely limiting color detail per icon. Icons are also tied to equipment identifiers rather than models, meaning swapping a weapon model does not update its icon.

This mod replaces that system entirely:

- Icons now use individual texture files instead of shared packs.
- Resolution doubled to **128×192** (or kept at 64×96 via the Small Icons variant).
- Every icon gets its own 256-color palette.
- Icons are assigned by **file name** mapped to their content identifier (e.g., `.../equipment/1.tm2` for equipment ID 1).
- Weapons and off-hands can use icons mapped by **model identifier**, so icons update automatically when the model changes.
- Adds icon support for items, loot, magicks, technicks, gambits, key items, and bazaar goods.
- Inventory content without icons no longer shows an empty border.
- Swapping icons only requires renaming files: no pack rebuilding or palette reconstruction needed.

{% hint style="info" %}
**Download & Documentation**

<a href="https://www.nexusmods.com/finalfantasy12/mods/487" class="button primary" target="_blank" data-icon="external-link-alt">Go to Official Mod Page</a>
{% endhint %}
