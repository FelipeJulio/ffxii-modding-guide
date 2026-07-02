# Enemy AI Scripts

**Enemy AI Scripts** is the full decode of every enemy's battle AI script, the state-machine logic that decides what an enemy actually does in combat.

**Credits:** Eochaid

### What can you do with this?

Each enemy in the game is driven by an AI script: a small state machine of checks and actions that decides, tick by tick, what it does in battle. This spreadsheet is the full decode of every one of them.

**Spreadsheet contents:**

- **AI Scripts:** the main decode, and by far the largest sheet in the whole collection (tens of thousands of rows). Every enemy has one or more scripts; each script is made of groups, and each group holds ordered entries that run in sequence. A row is a single instruction: the action it performs ("jump to AI Group 2 with X% chance", "idle for X seconds", "remove a given augment"), its numeric parameter, and up to three conditional cases that gate whether it fires ("caster is within X meters", "current HP below 100%"). Reading one enemy's script top to bottom reconstructs its actual behaviour: what it checks, how it responds, and how it loops between groups. Because the tab is so large, filter by enemy name or area rather than scrolling.
- **Action Packages:** weighted random-attack pools a script can trigger instead of always using one fixed action (for example, 30% "Ram" and 70% a basic "Attack"). This is where variety in enemy attacks comes from. The same data also has its own dedicated sheet, Enemy Action Groups, which adds usage counts.
- **Data:** the lookup tables the other two tabs reference: action IDs to names, target-condition IDs to descriptions (Highest Attack Power, Furthest, and so on), and target-type IDs (Foe, Ally, Self, Same Group, Attacker).

{% hint style="danger" %}
AI Scripts and Action Groups are heavily linked. Editing one without the other can leave enemies stuck in an infinite loop or otherwise broken, so change them together.
{% endhint %}

{% hint style="info" %}
**Also in The Insurgent's Toolkit**
This is section 3 of an `.ard` file, edited under ARD Editor > 3 : AI Scripts. The live structure is hard to edit through Cheat Engine because entries cross-reference each other, so reading a script here first is the practical way to understand it before changing it.
{% endhint %}

{% hint style="info" %}
**Access the spreadsheet**

<a href="https://docs.google.com/spreadsheets/d/1BEXZsbvK0Ey5Yl5WpI58Es4nEXNnI3PSd0_Asi5DE48/edit" class="button primary" target="_blank" data-icon="external-link-alt">Open the Spreadsheet</a>
{% endhint %}

{% content-ref url="enemy-and-area-data-map.md" %}
[enemy-and-area-data-map.md](enemy-and-area-data-map.md)
{% endcontent-ref %}
