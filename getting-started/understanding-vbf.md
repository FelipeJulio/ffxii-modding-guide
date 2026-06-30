# Understanding the VBF Archive

Even though modern modding uses the [FF12 External File Loader](../tools/external-file-loader.md) to bypass injecting files _into_ the game's archive, your mod files must still perfectly replicate the game's internal folder structure for the loader to recognize them.

## The VBF Tree Structure

Here is a simplified summary of the `.vbf` folder tree as seen through the **[VBF Browser](../tools/vbf-browser.md)**. You can use this as a quick reference to know where specific assets are located.

```text
FFXII_TZA.vbf
├── gamedata
│   ├── ...
│   └── d3d11
│       └── artdata
│           ├── ...
│           └── chr
│               ├── weapon
│               └── ...
├── ps2data
│   ├── ...
│   ├── plan_master
│   ├── ...
│   ├── image
│   │   └── ff12
│   │       ├── us
│   │       │   ├── test_battle
│   │       │   │   └── us
│   │       │   │       ├── binaryfile
│   │       │   │       ├── ...
│   │       │   └── myoshiok
│   │       │       ├── us
│   │       │       │   ├── ...
│   │       │       │   ├── handbook
│   │       │       ├── ...
│   │       ├── ...
│   │       ├── common
│   ├── ...
├── jsondata
│   ├── ...
└── prefetchdata
```

## How the Structure Works

The organization might seem a little confusing at first, but it is something you get used to very quickly once you understand the core separation:

- **`gamedata`:** This is where the majority of the game's visual assets are located, such as 3D models and textures.
- **`ps2data`:** This is where the game's logic resides. However, it doesn't just contain logic; you will also find text files and other binary textures here.

### Practical Examples

To help you navigate, here are a few practical examples of where important files are located:

#### Weapons (Models & Textures)

`gamedata/d3d11/artdata/chr/weapon`
This is where you will find the 3D models and textures for all the weapons in the game.

#### Weapon Statistics & Game Sessions

`ps2data/image/ff12/us/test_battle/us/binaryfile/battle_pack.bin`
This path holds the binary files related to various game sessions. For example, inside the `battle_pack.bin` file, you will find `section_13.bin`, which contains the binary data for all weapon statistics (status, attributes, etc.).

#### Map Logic & NPCs

`ps2data/plan_master/us/plan_map`
This is where the `.ebp` (Environment Blueprint Pack) files are located. These are the logic files for the maps, which include NPC dialogue scripts, configuration for loading models into that specific map, and the overall logic/mechanics that give "life" to the map.

#### Enemy Logic

`ps2data/plan_master/in`
Here you will find the `.ard` (Area Resource Data) files. There is one `.ard` file for every map in the game, and they handle the logic for the enemies located in that specific map (such as their status and attributes).
