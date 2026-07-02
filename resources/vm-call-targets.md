# VM Call Targets

**VM Call Targets** is a low-level reference for every VM call the game's script VM can invoke, including argument types and in-memory function addresses.

**Credits:** Xeavin

### What can you do with this?

The game's event and map scripts (EBP scripts) do their work by calling into a fixed set of built-in VM functions: movement, dialogue, camera control, item and gil checks, and much more. This spreadsheet is the low-level reference for those calls. For each one it gives the identifier, the internal function name, the argument count and the type of each argument, the return type, whether any shipped script actually uses it, and the in-memory addresses that back the call.

**Spreadsheet contents:** the calls are grouped into four tabs by range.

- **Basic Calls:** the large general-purpose range (around 1,500 calls). Movement (`setpos`, `move`), dialogue and messages (`ames`, `aask`, `messync`), camera, animation playback, item and gil checks, and more. This is the range you use when writing or editing an EBP event script.
- **Debug Calls:** debug-only calls left in the retail build. Almost none are used by any shipped script.
- **Battle Calls:** battle-specific calls (mostly prefixed `btlAtel`) for configuring a battle unit's ability, status, team, and event data.
- **Menu Calls:** fullscreen menu calls (prefixed `fsmenu`) that drive menu flow and UI outside of battle.

For a quick, reader-friendly lookup of the basic EBP scripting calls (name and arguments only), The Insurgent's Handbook's VM Call Targets page is the narrative companion. Use this spreadsheet when you need argument types, return types, or the other call ranges.

{% hint style="info" %}
**Access the spreadsheet**

<a href="https://onedrive.live.com/:x:/g/personal/553d7cdb377276fa/IQAE0VpMAD1mSa_TjHWYIQE4AQ5z4mpwakZm-OMzgtEBUi0" class="button primary" target="_blank" data-icon="external-link-alt">Open the Spreadsheet</a>
{% endhint %}

{% content-ref url="the-insurgents-handbook.md" %}
[the-insurgents-handbook.md](the-insurgents-handbook.md)
{% endcontent-ref %}
