# Updating and Versioning Your Mod

Publishing your mod is not the end of the journey. Most mods keep evolving: you fix bugs, add features, or update them to stay compatible with newer tools. Handling these updates in a clear, predictable way makes life easier for your players and for any modder who depends on your work.

## Use Semantic Versioning

Every release of your mod should have a version number, and the community standard is **Semantic Versioning** (SemVer). A SemVer number has three parts: `MAJOR.MINOR.PATCH` (for example, `1.4.2`).

You increase one of these numbers depending on what changed:

- **MAJOR** (`2.0.0`): you made an incompatible change. Old setups, saves, or mods that depended on the previous version may break.
- **MINOR** (`1.5.0`): you added new features, but everything from the previous version still works.
- **PATCH** (`1.4.3`): you only fixed bugs or made small corrections, with no new features and nothing broken.

A quick way to think about it: start at `1.0.0` for your first stable release, then bump the part that matches the kind of change you made.

{% hint style="info" %}
This is only a short summary. To understand the full set of rules, read the official specification at [semver.org](https://semver.org/).
{% endhint %}

## Always Write a Changelog

Whenever you release a new version, tell your players what changed. A **changelog** is a simple list of changes for each version, newest at the top. It helps people decide whether to update and makes troubleshooting much easier.

Keep each entry short and grouped by the type of change. For example:

```text
## 1.4.0
- Added: support for custom weapon icons.
- Fixed: crash when loading a save created in version 1.2.0.
- Changed: default config now disables debug logging.

## 1.3.1
- Fixed: typo in the Italian description file.
```

Good changelog habits:

- Write it for players, not for yourself. Describe the effect, not the internal code change.
- Always note anything that breaks compatibility, clearly and near the top.
- Keep the version number in the changelog identical to the one on your mod page.

## Best Practices for Updates

- **Keep your version numbers in sync** across your mod page, your changelog, and any version field inside the mod itself.
- **Call out breaking changes loudly.** If players must delete an old version, update a dependency, or start a new save, say so before they install.
- **State your dependencies and their versions.** If your mod now requires a newer External File Loader or Lua Loader, list the minimum version it needs.
- **Do not silently overwrite.** When you upload a new build, publish it as a new version with its own changelog entry instead of replacing the file with no explanation.
- **Test before you publish.** Make sure the update installs cleanly on top of, or in place of, the previous version the way your players will actually do it.
