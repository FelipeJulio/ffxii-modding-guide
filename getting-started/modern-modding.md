# The Modern Modding Scenario

Before installing any tools, it is important to understand how Final Fantasy XII modding works today, and why it is different from the past.

## The Old Way: DrakLab and the `.vbf` Archive

By default, FFXII stores all of its 30GB+ of game files inside a single encrypted archive file named `FFXII_TZA.vbf`.

In the early days of modding, tools like the **DrakLab Mod Loader** were used to inject modified files directly back into this massive `.vbf` archive.

{% hint style="danger" %}
**Do not use the DrakLab Mod Loader.** It is completely deprecated. Injecting mods directly into the `.vbf` file is slow, prone to corrupting your game installation, and makes it difficult to use multiple mods at the same time without conflicts.
{% endhint %}

## The New Way: FF12 External File Loader

To solve these problems, the community moved away from modifying the `.vbf` archive entirely. This was made possible by the **[External File Loader](../tools/external-file-loader.md)**.

Instead of injecting files into the archive, the FF12 External File Loader intercepts the game as it runs. It creates a local layer of files and tricks the game into reading your "unpacked" mod files directly from a normal folder on your computer.

If the FF12 External File Loader doesn't find a modded file, it just loads the original one from the `.vbf`. This means your original game files remain 100% untouched, and installing or removing a mod is as simple as deleting a folder.

## The FF12 Lua Loader

The flexibility provided by the FF12 External File Loader paved the way for another important development: the **[FF12 Lua Loader](../tools/lua-loader.md)**.

While the FF12 External File Loader allows you to replace files (like 3D models or textures), the FF12 Lua Loader allows you to write custom Lua scripts to interact with the game's code in real-time. You can manipulate memory, call in-game functions, and change executable behavior without ever having to hard-patch the `.exe` file.

{% hint style="info" %}
**Are these required?**
Yes. The **FF12 External File Loader** is mandatory for all modern mods. The **FF12 Lua Loader** is necessary if you plan to create Lua mods, and is highly recommended regardless, as many modern mods rely on it to function.
{% endhint %}
