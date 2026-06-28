# Dynamic Description

**Dynamic Description** is a real-time text generator and API for Final Fantasy XII: The Zodiac Age.

### What does it do?

Usually, the descriptions for items, weapons, or spells are hardcoded as static text. If you change a sword's attack power using a mod, its description will still show the old value unless you manually edit the text files too.

Dynamic Description solves this problem. It reads the battlepack data directly from the game's memory while the game is running. By acting as an API alongside mods like *The Insurgent's Descriptive Inventory*, it automatically generates accurate, dynamic item descriptions based on the actual stats the item has at that exact moment.

If you are a modder creating new weapons or modifying stats dynamically, you can use the Dynamic Description API to ensure the player's UI always reflects the truth.

{% hint style="info" %}
**Official Documentation**
To learn how to integrate this framework into your own Lua mods and use its API calls to generate custom descriptions, visit the official page.

<a href="https://www.nexusmods.com/finalfantasy12/mods/466" class="button primary" data-icon="external-link-alt">Go to Official Mod Page</a>
{% endhint %}
