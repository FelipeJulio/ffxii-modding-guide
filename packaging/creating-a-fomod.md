# Creating a FOMOD Installer

When distributing your mods, you want the installation process to be as smooth as possible for players. A **FOMOD installer** allows mod managers like Vortex and MO2 to present a graphical wizard when the user installs your mod, complete with custom text, images, and optional files to select.

Even if your mod doesn't have optional files, using a FOMOD is considered a **best practice** because it guarantees that your files are routed to the correct directories inside the mod manager.

---

## Folder Structure

The root of your zip archive must contain a `fomod` folder and a `data` folder (some creators name it `00 - Core`, but `data` is standard).

A typical, well-structured FOMOD looks like this:

```text
MyMod.zip/
├── fomod/
│   ├── Info.xml
│   └── ModuleConfig.xml
└── data/
    ├── mods/
    │   └── deploy/
    │       └── ff12data/
    │           └── ... (Your FF12 External File Loader / VBF files)
    └── x64/
        └── scripts/
            └── ... (Your Lua scripts)
```

By keeping your actual mod files inside `data/`, the root directory stays clean and organized.

---

## The XML Files

To create the installer, you only need to write two simple XML files inside the `fomod` folder.

### 1. `Info.xml`

This file contains the basic metadata of your mod. It tells the mod manager what your mod is called, who made it, and what it does.

```xml
<fomod>
    <Name>My Awesome Mod</Name>
    <Author>Your Name</Author>
    <Version>1.0.0</Version>
    <Website>https://www.YOUR-MOD-URL.com/</Website>
    <Description>A short description of what your mod does.</Description>
</fomod>
```

{% hint style="info" %}
Notice the `<Version>` field. Use **Semantic Versioning** (`MAJOR.MINOR.PATCH`, like `1.0.0`) here and keep it in sync with your mod page. See [Updating and Versioning Your Mod](updating-and-versioning.md) for the details.
{% endhint %}

### 2. `ModuleConfig.xml`

This is the brain of the installer. It dictates exactly which folders from your zip get installed and where they go.

**Critical Rule:** FFXII relies on two completely different file paths. Assets replacing `.vbf` files must go to the `mods/deploy/...` folder for the FF12 External File Loader, while Lua scripts must go to `x64/scripts`.

The `ModuleConfig.xml` solves this routing perfectly:

```xml
<config xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:noNamespaceSchemaLocation="http://qconsulting.ca/fo3/ModConfig5.0.xsd">
    <moduleName>My Awesome Mod</moduleName>

    <requiredInstallFiles>
        <!-- Routes your VBF replacement files to the correct FF12 External File Loader folder -->
        <folder source="data\mods" destination="mods" />

        <!-- Routes your Lua scripts to the correct loader folder -->
        <folder source="data\x64" destination="x64" />
    </requiredInstallFiles>
</config>
```

When Vortex or MO2 reads this file, it will take the contents of your zip's `data/mods` folder and place it exactly where it needs to be in the player's game directory. It will do the same for the `data/x64` folder.

---

## Optional Plugins (Advanced)

If you have optional features (like a Hard Mode patch or different language translations), you can add `installSteps` to your `ModuleConfig.xml` to present checkboxes to the user.

```xml
<config xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:noNamespaceSchemaLocation="http://qconsulting.ca/fo3/ModConfig5.0.xsd">
    <moduleName>My Awesome Mod</moduleName>

    <requiredInstallFiles>
        <folder source="data\mods" destination="mods" />
        <folder source="data\x64" destination="x64" />
    </requiredInstallFiles>

    <installSteps order="Explicit">
        <installStep name="Optional Features">
            <optionalFileGroups order="Explicit">
                <group name="Complements" type="SelectAny">
                    <plugins order="Explicit">

                        <plugin name="Complement A">
                            <description>Install Complement A.</description>
                            <files>
                                <folder source="Complement_A\x64" destination="x64" />
                            </files>
                            <typeDescriptor>
                                <type name="Optional" />
                            </typeDescriptor>
                        </plugin>

                        <plugin name="Complement B">
                            <description>Install Complement B.</description>
                            <files>
                                <folder source="Complement_B\x64" destination="x64" />
                            </files>
                            <typeDescriptor>
                                <type name="Optional" />
                            </typeDescriptor>
                        </plugin>

                    </plugins>
                </group>
            </optionalFileGroups>
        </installStep>
    </installSteps>
</config>
```

---

## Testing Your FOMOD

Before uploading to Nexus Mods, you should always test your installer locally:

1. Select the `fomod` and `data` folders and **Zip them**.
2. Open your Mod Manager (MO2 or Vortex).
3. Install the mod from the Zip file you just created.
4. Verify that the files were correctly placed in the `mods/deploy/ff12data/` and `x64/scripts/` folders.

{% hint style="warning" %}
**Bundling dependencies?** If your mod relies on a framework or another creator's mod, never pack it into your zip. Set it as a hard dependency instead, see the [Code of Conduct](../getting-started/code-of-conduct.md) for the full guidelines.
{% endhint %}

