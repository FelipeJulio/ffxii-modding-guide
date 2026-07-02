# Locations

**Locations** is the master index of every location in the game and which underlying files it loads.

**Credits:** Xeavin

### What can you do with this?

Before you can export or target the right file in The Insurgent's Toolkit's ARD or EBP editors, you need to know which `.ard` and `.ebp` file your current location actually uses, since many locations share the same file. This spreadsheet is that lookup, covering roughly 1,316 location entries: location name, region, the exact `.ard`/`.ebp`/map control file names behind it, and the event name where relevant. It's referenced directly from multiple Toolkit editor pages as the way to figure out the correct export path, for example the full folder structure an `.ard` export needs (`ps2data/plan_master/in/plan_map/dst_a/area/dst_a.ard.dir`).

{% hint style="warning" %}
The Insurgent's Toolkit only keeps one `.ard` or `.ebp` file loaded in memory at a time. Since many locations share the same file, switching to a different location can silently overwrite unsaved changes if the new location uses a different file. Check this sheet first to see whether two locations you're editing actually share a file.
{% endhint %}

{% hint style="info" %}
**Access the spreadsheet**

<a href="https://1drv.ms/x/s!Avp2cjfbfD1VgQgMMEfnznpsO5He" class="button primary" target="_blank" data-icon="external-link-alt">Open the Spreadsheet</a>
{% endhint %}

{% content-ref url="enemy-and-area-data-map.md" %}
[enemy-and-area-data-map.md](enemy-and-area-data-map.md)
{% endcontent-ref %}
