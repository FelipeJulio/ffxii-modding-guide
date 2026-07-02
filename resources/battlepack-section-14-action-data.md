# Battlepack Section 14: Action Data

**Battlepack Section 14: Action Data** is a full decode of Section 14, the game data section that defines every action (Magick, Attack, Item, Technick) in the game.

**Credits:** Eochaid

### What can you do with this?

Every action's targeting rules, charge time, MP/Mist cost, damage formula link, elements, statuses, and dozens of AI/gambit behavior flags live in Section 14. This spreadsheet decodes it action by action, with a "binary calculator" tab you can paste new raw hex into to preview how it would decode, handy for testing a custom action before writing it back into the game. It covers Actions 0-181 and links out to the formula each action uses, so you can trace exactly how an action's numbers actually resolve.

{% hint style="danger" %}
Some action IDs are hardcoded (Quickenings, Concurrences, Summons, Steal, Revive, and more) and will not behave the same even if all their data is copied elsewhere. Swapping one action for another should generally be avoided.
{% endhint %}

{% hint style="info" %}
**Access the spreadsheet**

<a href="https://docs.google.com/spreadsheets/d/1nm3f5DvkKvkMlcr1oknpgJwnk7Ud3sgXPaHKTcXbJMM/edit" class="button primary" data-icon="external-link-alt">Open the Spreadsheet</a>
{% endhint %}

{% content-ref url="action-formulas-reference.md" %}
[action-formulas-reference.md](action-formulas-reference.md)
{% endcontent-ref %}
