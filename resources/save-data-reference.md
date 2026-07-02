# Save Data Reference

**Save Data Reference** is a memory-offset map of the game's save data.

**Credits:** Eochaid

### What can you do with this?

A save file records everything the game remembers about your progress. The Insurgent's Toolkit's Save Game Editor can view and change nearly all of it, and this spreadsheet is the map that tells you what each part means. It focuses on the "Global Info" section, the largest and most important part of a save, and decodes it byte by byte.

**Spreadsheet contents:**

- **Global Info:** the main breakdown, around 1,974 fields. Each row gives the field's memory address and data type, the group it belongs to, a human-readable label, and the internal VM script variable name that EBP scripts use to read it. This covers everything from story flags to per-NPC talk counters.
- **Quest Stages:** for each quest, what its numeric stage value actually means. A quest stored as "50," for example, might mean "defeated the first stage." Use this to make sense of a raw stage number.
- **Global Flags:** the major story-progress checkpoints, describing what each flag marks (for example, "after controlling Reks") and which menus or features unlock at that point.

{% hint style="warning" %}
The Save Game Editor can technically edit inventory too, but it is easy to corrupt a save that way. To add or remove items, use the Inventory Editor instead.
{% endhint %}

{% hint style="info" %}
**Access the spreadsheet**

<a href="https://1drv.ms/x/s!Avp2cjfbfD1VgRLUKGdZBJ1suR7s" class="button primary" target="_blank" data-icon="external-link-alt">Open the Spreadsheet</a>
{% endhint %}

{% content-ref url="inventory-contents.md" %}
[inventory-contents.md](inventory-contents.md)
{% endcontent-ref %}
