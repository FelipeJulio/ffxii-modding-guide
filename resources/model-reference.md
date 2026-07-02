# Model Reference

**Model Reference** is an index of every 3D model file in the game, identified by its model ID and file path.

**Credits:** Xeavin, Eochaid

### What can you do with this?

Every 3D model in the game lives in a `.cm` file, and each one has a numeric model ID. This spreadsheet is the index that connects the two: give it a model ID or a name, and it tells you the file path inside the game's archive. Use it when you need to find or swap a specific model.

Every tab shares a core set of columns: the model ID (in hex and decimal), the model's name, the `.cm` file it points to inside `ps2data`, and notes (which flag quirks such as duplicate models, or reserved IDs that crash the game if used). **Spreadsheet contents:**

- **Backgrounds:** static scenery and interactive objects (doors, elevators, plants, save crystals, decor).
- **Party Members:** the playable characters, including story-specific variants. These rows add a set of true/false flags, one per weapon type, showing which weapon-holding model variants exist for that character.
- **Monsters:** enemy models, with Variation and Color Variation columns for palette-swapped types that share a single model.
- **NPCs:** named NPCs and generic town extras, with outfit and color variations and per-town area flags.
- **Summons:** esper models, both their summoned form and their "(Boss)" story-fight form.
- **Gadgets:** miscellaneous held and interactive objects: key items, vehicles like the Strahl, and story props.
- **Treasures:** chest and container models (chests, urns, pots, and the Mimic disguises).
- **Weapons:** individual weapon prop models as held in hand, including palette variants.

Several of these also have a "high" companion tab (Party Members, NPCs, and Summons) holding the higher-poly versions used in cutscenes and close-ups.

This is a global index of every model in the game. If you instead want to know which models a specific area actually uses, the Enemy & Area Data Map covers that narrower, per-area scope.

{% hint style="info" %}
**Access the spreadsheet**

<a href="https://onedrive.live.com/:x:/g/personal/553D7CDB377276FA/Qfp2cjfbfD0ggFWDAAAAAAAA9tJrrBaY-Z83Yg" class="button primary" target="_blank" data-icon="external-link-alt">Open the Spreadsheet</a>
{% endhint %}

{% content-ref url="enemy-and-area-data-map.md" %}
[enemy-and-area-data-map.md](enemy-and-area-data-map.md)
{% endcontent-ref %}
