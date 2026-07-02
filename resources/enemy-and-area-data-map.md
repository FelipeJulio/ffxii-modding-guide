# Enemy & Area Data Map

**Enemy & Area Data Map** is the full enemy and unit configuration map across every ARD (area) file in the game.

**Credits:** Eochaid

### What can you do with this?

Every enemy, NPC, and other unit in the game is defined inside an ARD (area) file. This spreadsheet decodes that entire structure, area by area, with everything cross-linked by ID. Its tabs are numbered to match the sections of an `.ard` file, the same ones you see in The Insurgent's Toolkit's ARD Editor.

**Spreadsheet contents:**

- **Units (section 4):** the main tab, one row per enemy or unit instance in an area. It ties everything else together: links to the unit's class and stat blocks, its four AI script slots, its model and appearance (weapon, size, and color or model variation), its full drop/steal/poach/monograph/canopic loot table, and flags such as Is Hunt, Is Boss, and Has Shield.
- **Classes (section 2):** shared templates that many units reuse, covering detection range and angle, elemental affinities (absorb, immune, half, weak), weight, max combo hits, and movement behaviour (flying, floating, teleport attacks).
- **Default and Additive Stats (sections 7 and 8):** a unit's real stat is its default value plus an additive value. Splitting them lets the same enemy species, reused across zones, share one base stat block while varying slightly per encounter. Covers HP, MP, the primary attributes, attack and defense, experience, license points, gil, and more.
- **Models (section 1):** the specific models used within this area, a narrower, per-area view than the global Model Reference.
- **Special Animations (section 9):** which combat animation a unit's AI script plays for a given attack.

Two more tabs are working aids rather than game data: a Data tab of shared lookup lists, and a Data-Check tab used to validate the sheet against a second copy. (Sections 5 and 6 exist in the file format but are unused, which is why the numbering skips them, and section 3, the AI scripts, is large enough to live in its own paired sheet.)

Note: in the source spreadsheet, colored cells mark cross-references between tabs, which do not survive a CSV export. Use the link and ID columns to follow those references instead. The whole thing is split across two linked workbooks (this one and Enemy AI Scripts) because it is too large for a single Google Sheet.

{% hint style="warning" %}
The Insurgent's Toolkit keeps only one `.ard` file loaded in memory at a time, and most `.ard` files are shared by several locations, so editing one affects everywhere it is used.
{% endhint %}

{% hint style="info" %}
**Access the spreadsheet**

<a href="https://docs.google.com/spreadsheets/d/1OyKQkfZkSvw5NHJeHpaEso-7e3dWaSZYsH4ZQ5BGD2g/edit" class="button primary" target="_blank" data-icon="external-link-alt">Open the Spreadsheet</a>
{% endhint %}

{% content-ref url="enemy-ai-scripts.md" %}
[enemy-ai-scripts.md](enemy-ai-scripts.md)
{% endcontent-ref %}
