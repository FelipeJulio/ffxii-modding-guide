# Enemy Action Groups

**Enemy Action Groups** is a spreadsheet documenting the weighted random-attack pools an enemy's AI can trigger. It covers Section 10 of the game data.

**Credits:** Eochaid

### What can you do with this?

An enemy's AI does not have to use a single fixed action. Instead it can point to an Action Group: a pool of several actions, each with its own chance to fire. Package 0, for example, is 30% "Ram" and 70% a basic "Attack." This is where the variety in enemy attack patterns comes from, and this sheet is the reference for it.

**Spreadsheet contents:**

- **Section 10:** one row per Action Group. Each gives the group's ID, a second internal identifier, columns for which enemies, AI scripts, areas, and zones use it, and then up to twelve action slots, each with an action ID, its name, and its percentage chance. The chances in a group add up to 100.
- **Enemy Action Counts:** a usage summary, one row per action. It shows how many area files reference the action at all (across any enemy's AI or action group) and how many Action Groups specifically include it. Use this to gauge how widely an action is used before repurposing it: an action referenced by many areas will have far-reaching effects if you change it.

{% hint style="danger" %}
Action Groups are tightly linked to the AI Scripts that call them. Editing a group without updating the matching AI Script can leave enemies stuck in a loop, frozen in a T-pose, or otherwise broken. Always edit the two together.
{% endhint %}

{% hint style="info" %}
**Also in The Insurgent's Toolkit**
The same data can be edited live under Battlepack Editor > 10 : Action Groups.
{% endhint %}

{% hint style="info" %}
**Access the spreadsheet**

<a href="https://docs.google.com/spreadsheets/d/1FeMWCdnrlqL-ZCuUz0xCOPxbY4lNh08TVknjQCmn-dw" class="button primary" target="_blank" data-icon="external-link-alt">Open the Spreadsheet</a>
{% endhint %}

{% content-ref url="enemy-ai-scripts.md" %}
[enemy-ai-scripts.md](enemy-ai-scripts.md)
{% endcontent-ref %}
