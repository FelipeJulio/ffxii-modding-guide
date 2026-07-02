# FF12 VM Script Decompiler

The **FF12 VM Script Decompiler** is a tool specifically focused on the game's map logic and event files.

**Credits:** ffgriever

### What does it do?

The game's maps and events run on a custom Virtual Machine using scripts stored inside `.ebp` files. This tool decompiles these raw binary `.ebp` scripts into a readable, C-like language.

By decompiling these scripts, you can:

- Add new NPCs to a map or edit existing ones.
- Change text, dialogues, and event triggers.
- Modify deep map-related features and mechanics (like trap placements or enemy spawn logic).

Once your edits are done, the tool compiles your C-like code back into a binary `.ebp` file that the game can execute.

{% hint style="warning" %}
**Technical Requirement** Because the decompiled scripts are represented in a C-like structure (with variables, functions, and arrays), using this tool effectively requires at least a basic understanding of C or similar programming languages.
{% endhint %}

{% hint style="info" %}
**Official Page & Documentation** For complete installation instructions, command-line arguments, and a deep dive into the VM architecture, please visit the official mod page.

<a href="https://www.nexusmods.com/finalfantasy12/mods/124" class="button primary" data-icon="external-link-alt">Go to Official Mod Page</a>
{% endhint %}

---

### See it in Action

Curious about how a C-like EBP script looks? Check out our quick example on how to spawn an NPC.

{% content-ref url="../examples/ebp-modding-example.md" %}
[View Example: Creating and Spawning an NPC](../examples/ebp-modding-example.md)
{% endcontent-ref %}
