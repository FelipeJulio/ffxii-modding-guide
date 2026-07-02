# Text Tags

**Text Tags** is a spreadsheet listing every text tag the game uses inside dialogue and menu strings.

**Credits:** Xeavin

### What can you do with this?

Text tags are how the game embeds formatting, timing, button prompts, and dynamic values (item names, amounts, NPC names) into a line of dialogue, things like `{wait}`, `{color:x}`, or `{icon:x}`. This sheet is the raw reference: every tag's byte sequence, its parameters and valid ranges, and notes on quirks and unused tags. It's the same data The Insurgent's Handbook's Text Tags page points readers to for the full list, that page explains the naming scheme and philosophy, this sheet has the exhaustive detail.

Before diving into the main tag table, read the sheet's general notes tab first. It explains the byte structure every tag shares (an indicator byte, an identifier byte, and parameter bytes), the `{Tag}` naming convention, and how pixel-based tags assume a 1280x720 resolution and get scaled at other resolutions, terms and concepts the other tabs assume you already know.

{% hint style="info" %}
**Access the spreadsheet**
For a narrative walkthrough of the tag system, see The Insurgent's Handbook's [Text Tags](https://xeavin.gitbook.io/the-insurgents-handbook/text/text-tags) and [Formats](https://xeavin.gitbook.io/the-insurgents-handbook/text/formats) pages.

<a href="https://onedrive.live.com/:x:/g/personal/553D7CDB377276FA/Qfp2cjfbfD0ggFWWAAAAAAAAe4Z0XLzxY5VBCw" class="button primary" target="_blank" data-icon="external-link-alt">Open the Spreadsheet</a>
{% endhint %}

{% content-ref url="the-insurgents-handbook.md" %}
[the-insurgents-handbook.md](the-insurgents-handbook.md)
{% endcontent-ref %}
