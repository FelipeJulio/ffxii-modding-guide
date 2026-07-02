# Locations

**Locations** is the master index of every location in the game and which underlying files it loads.

**Credits:** Xeavin

### What can you do with this?

Nearly every area in the game is built from a few underlying files, and different named locations often share them. Before you can edit or export the right file in The Insurgent's Toolkit's ARD or EBP editors, you first need to know which files your current location actually uses. This spreadsheet is that lookup, covering roughly 1,316 location entries.

Each row gives:

- the **location ID**, its **region**, and its **display name** (many early entries are reserved test or debug locations),
- the **`.ard` file** it loads (the area's enemy and unit data),
- the **`.ebp` file** it loads (the map's event and logic scripts),
- the **MapCtrl** reference (the map control and background), and
- the **event name**, where one applies.

Because many locations share the same `.ard` or `.ebp` file (one large area split into several named sub-locations), this sheet is how you tell whether editing one location's file will also change others. It is also how you work out the correct export path a file needs, for example the full folder structure for an `.ard` export: `ps2data/plan_master/in/plan_map/dst_a/area/dst_a.ard.dir`.

{% hint style="warning" %}
The Insurgent's Toolkit keeps only one `.ard` or `.ebp` file loaded in memory at a time. Since many locations share the same file, switching to a different location can silently overwrite unsaved changes if the new location uses a different file. Check this sheet first to see whether two locations you are editing share a file.
{% endhint %}

{% hint style="info" %}
**Access the spreadsheet**

<a href="https://1drv.ms/x/s!Avp2cjfbfD1VgQgMMEfnznpsO5He" class="button primary" target="_blank" data-icon="external-link-alt">Open the Spreadsheet</a>
{% endhint %}

{% content-ref url="enemy-and-area-data-map.md" %}
[enemy-and-area-data-map.md](enemy-and-area-data-map.md)
{% endcontent-ref %}
