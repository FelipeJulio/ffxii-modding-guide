# Enemy & Area Data Map

**Enemy & Area Data Map** is the full enemy and unit configuration map across every ARD (area) file in the game.

**Credits:** Eochaid

### What can you do with this?

Every enemy, NPC, and other unit in the game is defined inside an ARD file: its stats, AI script links, model, animations, and loot table, all cross-referenced by ID. This spreadsheet decodes that entire structure across tabs that mirror The Insurgent's Toolkit's ARD Editor sections exactly: Units (the main tab, one row per enemy instance, linking everything else together), Classes (shared templates for detection range, elemental resistance, and movement behavior that many named units reuse), Default/Additive Stats (a unit's real stat is the default value plus the additive value, which lets reused enemy species share a base block while varying slightly per encounter), Models (the subset of models used within this specific area), and Special Animations (which combat animation a unit's AI script triggers for a given attack). It is split into two linked workbooks (this one and Enemy AI Scripts) because the data is too large for a single spreadsheet, Google Sheets has a 10 million cell limit.

{% hint style="warning" %}
The Insurgent's Toolkit only keeps one `.ard` file loaded in memory at a time, and most `.ard` files are shared by multiple locations, so editing one affects everywhere it's used.
{% endhint %}

{% hint style="info" %}
**Access the spreadsheet**

<a href="https://docs.google.com/spreadsheets/d/1OyKQkfZkSvw5NHJeHpaEso-7e3dWaSZYsH4ZQ5BGD2g/edit" class="button primary" target="_blank" data-icon="external-link-alt">Open the Spreadsheet</a>
{% endhint %}

{% content-ref url="enemy-ai-scripts.md" %}
[enemy-ai-scripts.md](enemy-ai-scripts.md)
{% endcontent-ref %}
