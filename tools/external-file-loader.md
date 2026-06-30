# FF12 External File Loader

The **FF12 External File Loader** is the foundational mod that makes modern FFXII modding possible. It is a **mandatory requirement** for virtually all mods.

### What does it do?

By default, all game assets are packed inside the massive `FFXII_TZA.vbf` archive. The FF12 External File Loader intercepts the game at runtime and tricks it into reading loose files from a folder on your disk instead: without ever touching the original `.vbf` file.

- Your original game files remain **100% untouched**.
- Installing or removing a mod is as simple as adding or deleting a folder.
- Restoring the vanilla game takes seconds.
- Supports loading individual binary sections via the `.dir` folder system (see [Modding Folder Structure](../getting-started/modding-folder-structure.md)).

{% hint style="warning" %}
**Compatibility Note**
FF12 External File Loader version 1.3.15+ requires **FF12 Lua Loader 1.6.2+**. Older versions of either tool are not fully compatible with each other.
{% endhint %}

### How it works

The FF12 External File Loader is actually two components bundled together:

- **FF12 Module Loader**: loads native `.dll` modules when the game starts, enabling features like the FF12 External File Loader itself.
- **FF12 External File Loader**: the module that intercepts file reads and redirects them to your local mod folder.

Mods deployed via Vortex or MO2 are placed at `mods/deploy/ff12data/`, which mirrors the internal VBF structure. The FF12 External File Loader checks this folder first; if a file isn't found there, it falls back to the original `.vbf`.

{% hint style="info" %}
**Download & Documentation**

<a href="https://www.nexusmods.com/finalfantasy12/mods/2" class="button primary" data-icon="external-link-alt">Go to Official Mod Page</a>
{% endhint %}

