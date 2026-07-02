# Enemy Action Groups

**Enemy Action Groups** is a spreadsheet documenting weighted random-attack pools an enemy's AI can trigger.

**Credits:** Eochaid

### What can you do with this?

Instead of always using one fixed action, an enemy AI entry can point to an Action Group, a pool of several actions that each have their own chance to fire (for example, 30% chance of a special attack, 70% chance of a basic Attack). This is where random enemy attack variety comes from. The sheet also tracks how many areas and AI scripts reference each action overall, useful for judging how far-reaching a change to a given action would be before you make it.

{% hint style="danger" %}
The Insurgent's Toolkit warns that Action Groups should only be edited together with the matching AI Scripts, changing one without the other can cause enemies to get stuck in a loop or behave unpredictably.
{% endhint %}

{% hint style="info" %}
**Access the spreadsheet**

<a href="https://docs.google.com/spreadsheets/d/1FeMWCdnrlqL-ZCuUz0xCOPxbY4lNh08TVknjQCmn-dw" class="button primary" target="_blank" data-icon="external-link-alt">Open the Spreadsheet</a>
{% endhint %}

{% content-ref url="enemy-ai-scripts.md" %}
[enemy-ai-scripts.md](enemy-ai-scripts.md)
{% endcontent-ref %}
