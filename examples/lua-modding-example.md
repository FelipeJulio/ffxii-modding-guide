# Creating a Map Announcer Mod with the FF12 Lua Loader

In this guide, we will build a Lua mod from scratch, improving it step by step. By the end, the mod will display an in-game popup with the name of the current location every time the player changes areas in Rabanastre.

Before starting, make sure you have the **[FF12 External File Loader](../tools/external-file-loader.md)** and the **[FF12 Lua Loader](../tools/lua-loader.md)** installed. If not, check the [Installing Mods](../getting-started/installing-mods.md) guide first.

---

## Step 1: Hooking Into the Game

Create the file `x64/scripts/MapAnnouncer.lua` inside your game directory with the following content:

```lua
event.registerEventAsync("onMapJump", function(locationId)
    print("Jumped to location ID: " .. tostring(locationId))
end)
```

`onMapJump` fires every time the player enters a new area. The FF12 Lua Loader automatically passes the `locationId` as an argument.

`print` writes to the `hook.log` file located at `x64/hook.log` in your game directory. This is one of the most essential tools while developing a Lua mod: use it constantly to confirm your code is running and to inspect values.

{% hint style="warning" %}
**Remove all `print` calls before releasing your mod.** Debug output left in production is considered bad practice.
{% endhint %}

**Testing:** Launch the game, go to Rabanastre, and walk between areas. Open `x64/hook.log` in a text editor: you will see a new line appear for each map transition showing the location ID.

---

## Step 2: Showing an In-Game Message

Checking the log file works, but it is not very practical. The FF12 Lua Loader provides `message.print`, which displays a popup in the top-left corner of the screen directly while playing.

Update `MapAnnouncer.lua`:

```lua
event.registerEventAsync("onMapJump", function(locationId)
    event.executeAfterMs(2000, function()
        message.print(message.convert("Location ID: " .. tostring(locationId)))
    end)
end)
```

`message.print` displays a popup on screen. It expects text in the game's own format, so you must always pass the string through `message.convert` first. By default the message stays visible for 2 seconds.

`event.executeAfterMs(2000, ...)` adds a small delay before displaying the message. Without it, the popup may fire before the game finishes the map transition and fail to appear.

**Testing:** Travel between areas in Rabanastre. You should now see the location ID appear on screen each time you enter a new area.

---

## Step 3: Creating an External Module

Raw IDs are not very readable. Let's create a **module**, a separate file that maps IDs to human-readable names, and load it into our script.

Create `x64/scripts/MapAnnouncer/locations.lua`:

```lua
return {
    [289] = "North End",
    [290] = "Muthru Bazaar",
    [291] = "East End",
    [292] = "Southern Plaza",
    [295] = "Amal's Weaponry",
    [296] = "Panamis's Protectives",
    [297] = "Migelo's Sundries",
    [298] = "Yugri's Magicks",
    [299] = "Batahn's Technicks",
    [300] = "Yamoora's Gambits",
    [301] = "Samalzalam Manor",
    [302] = "The Clan Hall",
    [304] = "The Sandsea",
    [305] = "Eastgate",
    [306] = "Southgate",
    [307] = "Westgate",
    [788] = "Aerodrome",
}
```

This module is a plain Lua file that returns a table. The key is the location ID and the value is its name.

{% hint style="info" %}
**Loading external files**
To pull in a `.lua` file from disk, we use `loadfile`, giving each one its own sandboxed environment. This is the standard way to load modules and config in FFXII mods.
{% endhint %}

Now update `MapAnnouncer.lua` to load the module and use it:

```lua
local function loadFile(path)
    local chunk = loadfile(path, "t", setmetatable({}, { __index = _G }))
    if not chunk then return nil end
    local ok, result = pcall(chunk)
    return ok and result or nil
end

local locations = loadFile("scripts/MapAnnouncer/locations.lua")

event.registerEventAsync("onMapJump", function(locationId)
    local name = locations and locations[locationId]
    if not name then return end
    event.executeAfterMs(2000, function()
        message.print(message.convert("Entering: " .. name))
    end)
end)
```

Note that `loadfile` paths are relative to `{game}/x64/`.

The popup only appears for locations listed in `locations.lua`. If a location ID is not in the table, nothing happens.

**Testing:** Travel between the areas of Rabanastre. The popup now shows the location name: _"Entering: Muthru Bazaar"_, _"Entering: The Clan Hall"_, and so on.

---

## Step 4: Adding a Config

A config file lets users customize the mod without touching your code. We will use it to let the user choose which locations trigger the popup.

Create `x64/scripts/config/MapAnnouncerConfig/settings.lua`:

```lua
local enabledLocations = {
    [289] = true,   -- North End
    [290] = true,   -- Muthru Bazaar
    [291] = true,   -- East End
    [292] = true,   -- Southern Plaza
    [295] = false,  -- Amal's Weaponry
    [296] = false,  -- Panamis's Protectives
    [297] = false,  -- Migelo's Sundries
    [298] = false,  -- Yugri's Magicks
    [299] = false,  -- Batahn's Technicks
    [300] = false,  -- Yamoora's Gambits
    [301] = false,  -- Samalzalam Manor
    [302] = true,   -- The Clan Hall
    [304] = true,   -- The Sandsea
    [305] = true,   -- Eastgate
    [306] = true,   -- Southgate
    [307] = true,   -- Westgate
    [788] = true,   -- Aerodrome
}

return enabledLocations
```

The config is just another module: a file that returns a table. Now update `MapAnnouncer.lua` to load it and check it before showing the popup:

```lua
local function loadFile(path)
    local chunk = loadfile(path, "t", setmetatable({}, { __index = _G }))
    if not chunk then return nil end
    local ok, result = pcall(chunk)
    return ok and result or nil
end

local locations = loadFile("scripts/MapAnnouncer/locations.lua")
local enabledLocations = loadFile("scripts/config/MapAnnouncerConfig/settings.lua") or {}

event.registerEventAsync("onMapJump", function(locationId)
    if not enabledLocations[locationId] then return end
    local name = locations and locations[locationId]
    if not name then return end
    event.executeAfterMs(2000, function()
        message.print(message.convert("Entering: " .. name))
    end)
end)
```

**Testing:** Travel between areas. Locations set to `false` in the config no longer trigger a popup. Users can open `settings.lua` in any text editor and toggle locations as they wish: no code changes needed.

---

## Final File Overview

```text
x64/scripts/MapAnnouncer.lua
x64/scripts/MapAnnouncer/locations.lua
x64/scripts/config/MapAnnouncerConfig/settings.lua
```

---

## What's Next?

Congratulations: you just built your first Lua mod for Final Fantasy XII from scratch. And this is just the beginning.

The FF12 Lua Loader exposes a rich API that goes far beyond events and messages. Here are some things you can explore:

- **Memory read/write**: Read and modify any value in the game's memory in real-time. Change a character's HP, strength, gil, or any other stat directly from a script.
- **Hooks**: Hook into specific memory addresses to intercept and alter the game's execution flow, changing how core systems behave at a low level.
- **More events**: Beyond `onMapJump`, you can hook into `onInitDone` (game fully loaded), `onFlip` (every frame), `onSaveLoad` (save game loaded), and `onOpenFile` (file access).
- **Save/load handlers**: Persist custom data alongside the player's save game and restore it when they load, enabling stateful mods that remember things between sessions.
- **Flags**: Create flags that scripts can use to communicate with each other, enabling inter-mod signaling and coordination.
- **File change handler**: Watch config files for changes and hot-reload your mod automatically when the player edits them, without needing to restart the game.
- **JSON config**: Save and load structured data as JSON files using `config.saveJson` and `config.loadJson`, useful for complex mod state or user preferences.
- **Global symbols**: Register named memory addresses as global symbols so other mods can discover and interact with your mod's internals.
- **Assembly**: Parse and assemble x64 instructions directly from Lua, for advanced patching scenarios where you need to modify the game's executable code at runtime.
- And much more.

{% content-ref url="../tools/lua-loader.md" %}
[FF12 Lua Loader](../tools/lua-loader.md)
{% endcontent-ref %}

