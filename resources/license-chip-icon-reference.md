# License Chip Icon Reference

**License Chip Icon Reference** is a spreadsheet that maps out `license_chip.bin`, the game file controlling which icon shows up on each node of the License Board.

**Credits:** Eochaid

### What can you do with this?

Every node on the License Board shows a small icon, and `license_chip.bin` is the file that decides which one. This spreadsheet is the lookup table for it: one row per License Board entry (weapons, armor, magick categories, augments, gambits, technicks, and more), grouped under labeled headers such as Backgrounds and character-specific overlays.

For each entry, the sheet gives the raw values `license_chip.bin` stores:

- **Entry Identifier** and a text link,
- **Texture Group, Section, and Entry links** (which texture, and which part of it, to draw),
- **Animation**,
- **Clut Link** (the color palette), and
- **X and Y position**.

To change a node's icon, find the entry by name (Excalibur, Ribbon, Zodiac Spear) and read across its row for the values to write. A few rows are section separators rather than real entries (labeled things like "First Overlay" or "CLEAR IT"), so expect a handful that do not map to an actual icon.

{% hint style="info" %}
**Also in The Insurgent's Toolkit**
This sheet accompanies the Toolkit's License Node Icons Editor, which lets you view and change these same values live in memory.
{% endhint %}

{% hint style="info" %}
**Access the spreadsheet**

<a href="https://docs.google.com/spreadsheets/d/1TKyxjciZ-wDKQLBdx5gsGwnEM96HmsDw29qUDpwdl14/edit" class="button primary" target="_blank" data-icon="external-link-alt">Open the Spreadsheet</a>
{% endhint %}
