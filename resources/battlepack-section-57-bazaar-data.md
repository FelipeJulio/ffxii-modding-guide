# Battlepack Section 57: Bazaar Data

**Battlepack Section 57: Bazaar Data** is the full decode of Section 57, the game data section that defines every bazaar recipe.

**Credits:** Eochaid

### What can you do with this?

A bazaar recipe turns a set of loot ingredients you are carrying into a purchasable good. Section 57 is where those recipes are defined, and this spreadsheet decodes all of them, roughly 99 entries.

**Spreadsheet contents:**

- **Bazaar Calculator:** the main reference. Each row is one bazaar entry, starting with its raw hex string and then every decoded field: its name, up to three reward and count pairs, the gil cost, a repeatability flag (non-repeatable, repeatable, or monograph), up to three ingredient and count pairs, and its icon. This tab doubles as a calculator: paste a new raw hex string and it decodes the entry for you, useful for testing a custom recipe before committing it.
- **Data:** a per-entry byte breakdown, splitting each raw hex string into individual labeled byte columns so you can see exactly which offset encodes which field.
- **Decoder:** a small helper that maps a two-byte item or gil code to its name and decimal ID, for decoding a raw ingredient or reward pair you find elsewhere.
- **Vanilla Dumpers:** a validation tab that compares the original bytes against a re-encoded version byte by byte, used by the author to confirm the decode round-trips correctly.

{% hint style="warning" %}
When a reward or ingredient slot is unused, the game still lists it as Potion with quantity 0. That is not a real requirement, it just means "nothing here."
{% endhint %}

{% hint style="info" %}
**Also in The Insurgent's Toolkit**
This data is edited live under Battlepack Editor > 57 : Bazaar Goods.
{% endhint %}

{% hint style="info" %}
**Access the spreadsheet**

<a href="https://docs.google.com/spreadsheets/d/1joQbsDI60eVm4eOY93k61TgmQJbckrCSasdEiX9_j6g/edit" class="button primary" target="_blank" data-icon="external-link-alt">Open the Spreadsheet</a>
{% endhint %}

{% content-ref url="inventory-contents.md" %}
[inventory-contents.md](inventory-contents.md)
{% endcontent-ref %}
