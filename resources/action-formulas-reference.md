# Action Formulas Reference

**Action Formulas Reference** is a spreadsheet documenting all 108 damage and effect Formulas the game uses, and the individual Functions each formula calls internally.

**Credits:** Eochaid, Xeavin

### What can you do with this?

Every action in the game resolves through one of these Formulas: a named sequence of functions that decides what actually happens when a spell or attack lands. This sheet documents all of them and the functions they call, so you can see exactly how an action calculates its result, not just its raw Power and Accuracy numbers.

**Spreadsheet contents:**

- **Formulae:** one row per formula. Each gives the formula's ID, its name (Restore HP, Magick Damage, KO, and so on), a category, a plain-language summary, and a "Used By" column listing every action that runs through it. It then lays out the execution order in two stages: the on-cast functions that run when the action is first cast (safety checks, evade checks, and the like), and the on-hit functions that run once it connects (the damage or healing math, applying status effects). Each function in the chain carries its own ID and a short description of what it does. Because every action appears under some formula's "Used By" column, you can search for a spell by name to find the exact formula and function chain behind it.
- **Functions:** a flat reference list of every function used across the formulas, by ID, with its description. Use this when you already have a function ID or name from a formula chain and just want to look it up on its own.

For execution-order edge cases that the raw function chain does not make obvious (how a formula behaves on a combo hit, a counter, a reflected spell, and so on), The Insurgent's Forge documentation walks through concrete scenarios.

{% hint style="info" %}
**Access the spreadsheet**

<a href="https://docs.google.com/spreadsheets/d/1yyflms0sghclccDE5R3qb-NdiTFkiMimmhbuX5iYWUk/edit" class="button primary" target="_blank" data-icon="external-link-alt">Open the Spreadsheet</a>
{% endhint %}

{% content-ref url="battlepack-section-14-action-data.md" %}
[battlepack-section-14-action-data.md](battlepack-section-14-action-data.md)
{% endcontent-ref %}
