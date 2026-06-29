# Installing Mods

There are three ways to install mods for Final Fantasy XII: The Zodiac Age. Using a Mod Manager is strongly recommended for most users.

---

## Vortex

**Vortex** is the official mod manager from Nexus Mods. It is the most beginner-friendly option, with one-click installation directly from mod pages.

{% hint style="warning" %}
**Vortex known issues**
Vortex is the easiest to get started with, but it is not always the most reliable option. It can occasionally have issues with mod deployment or failing to recognize certain mods. If you install mods and they are not working, try uninstalling and reinstalling the **External File Loader** and **Lua Loader** through Vortex first before troubleshooting anything else.

For a more stable experience, consider using **Mod Organizer 2** instead.
{% endhint %}

**How to install mods with Vortex:**

1. Download and install Vortex.
2. Open Vortex, go to **Games**, search for Final Fantasy XII, and click **Manage**.
3. On any mod page, click the **Mod Manager Download** button: Vortex handles the rest automatically.
4. Go to **Mods** in the left sidebar and make sure the mod is enabled.
5. Click **Deploy Mods** to apply changes to the game.

{% hint style="danger" %}
**External File Loader hook method**
When installing the External File Loader, it will ask you to choose a hook method. **Select `dinput8.dll`** when using Vortex.
{% endhint %}

{% hint style="info" %}
**Download Vortex**

<a href="https://www.nexusmods.com/site/mods/1" class="button primary" data-icon="external-link-alt">Download Vortex</a>
{% endhint %}

---

## Mod Organizer 2

**Mod Organizer 2 (Mod Organizer 2)** is the recommended mod manager for FFXII. It uses a virtual file system to keep your game directory completely clean: mods are never written directly into the game folder. The only extra step compared to Vortex is a one-time plugin installation.

{% hint style="warning" %}
**FF12 Plugin Required**
Mod Organizer 2 does not support Final Fantasy XII out of the box. You must install the community-made FF12 plugin. All installation instructions are on the plugin's mod page.

<a href="https://www.nexusmods.com/finalfantasy12/mods/430" class="button primary" data-icon="external-link-alt">FF12 Plugin for Mod Organizer 2</a>
{% endhint %}

**How to install mods with Mod Organizer 2:**

1. Download and install Mod Organizer 2.
2. Install the FF12 plugin and configure it following the author's documentation.
3. Download a mod file manually from Nexus Mods.
4. In Mod Organizer 2, click the **Install Mod** button (disk icon) and select the downloaded archive.
5. Enable the mod by checking the box in the left pane.
6. Always launch the game **through Mod Organizer 2** so the virtual file system loads your mods.

{% hint style="danger" %}
**External File Loader hook method**
When installing the External File Loader, it will ask you to choose a hook method. **Select the Mod Organizer 2 option** when using Mod Organizer 2, as Mod Organizer 2 has its own hook system and requires a different setting than Vortex.
{% endhint %}

{% hint style="info" %}
**Download Mod Organizer 2**

<a href="https://github.com/Modorganizer2/modorganizer/releases" class="button primary" data-icon="external-link-alt">Download Mod Organizer 2</a>
{% endhint %}

---

## Manual Installation

Manual installation requires understanding how FFXII's mod folder structure works. It is intended for users who already know how the game loads mods and want full control.

{% hint style="danger" %}
**Not recommended for casual users.** Manual installation is for experienced modders who understand how FFXII modding works. If you just want to install and play mods, use Vortex or Mod Organizer 2 instead.
{% endhint %}

There are two separate locations where mod files go, depending on the type of mod:

**Binary game file replacements (External File Loader mods):**
Place your files inside the game's mod folder, mirroring the VBF structure:
`mods/deploy/ff12data/...`

**Lua script mods:**
Place your scripts inside:
`x64/scripts/...`

{% content-ref url="modding-folder-structure.md" %}
[Modding Folder Structure](modding-folder-structure.md)
{% endcontent-ref %}

---

## Conflict Management

When two mods modify the same file, a conflict occurs. One mod will overwrite the other, and the player may lose changes from whichever mod loses the conflict.

**Vortex and Mod Organizer 2 both include visual conflict managers.** When a conflict is detected, you can see exactly which mods are fighting over the same file and decide which one should take priority. Mod authors usually document known conflicts and the correct load order on their mod page: always check there first.

Manual installation has no conflict management tooling. You are responsible for tracking which files each mod touches and resolving overlaps yourself. This is one of the main reasons manual installation is not recommended for most users.
