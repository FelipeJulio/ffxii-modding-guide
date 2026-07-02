# The Insurgent's Toolkit

**The Insurgent's Toolkit** is the ultimate, essential real-time memory editor and modding suite for _Final Fantasy XII: The Zodiac Age_.

If you are a modder, this tool is practically mandatory. It acts as a bridge between the game's live memory and your ideas. Through The Insurgent's Toolkit, you can modify the game in real-time, understand exactly how certain data structures are read from memory, and obtain static and dynamic addresses to use in your **FF12 Lua Loader** mods.

It also includes an export functionality, allowing you to edit files live in the game and export them directly to use as a mod.

**Credits:** Xeavin

---

### What does it do?

The Toolkit is massive and touches almost every system in the game. Here is a brief summary of what you can accomplish with it:

- **Live Data Editors:** View and modify critical game structures in real-time, including the **Battlepack** (gambits, equipment, actions, stats), **EBP** (map logic, treasures, traps), **ARD** (foe stats, AI per location), and **MRP** (UI menus).
- **Party & Character Control:** Manipulate your party on the fly. Add or remove members, recalculate stats and levels, freely add or remove any item, equipment, magick, technick, or other inventory content, and view extensive hidden data about any character in battle.
- **World Manipulation:** Free teleport anywhere, turn any location into a Trial Mode on demand (Custom Foe Respawn), banish nearby foes, summon a Chocobo, open any shop, open the save/load menu, cast any battle action on demand, or instantly complete the bestiary.
- **Game State Control:** Manipulate the RNG (PRNG), chain levels, magick fields, FOV, no-clip, and general post-processing, UI, or Game Settings (resolution, VSync, anti-aliasing, shadows, frame rate limit, and more).
- **Save Game Editing:** A complete, comprehensive save game editor that lets you alter absolutely anything in your save file.
- **Modder Resources:** Provides VM Call Target pointers, license node icon viewers, multipalette texture viewers, and clan primer handbook editors.

{% hint style="info" %}
**Newer than the public wiki**
The cheat table itself is ahead of The Insurgent's Toolkit's published wiki. Recent revisions add editors the wiki doesn't cover yet, exact behavior isn't documented anywhere yet, so treat these as advanced/experimental until the community wiki catches up:

- Traveler's Tips Requirements Editor
- Bestiary Requirements Editor
- Global Message Editor
- Behind Camera Editor
- Map Ref Editor
- Map Jump Group Flag Rom Editor
- Menu Section Plus Editor
- License Board Node Editor
- Special Action Processing Editor
- Action List Categories Editor
- File Viewer
- Battle Script Input Editor
- VM Call Target Executor
- VM Opcode Editor
- Forced Input Icons
{% endhint %}

{% hint style="warning" %}
The Toolkit is built for specific game versions only: Steam 1.0.4.0 and Microsoft Store 1.0.1.0. Other versions are not supported, and some editors won't work at all on the Microsoft Store version since that build doesn't support mods yet.
{% endhint %}

{% hint style="warning" %}
Every editor can only modify content that already exists in the game, it cannot add entirely new content. The game does contain a lot of reserved, unused data though, which is the usual workaround: repurpose a reserved entry instead of trying to create a new one.
{% endhint %}

{% hint style="info" %}
Requires [Cheat Engine v7.4+](https://github.com/cheat-engine/cheat-engine/releases) to run, since the Toolkit is a Cheat Engine table. If you close Cheat Engine without deactivating a running script first, that script won't reactivate properly next time, a game restart fixes it.
{% endhint %}

{% hint style="success" %}
**Download & Setup**
Because The Insurgent's Toolkit is incredibly powerful, it comes with its own extensive wiki. We highly recommend reading through it to understand how to properly set it up and utilize all of its features.

<a href="https://www.nexusmods.com/finalfantasy12/mods/160" class="button primary" target="_blank" data-icon="external-link-alt">Go to Official Mod Page</a>
{% endhint %}

