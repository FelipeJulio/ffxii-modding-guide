# FF12 Lua Loader

The **FF12 Lua Loader** is the foundational module that enables dynamic Lua scripting in Final Fantasy XII.

**Credits:** ffgriever

### What does it do?

Instead of hard-patching the game's `.exe` or dealing exclusively with static asset files, the FF12 Lua Loader injects a Lua engine into the game. It provides an API of memory hooks and internal game functions.

With it, you can:

- Read and write game memory in real-time.
- Hook into core game functions to change how the game behaves.
- Serve as the required dependency engine for almost all modern Lua-based mods.

{% hint style="info" %}
**Official API & Documentation** The FF12 Lua Loader has an extensive list of known calls, functions, and memory addresses. To actually write Lua mods, you must consult its official documentation.

<a href="https://xeavin.gitbook.io/ff12-lua-loader" class="button primary" target="_blank" data-icon="external-link-alt">Go to Official Documentation</a>
{% endhint %}

---

### Want to write your own?

Check out our brief guide on the best practices for structuring your code and a simple practical example.

{% content-ref url="../getting-started/creating-lua-mod.md" %}
[Creating a Lua Mod](../getting-started/creating-lua-mod.md)
{% endcontent-ref %}

{% content-ref url="../getting-started/modding-folder-structure.md" %}
[Modding Folder Structure](../getting-started/modding-folder-structure.md)
{% endcontent-ref %}
