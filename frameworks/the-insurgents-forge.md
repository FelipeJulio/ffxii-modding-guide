# The Insurgent's Forge

**The Insurgent's Forge** is a Lua-based framework that runs on top of the FF12 Lua Loader, designed specifically to overhaul how the game handles action formulas.

**Credits:** Xeavin

### What does it do?

In the vanilla game, every action (like casting _Cure_ or attacking with a sword) uses a "formula" to determine what happens. This formula calculates damage, checks for elemental immunities, adds status effects, and determines if the attack misses. These formulas are usually hardcoded in the game's executable.

The Insurgent's Forge bypasses this limitation. It allows you to:

- **Modify existing formulas** to the tiniest detail using Lua.
- **Create entirely new formulas** from scratch.
- Use object-oriented classes and helper functions to manage complex battle logic.
- Assign your custom formulas to actions or equipment using the Battlepack Editor (via The Insurgent's Toolkit).

{% hint style="info" %}
**Official Documentation** Because it completely changes how the game processes logic, learning The Insurgent's Forge requires reading its detailed breakdown of formulas, functions, assemblies, and middlewares.

<a href="https://www.nexusmods.com/finalfantasy12/mods/386" class="button primary" target="_blank" data-icon="external-link-alt">Go to Official Mod Page</a>
{% endhint %}

---

### See it in Action

Want to see how simple it is to write an Insurgent's Forge function? Check out our quick example!

{% content-ref url="../examples/forge-modding-example.md" %}
[View Example: Creating an Insurgent's Forge Function](../examples/forge-modding-example.md)
{% endcontent-ref %}
