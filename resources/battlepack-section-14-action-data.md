# Battlepack Section 14: Action Data

**Battlepack Section 14: Action Data** is a full decode of Section 14, the game data section that defines every action (Magick, Attack, Item, Technick) in the game.

**Credits:** Eochaid

### What can you do with this?

Every action's targeting rules, charge time, MP/Mist cost, damage formula link, elements, statuses, and dozens of AI/gambit behavior flags live in Section 14. This spreadsheet decodes it action by action, with a "binary calculator" tab you can paste new raw hex into to preview how it would decode, handy for testing a custom action before writing it back into the game. It covers Actions 0-181 and links out to the formula each action uses, so you can trace exactly how an action's numbers actually resolve.

{% hint style="danger" %}
Some action IDs are hardcoded (Quickenings 208-225, Concurrences 226-241, Summons 262-274, plus Shades of Black, Steal, Revive, Dismiss, and Spawn) and will not behave the same even if all their data is copied elsewhere. Swapping a Magick for another Magick is generally fine, but swapping across types (a Technick for an Item, for example) may not be, so avoid it unless you know the specific action is safe.

A few other things to keep in mind: avoid reusing reserve action IDs 147-484, since some are referenced by unknown internal functions (111-123 and anything after 497 are safer reserve ranges). Since party members and foes share the same action table, changing an action's effect can break enemy AI that depends on it, for example if Esuna stops removing Slow, an AI conditioned on "if I have Slow, cast Esuna" can loop forever. Reusing a Required Content ID across more than one action breaks inventory sort order, and gambit page/order changes require a game restart to take effect. Before repurposing an action ID, it also helps to know how many enemies actually use it, a high reference count means the change will ripple further than you might expect.
{% endhint %}

{% hint style="success" %}
The Toolkit's own live Actions list actually goes past 540 total slots, far beyond the 182 (Actions 0-181) this sheet documents. That gap is exactly the reserve range the warning above refers to: hundreds of slots exist in the engine with no confirmed name or effect yet.
{% endhint %}

{% hint style="info" %}
**Access the spreadsheet**

<a href="https://docs.google.com/spreadsheets/d/1nm3f5DvkKvkMlcr1oknpgJwnk7Ud3sgXPaHKTcXbJMM/edit" class="button primary" target="_blank" data-icon="external-link-alt">Open the Spreadsheet</a>
{% endhint %}

{% content-ref url="action-formulas-reference.md" %}
[action-formulas-reference.md](action-formulas-reference.md)
{% endcontent-ref %}
