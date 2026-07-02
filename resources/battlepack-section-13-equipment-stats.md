# Battlepack Section 13: Equipment Stats

**Battlepack Section 13: Equipment Stats** is the full raw dump of Section 13, the game data section that defines the mechanical stats of every weapon, shield, helm, armor, and accessory.

**Credits:** Eochaid

### What can you do with this?

Section 13 is the game data that gives every piece of gear its mechanical stats. This spreadsheet is the full raw dump of it, one row per gear item, covering all 420 weapons, shields, helms, armor, and accessories. Each row has roughly 47 columns, though most stay blank for any given item since a weapon only uses a handful of them.

The columns group into a few kinds:

- **Identification:** the item's ID, name, icon, and model.
- **Economics:** its gil price, sale value, and menu sort order.
- **Weapon combat stats:** range, the damage formula it uses, attack power, knockback, combo and crit rates, evade, charge time, and stance. Populated for weapons.
- **Defensive stats:** defense and magick resist. Populated for armor and shields.
- **Attribute link:** an `Attrib ID` that points to the Equipment Attribute Reference sheet, which holds the item's bonus stats and status effects.
- **Elemental and status block:** the element it deals, its on-hit chance, statuses it inflicts, statuses it grants while equipped, and its elemental affinities.

Any change to how hard a weapon hits, how much an armor blocks, or what elemental or status properties a piece of gear carries goes through this data.

{% hint style="danger" %}
Do not reorder equipment or change an item's type unless you are swapping within the same category. The game calculates gear by order and by type, so doing otherwise breaks inventory sorting and type checks. Each type also has an inventory slot limit: Weapons 200, Armor (including shields) 140, Accessories 48, Ammunition 32.
{% endhint %}

{% hint style="info" %}
**Also in The Insurgent's Toolkit**
This data is edited live under Battlepack Editor > 13 : Equipment & Attributes.
{% endhint %}

{% hint style="info" %}
**Access the spreadsheet**

<a href="https://docs.google.com/spreadsheets/d/1NZ0ezAqZ4bYecIsHbF04aYdsuZykOePa90aYnR6KuiI/edit" class="button primary" target="_blank" data-icon="external-link-alt">Open the Spreadsheet</a>
{% endhint %}

{% content-ref url="equipment-attribute-reference.md" %}
[equipment-attribute-reference.md](equipment-attribute-reference.md)
{% endcontent-ref %}
