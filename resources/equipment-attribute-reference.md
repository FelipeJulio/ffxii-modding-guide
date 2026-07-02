# Equipment Attribute Reference

**Equipment Attribute Reference** is a spreadsheet mapping every gear Attribute ID to the stat bonuses and status effects it grants.

**Credits:** Eochaid

### What can you do with this?

In the game's data, a weapon or piece of armor does not store its bonus stats directly. Instead it stores an Attribute ID that points to a shared attribute block. This sheet is the decoder for those blocks: it lists all 177 Attribute IDs and, for each one, what it actually grants.

For each attribute you get:

- **Used By Gear:** every weapon, armor, or accessory that references this attribute.
- **Stat bonuses:** the numeric Max HP, Max MP, Strength, Magick, Vitality, and Speed it adds (blank where none).
- **Status Effects:** free-text effects, from elemental affinities (absorb, half, weak) and immunities to named effects like Regen, Haste, or Bravery.

Any gear not listed here uses Attribute ID 0, which grants nothing. The list is meant to be exhaustive across all 420 gear items.

One thing to keep in mind while editing: a single attribute is often shared by many items. Because gear only stores the ID, changing an attribute changes every item that uses it, not just the one you have in mind.

{% hint style="warning" %}
Attribute 0 is the placeholder for "no bonus" and should never be modified. Changing it can affect any gear that was never meant to have an attribute at all.
{% endhint %}

{% hint style="info" %}
**Also in The Insurgent's Toolkit**
This sheet backs the Battlepack Editor > 13 : Equipment & Attributes section. The editing flow is to pick a new attribute here, copy its offset, and paste it into the equipment's Attribute Offset field.
{% endhint %}

{% hint style="info" %}
**Access the spreadsheet**

<a href="https://docs.google.com/spreadsheets/d/1S0TqQV5cTynoT3VVecvytEuMm5EAMxTp2Cx_-_GL0OU/edit" class="button primary" target="_blank" data-icon="external-link-alt">Open the Spreadsheet</a>
{% endhint %}

{% content-ref url="battlepack-section-13-equipment-stats.md" %}
[battlepack-section-13-equipment-stats.md](battlepack-section-13-equipment-stats.md)
{% endcontent-ref %}
