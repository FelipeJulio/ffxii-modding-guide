# DDS Phyre Tool

The **DDS Phyre Tool** is a simple but incredibly useful command-line converter specifically built for the PhyreEngine's texture format.

**Credits:** ffgriever

### What does it do?

Final Fantasy XII stores many of its textures in a `.dds.phyre` format. Standard image editors (like Photoshop or GIMP) cannot open `.phyre` files natively.

This tool solves that by allowing you to convert back and forth between them:

- **Unpack:** Converts a `.dds.phyre` file into a standard `.dds` texture file so you can edit it.
- **Pack:** Converts your edited `.dds` texture back into a `.dds.phyre` file so the game can read it.

{% hint style="success" %}
**Advanced Features** The tool supports importing resized textures (higher or lower resolutions) and changing the texture compression format (e.g., from DXT5 to ARGB8 for maximum quality).
{% endhint %}

{% hint style="warning" %}
**Important Rule** When packing a `.dds` file back into `.phyre`, the original `.phyre` file **must exist** in the same directory. The tool doesn't recreate all headers from scratch; it simply modifies the data of the existing file.
{% endhint %}

{% hint style="info" %}
**Download & Source** You can download the tool from Nexus Mods.

<a href="https://www.nexusmods.com/finalfantasy12/mods/289" class="button primary" data-icon="external-link-alt">Go to Official Mod Page</a>
{% endhint %}
