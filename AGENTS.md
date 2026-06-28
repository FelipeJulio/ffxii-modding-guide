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

Keep all pages consistent. Do not invent new layouts. The established structure for a **tool or framework** page is:

1. `# Title` (the full, correct product name).
2. A single bold sentence stating what it is.
3. `### What does it do?` with a short explanation and a bullet list of capabilities.
4. One or more GitBook `hint` blocks for features, requirements, warnings, and the official link.
5. Where relevant, a `content-ref` linking to a matching example or guide.

**Section landing pages** (`README.md` inside each folder) open with a `# Title`, one or two sentences of intro, then a `card` table listing the pages in that section.

**Example and guide titles always use an action format** that states what the reader will accomplish: "Creating X with Y" or "Doing X with Y" (for example, "Creating a Map Announcer Mod with the Lua Loader", "Creating a Custom NPC with the FF12 VM Script Decompiler"). Never use a vague or generic title like "Lua Modding Example". The reader should know the concrete outcome and the main tool involved just from the title.

**Never abbreviate the name of a mod, tool, or framework. Always use its full, official name**, everywhere it appears: page titles, `SUMMARY.md`, card tables, body text, and links. The name must be identical in all of these places for the same item. For example, always write "The Insurgent's Stat Lores", never "Stat Lores"; "The Insurgent's Forge", never "the Forge".

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

**Buttons** for outbound links (official mod pages, Discord):

```
<a href="https://..." class="button primary" data-icon="external-link-alt">Go to Official Mod Page</a>
```

**Content references** for internal cross-links:

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
