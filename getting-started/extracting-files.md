# Extracting Files

Now that you understand the internal structure of the game, you need a way to actually pull those original files out of the `.vbf` archive so you can modify them.

To do this, we use the **VBF Browser**.

## VBF Browser

The **VBF Browser** is an essential tool that lets you browse the massive `FFXII_TZA.vbf` file and extract exactly what you need.

### How to Extract a File

{% content-ref url="../tools/vbf-browser.md" %}
[Learn more about VBF Browser](../tools/vbf-browser.md)
{% endcontent-ref %}
Extracting a file is very simple:

1. **Download and Open:** Download the tool from Nexus Mods and run the application.
2. **Open the Archive:** Use the File menu to open your `FFXII_TZA.vbf` file (usually located in your Steam installation folder).
3. **Navigate:** Use the directory tree on the left side (which we covered in the previous section) to find the file you want to edit.
4. **Extract:** Right-click the file and select **Extract**. Choose a safe folder on your computer to save it.

Once you have extracted the file, you are ready for the next step: modifying or decompiling it!

{% hint style="warning" %}
**Important:** When extracting files like `battle_pack.bin`, it is highly recommended to recreate and keep the **complete folder structure** intact on your computer. You will need this exact path later when creating a mod loadable by the External File Loader, which will be explained in detail later in the guide.
{% endhint %}
