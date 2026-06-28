# Creating a Lua Mod

One of the most powerful ways to mod Final Fantasy XII today is by writing your own custom scripts in **Lua**. This allows you to manipulate the game's memory, call internal functions, and change logic dynamically without hard-patching the game executable.

## The Foundation: Lua Loader

To create or run any Lua mods, you absolutely must have the **Lua Loader** installed. It is the engine that injects your custom code into the game.

To actually write these mods, you must use the official documentation as your primary base of reference. It contains all available functions, memory addresses, and event hooks.

{% content-ref url="../tools/lua-loader.md" %}
[Learn more about Lua Loader](../tools/lua-loader.md)
{% endcontent-ref %}
---

## Recommended Code Structure

When structuring the code of your Lua mod, it is highly recommended to follow established best practices:

```
├── MyModName.lua
├── MyModName/
│   ├── module1.lua
│   └── module2.lua
└── config/
    └── MyModName/
        └── settings.lua
```

### 1. The Main File (`MyModName.lua`)

This is the entry point of your mod. Its primary responsibility is **not** to hold all the logic, but to initialize the mod. It should load your configurations, require your internal modules, and register the primary events.

### 2. The Modules Folder (`/MyModName/`)

Separate your logic into smaller files (modules) and place them inside this folder. For example, one file for handling UI and another for math. Your main file will just load these modules.

### 3. The Config Folder (`/config/MyModName/`)

Place a `settings.lua` or `settings.json` file inside the `config` folder to expose parameters safely to the end user or other modders, avoiding the need for them to edit your core code.

---

## Code Examples

Now that you understand the best practices for folder structure, you can see how this looks in practice with our code examples.

{% content-ref url="../examples/lua-modding-example.md" %}
[View Example: Reading Map IDs](../examples/lua-modding-example.md)
{% endcontent-ref %}
---

## Scripting Frameworks

Writing Lua mods from scratch can be challenging for complex mechanics. Fortunately, there are **Scripting Frameworks** that run on top of the Lua Loader. You can use these frameworks as dependencies to accomplish complex tasks easily.

### The Insurgent's Forge

A massive framework that overhauls how the game handles action formulas. Instead of hardcoded `.exe` logic, Forge allows you to calculate damage, status effects, and combat mechanics using Lua classes and middlewares.

{% content-ref url="../frameworks/insurgents-forge.md" %}
[Learn more about The Insurgent's Forge](../frameworks/insurgents-forge.md)
{% endcontent-ref %}
### Dynamic Description

An API and framework designed to generate real-time item and ability descriptions in the UI by reading the battlepack data directly from the game's memory.

{% content-ref url="../frameworks/dynamic-description.md" %}
[Learn more about Dynamic Description](../frameworks/dynamic-description.md)
{% endcontent-ref %}
