# Modding Folder Structure

When building mods for Final Fantasy XII, understanding how your files are loaded into the game is essential. There are two primary loaders you'll interact with: the **[External File Loader](../tools/external-file-loader.md)** for vanilla asset replacement, and the **Lua Loader** for scripts.

In this section, we will break down both folder structures and explain how to use them effectively.

---

## 1. External File Loader Structure

The External File Loader hooks into the game engine and allows you to load loose files directly from your disk, overriding the assets stored inside the game's massive `.vbf` archive.

When a mod is deployed (e.g., via Mod Organizer 2), its files are placed into this core directory:
`mods/deploy/ff12data/`

This folder acts as a **direct mirror of the VBF**. If a file exists in the VBF at `ps2data/image/ff12.bin`, you must place your modified file at `mods/deploy/ff12data/ps2data/image/ff12.bin` for the EFL to recognize it.

### Layered Loading (The `.dir` Feature)

The most powerful feature of the EFL is its ability to load **individual binary sections**.

Many files in FFXII, such as `battle_pack.bin` or map `.ebp` files, are actually archives containing dozens of smaller binary sections. **It is considered a bad practice to repack and overwrite an entire pack file**, as this will immediately cause conflicts with any other mod trying to edit a different section of the same pack.

Instead, the EFL allows you to turn a file name into a directory by appending `.dir` to it. The EFL will then inject only the loose sections found inside into the original game pack at runtime.

**Example 1: Single Level Depth**
If you want to edit `section_013.bin` inside `battle_pack.bin`, you create a folder named `battle_pack.bin.dir` and place your edited section inside:

```text
mods/
└── deploy/
    └── ff12data/
        └── ps2data/
            └── image/
                └── ff12/
                    └── us/
                        └── test_battle/
                            └── us/
                                └── binaryfile/
                                    └── battle_pack.bin.dir/
                                        └── section_013.bin
```

**Example 2: Multi-Level Depth**
Binary files in FFXII can be nested. For example, `section_061.bin` (which is inside `battle_pack.bin`) contains its own sub-sections. If you want to modify `section_000.bin` (which handles ability names) located inside `section_061.bin`, you simply chain the `.dir` folders:

```text
mods/
└── deploy/
    └── ff12data/
        └── ps2data/
            └── image/
                └── ff12/
                    └── us/
                        └── test_battle/
                            └── us/
                                └── binaryfile/
                                    └── battle_pack.bin.dir/
                                        └── section_061.bin.dir/
                                            └── section_000.bin
```

This layered loading architecture ensures that your mod is highly compatible with other mods, as you are only replacing the exact byte sections you modified rather than the entire archive.

---

## 2. Lua Loader Structure

Unlike the EFL which mirrors the original VBF file structure, Lua mods do not replace game files. Instead, they run entirely from memory.

All scripts injected via the Lua Loader must reside in the `x64/scripts` directory of your mod folder.

When building a Lua Mod, it's highly recommended to adopt a modular architecture to keep your code organized. A standard, well-structured Lua Mod looks like this:

```text
mods/
└── MyAwesomeMod/
    └── x64/
        └── scripts/
            ├── MyAwesomeMod.lua
            ├── MyAwesomeMod/
            │   ├── helpers.lua
            │   └── main_logic.lua
            └── config/
                └── MyAwesomeModConfig/
                    ├── us.lua
                    ├── es.lua
                    └── fr.lua
```

### Breaking Down the Structure

- **Main Entry File (`MyAwesomeMod.lua`):** This is the root file that the Lua Loader will find and execute. It should ideally be lightweight, serving only to load configuration files and bootstrap the modules located in your subfolder.
- **Component Directory (`MyAwesomeMod/`):** To avoid cluttering the `scripts` root folder and causing conflicts with other mods, you should create a folder named exactly after your mod. Inside it, you can place all your secondary modules, hooks, classes, and helper functions (e.g., `helpers.lua`).
- **Configuration Directory (`config/MyAwesomeModConfig/`):** If your mod requires user-adjustable settings or multi-language support (like localizing strings for US, ES, FR), you should place these files in a dedicated `config` folder. Using a suffix like `Config` for the subfolder ensures it is clearly separated from your core logic.

By adhering to this structure, your code remains modular, easy to maintain, and extremely compatible with the FFXII Lua Loader ecosystem.
