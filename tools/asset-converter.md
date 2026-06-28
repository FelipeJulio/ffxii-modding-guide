# FFXII Asset Converter

The **FFXII Asset Converter** is a tool for anyone looking to modify the game's visual assets, specifically 3D models and advanced textures.

### What does it do?

Similar to other decompilers, this tool converts the game's original complex visual assets into standard, easy-to-use intermediary formats, and then packs them back when you're done.

- **Models:** It converts `.dae.phyre` model files into standard `.fbx` files. You can open these in Blender or Maya to completely remodel characters, weapons, or maps.
- **Textures:** It automatically extracts and converts related `.dds.phyre` textures into `.png` files, which are much easier to work with.

When you're finished, the tool packs your `.fbx` and `.png` files back into the original formats so the game can read them.

{% hint style="info" %}
**Key Features:**

- Supports HD textures and complete mesh remodeling.
- Comes with both a Command Line Interface (CLI) and a built-in GUI.
- The GUI includes an **Asset Previewer**, allowing you to see 3D models and textures directly before extracting them.
{% endhint %}

{% hint style="warning" %}
**Important Requirement** You will need the **MSVC Runtime Libraries** installed on your PC to run the GUI version of this tool.
{% endhint %}

{% hint style="success" %}
**Download & Documentation** For more details on advanced topics like bone assignments, scene-graphs, and morphing animations, check out the full documentation on the mod page.

<a href="https://www.nexusmods.com/finalfantasy12/mods/288" class="button primary" data-icon="external-link-alt">Go to Official Mod Page</a>
{% endhint %}
