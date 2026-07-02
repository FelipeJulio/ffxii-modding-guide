# XII Font Editor

The **XII Font Editor** is a web-based utility for editing and creating custom fonts for Final Fantasy XII.

**Credits:** FehDead

{% hint style="danger" %}
**Experimental Tool** Please note that this tool is currently **experimental**. Some features might not work precisely as expected, and bugs may occur. Always keep backups of your original font files before making changes.
{% endhint %}

### What does it do?

Fonts in FFXII are handled through specialized atlas and kerning files. This editor allows you to unpack, edit, and compile these specific font formats:

- **Atlas Files (`.dat` / `.txt`):** The atlas defines the visual layout and metrics of every character. The editor lets you convert the compiled binary `.dat` into a readable `.txt` format for adjustments, and recompile it back to `.dat` for the game engine.
- **Kerning Files (`.ker` / `.txt`):** Handles the spacing between individual character pairs to ensure your custom font is visually balanced.
- **Visual Previews (`.png`):** The editor can export a high-resolution snapshot of the glyph map to replace the original `.dds` texture in the game files.
- **Custom Fonts:** You can upload your own `.ttf` or `.otf` fonts to completely replace the game's default typography.
- **Visual Overlay:** Allows you to load a `.png` of the original `.dds` texture as an overlay beneath your canvas, ensuring your custom glyphs perfectly align with the game's expectations to avoid "letterbox" issues.
- **Advanced Typography:** Fine-tune spacing, kerning, strokes, shadows, and colors (with HEX/RGBA support).

{% hint style="info" %}
**Web Tool Link** You can access the editor and its full documentation directly in your browser.

<a href="https://ff12-font-editor.vercel.app/" class="button primary" data-icon="external-link-alt">Open XII Font Editor</a>
{% endhint %}
