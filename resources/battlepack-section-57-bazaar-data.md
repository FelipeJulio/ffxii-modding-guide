# Battlepack Section 57: Bazaar Data

**Battlepack Section 57: Bazaar Data** is the full decode of Section 57, the game data section that defines every bazaar recipe.

| Credits |
| --- |
| Eochaid |

### What can you do with this?

Every bazaar good's ingredients, rewards, gil cost, and repeatability flag comes from Section 57. This spreadsheet decodes it entry by entry, with a binary calculator tab for previewing custom entries from raw hex before writing them back into the game, plus a byte-decoder helper and a validation tab that checks the decode logic round-trips correctly.

{% hint style="warning" %}
When a reward or ingredient slot is unused, the game still lists it as Potion with quantity 0, that isn't a real requirement, it just means "nothing here."
{% endhint %}

{% hint style="info" %}
**Access the spreadsheet**

<a href="https://docs.google.com/spreadsheets/d/1joQbsDI60eVm4eOY93k61TgmQJbckrCSasdEiX9_j6g/edit" class="button primary" data-icon="external-link-alt">Open the Spreadsheet</a>
{% endhint %}

{% content-ref url="inventory-contents.md" %}
[inventory-contents.md](inventory-contents.md)
{% endcontent-ref %}
