# MRP (UI Layout) Documentation

**MRP (UI Layout) Documentation** is a spreadsheet documenting the game's MRP files, the binary format behind menu and HUD layout. Researched using The Insurgent's Toolkit.

**Credits:** Kule, Neonsquare

### What can you do with this?

An MRP file describes the layout of one part of the game's interface: where each element sits, how big it is, and which texture it uses. Inside a file, elements are organised as a hierarchy of Groups, and each Group holds Entries. Every Entry carries a position (X and Y), a size (Width and Height), a type code, and, for textured elements, a texture reference plus its own position, scale, and color tint (Red, Green, Blue, Alpha). This spreadsheet maps out that hierarchy so you can find the exact Group and Entry behind a given on-screen element instead of guessing.

**Spreadsheet contents:** two tabs, matching the game's two MRP sources.

- **MRP Pack:** the Battle and Field UI, bundled as 23 `.mrp` files that are always loaded in memory. This is where the HUD lives: target info bars, quickening timers, HP and MP digit graphics, and similar in-battle elements. Rows are organised by Section.
- **MRP Menu:** 8 `.mrp` files loaded only when needed and overwritten once they are no longer on screen, covering menu screens such as the logo, game over, and loading. Rows are organised by File.

One note about the live sheet: purple cells mark values that are not fully confirmed, and grey cells mark data that is unused or cannot be changed. That color coding does not survive a plain export, so keep it in mind when reading the source spreadsheet.

{% hint style="info" %}
**Also in The Insurgent's Toolkit**
This is the reference behind the Toolkit's MRP Editor, which reads and writes these same Groups and Entries live. Because MRP Menu files are unloaded once they leave the screen, a change to one must be exported before that happens, or it is lost. Exported files then load through the FF12 External File Loader.
{% endhint %}

{% hint style="info" %}
**Access the spreadsheet**

<a href="https://docs.google.com/spreadsheets/d/1Nojt7MhWiGa97OhUFpZIObFiTSZLmZyTJ6NIZGXroKI/edit" class="button primary" target="_blank" data-icon="external-link-alt">Open the Spreadsheet</a>
{% endhint %}

{% content-ref url="ui-settings-documentation.md" %}
[ui-settings-documentation.md](ui-settings-documentation.md)
{% endcontent-ref %}
