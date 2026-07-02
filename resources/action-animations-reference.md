# Action Animations Reference

**Action Animations Reference** is a spreadsheet cataloguing the visual animation played by every spell, weapon hit, and Mist Action in the game.

**Credits:** Eochaid

### What can you do with this?

When you reassign an action to use a different animation, this sheet tells you exactly what that animation looks like and how it behaves, so you do not ship a change that looks wrong in play. The most important field is whether an animation is "AoE friendly." Some animations only connect visually to their first target and affect the rest silently a moment later. Cure is the classic example: it plays on one ally while the others are healed with no visible effect. "AoE friendly" here means the animation is visually correct on every target it hits, which is not the same thing as whether the action can hit a group.

**Spreadsheet contents:**

- **Animations:** the main list (around 99 entries) of spell and action animations. Each row gives the animation ID, the action it belongs to (Cure, Fire, Holy, and so on), a plain-language description of what it looks like, and flags for whether it is AoE friendly, has a party-wide effect, or triggers a cinematic camera.
- **Effect Finishes:** a separate ID range (starting at 32769) covering weapon hit "finish" effects, the flash or particle burst shown on a successful attack (Bash, Slash, Ninja Sword, Gun, Firework, and more), broken down by color and element variant.
- **Event Animations:** the animation IDs used specifically for Mist Actions. Many of these are placeholder poses, used for IDs that were never given a unique Mist animation.

{% hint style="info" %}
**Access the spreadsheet**

<a href="https://docs.google.com/spreadsheets/d/1UYFBz27shCOHux1N5NOXNPS7rN7WJebxyhjoIg6DWs0/edit" class="button primary" target="_blank" data-icon="external-link-alt">Open the Spreadsheet</a>
{% endhint %}
