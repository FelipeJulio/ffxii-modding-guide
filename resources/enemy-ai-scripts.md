# Enemy AI Scripts

**Enemy AI Scripts** is the full decode of every enemy's battle AI script, the state-machine logic that decides what an enemy actually does in combat.

**Credits:** Eochaid

### What can you do with this?

Each unit's AI runs as a script made of groups and ordered entries: checks (like "target is within X meters" or "caster's HP is below 100%") paired with the action that fires when a check passes, plus the ability to jump between groups. This spreadsheet reconstructs that logic per enemy, so you can read exactly why an enemy behaves the way it does, and safely change it. It also documents Action Packages, weighted random-attack pools an AI script can trigger instead of a single fixed move. This is the largest spreadsheet in the collection, so when researching a specific enemy, search by name rather than reading it top to bottom.

{% hint style="danger" %}
The Insurgent's Toolkit warns that AI Scripts and Action Groups are heavily linked, editing one without the other can cause enemies to get stuck in an infinite loop or other broken behavior.
{% endhint %}

{% hint style="info" %}
**Access the spreadsheet**

<a href="https://docs.google.com/spreadsheets/d/1BEXZsbvK0Ey5Yl5WpI58Es4nEXNnI3PSd0_Asi5DE48/edit" class="button primary" target="_blank" data-icon="external-link-alt">Open the Spreadsheet</a>
{% endhint %}

{% content-ref url="enemy-and-area-data-map.md" %}
[enemy-and-area-data-map.md](enemy-and-area-data-map.md)
{% endcontent-ref %}
