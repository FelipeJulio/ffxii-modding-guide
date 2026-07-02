# License Chip Icon Reference

**License Chip Icon Reference** is a spreadsheet that maps out `license_chip.bin`, the game file controlling which icon shows up on each node of the License Board.

**Credits:** Eochaid

### What can you do with this?

If you are using The Insurgent's Toolkit to give a custom license node its own icon, this spreadsheet is your lookup table. It lists every License Board entry (weapons, armor, magick categories, augments, gambits, technicks, and more), organized under labeled group headers like Backgrounds and character-specific overlays, alongside the exact values `license_chip.bin` stores for it: Entry Identifier, Texture Group/Section Link, Animation, color palette (Clut), Texture Entry Link, and X/Y position. Instead of guessing which values control which icon, you find the entry you want to change by name (Excalibur, Ribbon, Zodiac Spear) and copy its row's values straight into the Toolkit.

The Insurgent's Toolkit's own License Node Icons Editor page is only a one-line description of the feature, it doesn't explain what any of these values mean. This spreadsheet is the actual documentation for that editor, not a supplement to it. A few rows (labeled things like "First Overlay" or "CLEAR IT") are section separators rather than real license entries, so don't be surprised if a handful of rows don't map to an actual icon.

{% hint style="info" %}
**Access the spreadsheet**
Built to accompany The Insurgent's Toolkit's License Node Icons Editor.

<a href="https://docs.google.com/spreadsheets/d/1TKyxjciZ-wDKQLBdx5gsGwnEM96HmsDw29qUDpwdl14/edit" class="button primary" target="_blank" data-icon="external-link-alt">Open the Spreadsheet</a>
{% endhint %}
