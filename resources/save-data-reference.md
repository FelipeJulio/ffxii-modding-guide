# Save Data Reference

**Save Data Reference** is a memory-offset map of the game's save data.

**Credits:** Eochaid

### What can you do with this?

The Save Game Editor can view and modify essentially everything the game remembers about a player's progress, split into 5 technical sections (Main Extended Info, Global Info, Battle Info Old/New, Menu Info, Main Basic Info). This sheet documents Global Info specifically, byte by byte, across three tabs: the main ~1,974-row breakdown of every field (story flags, NPC talk counters, and more, each with its address, type, and internal VM script variable name), a quest stage tab explaining what each numeric stage value means for a given quest (for example, what "50" means for the Rogue Tomato hunt), and a global flags tab covering major story-progress checkpoints and what UI or features unlock at each one.

The Toolkit's own docs note that inventory changes specifically should go through the Inventory Editor instead, the Save Game Editor can technically touch inventory data too, but it's easy to break that way.

{% hint style="info" %}
**Access the spreadsheet**

<a href="https://1drv.ms/x/s!Avp2cjfbfD1VgRLUKGdZBJ1suR7s" class="button primary" target="_blank" data-icon="external-link-alt">Open the Spreadsheet</a>
{% endhint %}

{% content-ref url="inventory-contents.md" %}
[inventory-contents.md](inventory-contents.md)
{% endcontent-ref %}
