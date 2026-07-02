# UI Settings Documentation

**UI Settings Documentation** is a spreadsheet documenting `uisize.json`, the game file controlling UI element sizing and positioning. Researched using The Insurgent's Toolkit.

**Credits:** Kule, Neonsquare

### What can you do with this?

`uisize.json` is the game file that controls the size and position of interface elements: cursor positions, message box padding, battle menu spacing, license board info boxes, and more. Every value is a raw pixel or offset number with a cryptic internal name like `mCursorRightX`, which makes editing it blind almost impossible. This sheet is the decoder: it lists all of the roughly 230 settings and explains, in plain language, what each one visually controls.

For each setting you get:

- the **UI Section** it belongs to (Font, Pause Screen, Battle Menu, Hand Cursor, License Board, Message Box, and so on),
- the exact **internal parameter name**,
- a **description** of what it visually changes,
- the **vanilla default value**, and
- **notes** on quirks, for example that some values behave erratically outside the 0 to 127 range, or update only when you change zones.

The rows are ordered to match The Insurgent's Toolkit's UI Settings editor, so you can work through both side by side.

Two things to know before editing: a change only shows once the game redraws that element (you may need to trigger it, for example take damage to redraw an HP bar, or reopen a menu), and a handful of settings are dead and ignored by the game entirely.

{% hint style="info" %}
**Also in The Insurgent's Toolkit**
The Toolkit's UI Settings editor reads and writes these same values live. To ship a permanent change, extract `uisize.json` with the VBF Browser (under `jsondata/uisize`), edit the fields, then package it as a mod.
{% endhint %}

{% hint style="info" %}
**Access the spreadsheet**

<a href="https://docs.google.com/spreadsheets/d/1vIi0By-pGLldUIJ-CplHQWGyo8eYqUuxBYPlJoDrlBY/edit" class="button primary" target="_blank" data-icon="external-link-alt">Open the Spreadsheet</a>
{% endhint %}

{% content-ref url="mrp-ui-layout-documentation.md" %}
[mrp-ui-layout-documentation.md](mrp-ui-layout-documentation.md)
{% endcontent-ref %}
