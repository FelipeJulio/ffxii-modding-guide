# Text Tags

**Text Tags** is a spreadsheet listing every text tag the game uses inside dialogue and menu strings.

**Credits:** Xeavin

### What can you do with this?

Text tags are how the game embeds formatting, timing, button prompts, and dynamic values (item names, amounts, NPC names) into a line of dialogue: things like `{wait}`, `{color:x}`, or `{icon:x}`. This spreadsheet is the raw reference for the whole system. It is worth reading the **Other Information** tab first, since it explains the byte-structure terms the other tabs rely on.

**Spreadsheet contents:**

- **Special Text Tags:** the main table. Every tag, keyed by its raw byte sequence, with its parameters and valid ranges and notes on behavior. An "Unused?" column flags tags that exist in the game's code but appear in no actual text, and some byte codes are still undocumented. This is the reference for hand-writing or decoding custom dialogue strings.
- **Argument Types:** the nine argument types (Caster, Target, Gil, Status Effect, Level, Content, Action, Count, and so on) used by battle-message dialogue headers. A dialogue's header points to one of these, which tells the game what kind of value to substitute into an argument tag.
- **Header Identifiers:** the values for the `{header:x}` tag, which sets the label in the top-right corner of a dialogue box ("Next", "Close", "Log & Next").
- **Icon Identifiers:** the icon IDs usable with the `{icon:x}` tag: minimap building icons, elemental icons, status icons, and more. Some require a specific version of The Insurgent's Manifesto to display correctly.
- **Other Information:** general notes on how the tag system works: the byte structure every tag shares (an indicator byte, an identifier byte, and parameter bytes), the `{Tag}` naming convention, and how pixel-based tags assume a 1280x720 resolution and scale at other resolutions.

{% hint style="info" %}
**Companion reading**
For a narrative walkthrough of the tag system, see The Insurgent's Handbook's [Text Tags](https://xeavin.gitbook.io/the-insurgents-handbook/text/text-tags) and [Formats](https://xeavin.gitbook.io/the-insurgents-handbook/text/formats) pages.
{% endhint %}

{% hint style="info" %}
**Access the spreadsheet**

<a href="https://onedrive.live.com/:x:/g/personal/553D7CDB377276FA/Qfp2cjfbfD0ggFWWAAAAAAAAe4Z0XLzxY5VBCw" class="button primary" target="_blank" data-icon="external-link-alt">Open the Spreadsheet</a>
{% endhint %}

{% content-ref url="the-insurgents-handbook.md" %}
[the-insurgents-handbook.md](the-insurgents-handbook.md)
{% endcontent-ref %}
