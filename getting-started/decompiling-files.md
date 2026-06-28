# Decompiling Files

Once you have extracted the original `.vbf` files to your computer, you will notice that they are mostly raw binary files that you cannot simply open in Notepad to edit.

To modify the logic, stats, or text inside these files, you need to use **decompilation tools** to translate them into human-readable formats (like `.json` or `.txt`). After editing the readable format, you then compile it back into the binary format so the game can read it.

There are several tools created by the community specifically for decompiling different types of game files.

---

### The Insurgent's Workshop

This is the primary tool used to unpack and pack the game's general binary files into readable JSON or text formats, making them incredibly easy to modify.

{% content-ref url="../tools/insurgents-workshop.md" %}
[Learn more about The Insurgent's Workshop](../tools/insurgents-workshop.md)
{% endcontent-ref %}
---

### FF12 VM Script Decompiler and Compiler

This tool specializes in decompiling the game's map and event scripts (`.ebp` files) into a C-like programming language. It is essential for editing map logic, adding NPCs, and changing dialogues.

{% content-ref url="../tools/script-decompiler.md" %}
[Learn more about the VM Script Decompiler](../tools/script-decompiler.md)
{% endcontent-ref %}
---

### DDS Phyre Tool

A converter for texture files. It unpacks the game's `.dds.phyre` textures into standard `.dds` formats for image editing, and packs them back for the game to read.

{% content-ref url="../tools/dds-phyre-tool.md" %}
[Learn more about DDS Phyre Tool](../tools/dds-phyre-tool.md)
{% endcontent-ref %}
---

### FFXII Asset Converter

A powerful tool designed to convert 3D models (`.dae.phyre`) and textures into common formats like `.fbx` and `.png`. It includes a built-in 3D previewer and is essential for editing character meshes, weapons, and maps.

{% content-ref url="../tools/asset-converter.md" %}
[Learn more about Asset Converter](../tools/asset-converter.md)
{% endcontent-ref %}
---

### XII Font Editor

An experimental web-based tool for editing the game's fonts. It handles atlas (`.dat`) and kerning (`.ker`) files, allowing you to import your own `.ttf` or `.otf` custom fonts.

{% content-ref url="../tools/font-editor.md" %}
[Learn more about XII Font Editor](../tools/font-editor.md)
{% endcontent-ref %}
---
