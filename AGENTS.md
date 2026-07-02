# AGENTS.md

Instructions for any LLM or AI agent contributing to the **FFXII: The Zodiac Age Modding Guide**. Read this fully before creating or editing any page. These rules override default behavior.

This is a **GitBook** documentation project. The audience ranges from complete beginners to experienced modders, so every page must be approachable without being shallow.

---

## 1. Fetch GitBook context first

Before writing any GitBook-specific markup, get accurate context on the available components.

1. **Prefer the GitBook MCP server.** If it is connected, use it to look up component syntax and documentation: https://gitbook.com/docs/~gitbook/mcp
2. **If the MCP is not connected,** ask the requester whether they would like to set up the connection. Do not assume.
3. **If they decline,** fall back to studying the existing `.md` files in this repo (start with any section `README.md` and a tool or framework page). Match the patterns you find there exactly. Never invent component syntax.

---

## 2. Writing style

The voice is **simple, clear, direct, and friendly**. Imagine explaining to a smart person who has never modded before.

- **Be semantic and coherent.** Every paragraph should earn its place and follow logically from the last.
- **Avoid prolixity.** Cut filler. Do not pad. A short, well structured page beats pages of rambling text. Less is more.
- **Explain step by step.** Many readers are not technical. Break processes into ordered, followable steps. Never assume hidden knowledge; if a term is new, define it the first time it appears.
- **Friendly, not casual to a fault.** Encouraging and warm, but still precise and trustworthy.
- **Never use em-dashes (`—`).** Rewrite with commas, parentheses, or separate sentences. This applies to every page.
- **Question your own writing before committing it.** After drafting a paragraph or page, reread it and ask: Does this actually make sense? Would a newcomer understand it without prior context? Is it accurate, or am I assuming? Does every sentence add value, or is some of it filler? If any answer is no, rewrite it. Do not ship text just to fill space; if you are unsure something is correct or useful, flag it to the requester instead of guessing.

---

## 3. Page structure

Keep all pages consistent. Do not invent new layouts.

**Section intent.** Each top-level section serves a different reader intent. Calibrate tone and depth accordingly:

- **Getting Started:** show the full landscape, everything available and how modding here works. Written for total beginners.
- **Tools:** what each tool is, what problem it solves, what becomes possible with it.
- **Frameworks:** same as Tools, but for in-game frameworks other mods build on.
- **Resources:** external sources, what is in them, what they help with. Always link out, never reproduce.
- **Packaging:** how to package and distribute a finished mod.
- **Examples:** educational, hands-on walkthroughs (not necessarily full mods) demonstrating a technique in practice.

The established structure for a **tool or framework** page is:

1. `# Title` (the full, correct product name).
2. A single bold sentence stating what it is.
3. `### What does it do?` with a short explanation and a bullet list of capabilities. Always use this exact heading, never "Core Features" or any other variant.
4. One or more GitBook `hint` blocks for features, requirements, warnings, and the official link.
5. Where relevant, a `content-ref` linking to a matching example or guide.

Use `---` to separate major sections within a longer page. Do not overuse it; it is for meaningful breaks, not decoration.

**Resources / external source pages.** Some pages exist only to point the reader at an external source, a spreadsheet, a GitHub repo, another GitBook, a doc site, anything not hosted in this guide. The structure is:

1. `# Title` (the full, correct name of the source).
2. A single bold sentence stating what it is.
3. `### What can you do with this?`. Always use this exact heading, unless the one-line description already makes the value obvious, in which case skip it.
4. A `hint` block or button linking out to the actual source. **Never reproduce the source's content on the page:** no copied tables, no re-hosted data. Summarize, then link.

Before writing `### What can you do with this?`, actually open and inspect the real source, do not assume from its name or file list alone. Match the write-up's depth to what the source actually contains: a source with many fields, categories, or clear use cases earns a fuller paragraph covering multiple angles (what it is for, what problem it solves, what it helps you do, what possibilities it opens). A thin source gets a short, honest paragraph. Never pad to fill a template. If neither the request nor the source gives enough to write something substantive, stop and ask the requester what is in it, who would use it, and what problem it solves, instead of guessing (see section 5, this is the same rule extended to content depth, not just crediting).

**Section landing pages** (`README.md` inside each folder) open with a `# Title`, one or two sentences of intro, then a `card` table listing the pages in that section.

**Example and guide titles always use an action format** that states what the reader will accomplish: "Creating X with Y" or "Doing X with Y" (for example, "Creating a Map Announcer Mod with the Lua Loader", "Creating a Custom NPC with the FF12 VM Script Decompiler"). Never use a vague or generic title like "Lua Modding Example". The reader should know the concrete outcome and the main tool involved just from the title.

**When a section grows large, create a landing page for it.** If a section starts accumulating many pages or covering clearly distinct sub-topics, do not keep dumping everything into a flat list. Instead, create a `README.md` for that section with a card table linking to its pages, and add it to `SUMMARY.md` as a parent entry with children. This makes navigation scannable and keeps individual pages focused. The existing sections (Tools, Frameworks, Examples, etc.) already follow this pattern.

**Never abbreviate the name of a mod, tool, or framework anywhere, with no exceptions.** Always use its full, official name in every single place it appears: page titles, body text, `SUMMARY.md`, card tables, links, **file names**, **URLs and slugs**, config paths, and code comments. The name must be identical everywhere for the same item, and the file name must be the full slugified name. For example, the file is `the-insurgents-stat-lores.md` (never `stat-lores.md`), the title is "The Insurgent's Stat Lores" (never "Stat Lores"), and prose says "The Insurgent's Forge" (never "the Forge" or "Forge"). Acronyms count as abbreviations too: write "External File Loader", never "EFL". The only names that legitimately have no prefix are the products whose official name truly lacks one (for example "Dynamic Description" and "Dynamic Preview Icons"); confirm against the page body before assuming.

**File names use kebab-case.** Every `.md` file is named as a full, lowercase, hyphen-separated slug of the page title: `the-insurgents-learnable-foecraft.md`, `creating-a-fomod.md`. No camelCase, no underscores, no abbreviations.

**File paths in documentation always use forward slashes (`/`).** Never backslashes (`\`) or arrows (`>`). Example: `ps2data/plan_master/us/plan_map`, never `ps2data\plan_master\us\plan_map` or `ps2data > plan_master > us > plan_map`.

---

## 4. GitBook components

Use native GitBook components rather than plain markdown wherever one fits. The components in use here:

**Hints** for callouts. Styles: `info`, `warning`, `danger`, `success`.

```
{% hint style="info" %}
**Heading** Body text.
{% endhint %}
```

**Card tables** for section landing pages. Each row links to a page and uses a cover icon from `.gitbook/assets/`:

```
<table data-view="cards"><thead><tr><th></th><th></th><th data-hidden data-card-target data-type="content-ref"></th><th data-hidden data-card-cover data-type="files"></th></tr></thead><tbody>
<tr><td><strong>Page Name</strong></td><td>One line description.</td><td><a href="page.md">page.md</a></td><td><a href="../.gitbook/assets/icon.svg">icon.svg</a></td></tr>
</tbody></table>
```

Section icons are shared per category: tools use `tool.svg`, frameworks use `framework.svg`, examples use `guide.svg`. Keep icons consistent within a section.

**Card image sizes and sourcing rules:**

- GitBook recommends 1920x1080 for card covers, but that is too heavy for cards. Use **~960x540** (half resolution) to keep page load fast.
- **Home page cards** (`README.md`) use in-game screenshots. Any contributor can provide these since they are just screenshots of the game.
- **All other section cards** use SVG icons from the existing pack in `.gitbook/assets/`. Do not use raster images for section cards outside the home.
- If a new SVG icon is needed that does not exist in the pack, **request it from FehDead** so it follows the established visual standard. Do not create or source your own SVG without asking first.

**Buttons** for outbound links (official mod pages, Discord):

```
<a href="https://..." class="button primary" target="_blank" data-icon="external-link-alt">Go to Official Mod Page</a>
```

**Content references** for internal cross-links. Use at the end of a section to point the reader to a related page: a tool or framework page links to its matching example, and a getting-started page links to the relevant tool or framework.

```
{% content-ref url="../examples/forge-modding-example.md" %}
[Link text](../examples/forge-modding-example.md)
{% endcontent-ref %}
```

**Navigation** lives in `SUMMARY.md`. Section pages are listed as a parent entry pointing to their `README.md` with child pages nested below, so the entry is both a clickable landing page and an expandable dropdown:

```
- [Tools](tools/README.md)
  - [VBF Browser](tools/vbf-browser.md)
  - ...
```

---

## 5. Sourcing and credits (mandatory)

This guide compiles work by many community creators and **never re-hosts their files**. Readers must always be sent to the creator's official page to download.

Therefore, **before creating any new tool, framework, or documentation page, ask the requester for the source:**

- What is the official page or link for this tool or framework? (Nexus Mods, the creator's site, etc.)
- Who created it, so credit is correct?

Do not write a page from assumptions or memory. If the requester cannot provide a source, flag it before proceeding. Every tool and framework page must link out to its official page via a button.

---

## 6. Quick checklist before finishing

- [ ] GitBook context confirmed (MCP or existing files), components used correctly.
- [ ] Text is clear, semantic, friendly, and free of filler.
- [ ] Process explained in followable steps for non-technical readers.
- [ ] No em-dashes anywhere.
- [ ] Page follows the established structure.
- [ ] Mod, tool, and framework names are never abbreviated and are identical across title, `SUMMARY.md`, card table, body, and links.
- [ ] Source link and credit confirmed with the requester and linked on the page.
- [ ] New page added to `SUMMARY.md` and its section card table.
