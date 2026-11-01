---
name: a11y-help
description: "ADRenaline. Help: catalog of plugin-accessibility (skills, rules, commands)."
---

# Help — ADRenaline Accessibility

Print this catalog as the reply. Do not run any skill or command. Do not invent entries that are not listed. If a component was added to the plugin and is missing here, add one line from its frontmatter `description` and say the catalog was refreshed.

When this help command is the first command in the message, every command, skill, or rule named after it is the subject of the help. Do not run those names. Do not print the full catalog. For each name, in the order given, print its catalog line (the linked id and the sentence). When the README has a heading for that command, also print the paragraphs under that heading, up to the next heading. A skill name uses the skill's catalog line and the README group that names that skill, up to its first command heading. A name that is not in this catalog is one line: it is not in this plugin. Do not invent what it does, and do not write a file.

Write the sentences in the language of the request. Keep command names, file ids, and every URL unchanged. Every id is a markdown link to the GitHub URL on its line. Do not print a repository `name` as the visible label of a plugin.

Keep the section headings, in this order: Plugin, Commands, Skills, Rules, then Agents, Hooks, and MCP when the plugin has them, then Output, then Not in this plugin. The title and the Plugin line show `ADRenaline` plus the `displayName`, then one sentence on what the plugin does. Under Commands, group the lines by the skill named in the line. Each group opens with that skill name linked to its SKILL.md. One line per item: the linked id, then the sentence. Output links this plugin's GitHub repository under that same label. A plugin under Not in this plugin uses `ADRenaline` plus its short name, and links to `https://github.com/<owner>/<other-plugin>` only when that repository exists.

## Plugin

- [**ADRenaline Accessibility**](https://github.com/ADRenaline-Suite/plugin-accessibility/blob/main/README.md) — Audits a design or a built screen against WCAG 2.2, and writes the requirement before the screen is coded.

## Commands

- [**/a11y-help**](https://github.com/ADRenaline-Suite/plugin-accessibility/blob/main/README.md) — This help (one-line catalog of the plugin).
- [**audit-accessibility**](https://github.com/ADRenaline-Suite/plugin-accessibility/blob/main/skills/audit-accessibility/SKILL.md) — Audits a design or a built screen against WCAG 2.2 AA.
- [**/a11y-design**](https://github.com/ADRenaline-Suite/plugin-accessibility/blob/main/skills/audit-accessibility/references/design.md) — Design audit: the handoff or the mock, checked before code.
- [**/a11y-implementation**](https://github.com/ADRenaline-Suite/plugin-accessibility/blob/main/skills/audit-accessibility/references/implementation.md) — Implementation audit: a built screen, by URL or by screenshot.
- [**specify-accessibility**](https://github.com/ADRenaline-Suite/plugin-accessibility/blob/main/skills/specify-accessibility/SKILL.md) — Writes the accessibility requirement or the note a screen must meet before it is built.
- [**/a11y-requirements**](https://github.com/ADRenaline-Suite/plugin-accessibility/blob/main/skills/specify-accessibility/references/requirements.md) — Requirement: one WCAG 2.2 criterion this screen must meet, and how to tell.
- [**/a11y-notes**](https://github.com/ADRenaline-Suite/plugin-accessibility/blob/main/skills/specify-accessibility/references/notes.md) — Note: what the builder must keep (name, focus, contrast, target size).

## Skills

- [**audit-accessibility**](https://github.com/ADRenaline-Suite/plugin-accessibility/blob/main/skills/audit-accessibility/SKILL.md) — Audits a design or a built screen against WCAG 2.2 AA.
- [**specify-accessibility**](https://github.com/ADRenaline-Suite/plugin-accessibility/blob/main/skills/specify-accessibility/SKILL.md) — Writes the accessibility requirement or the note a screen must meet before it is built.

## Rules

- [**output-folder**](https://github.com/ADRenaline-Suite/plugin-accessibility/blob/main/rules/output-folder.mdc) — Every file goes in `adrenaline/accessibility/` (or in `outputDirs["plugin-accessibility"]` of `.cursor/adrenaline.json`). The artifact follows the language of the request.
- [**wcag-not-reinvented**](https://github.com/ADRenaline-Suite/plugin-accessibility/blob/main/rules/wcag-not-reinvented.mdc) — The norm is WCAG 2.2. A second language does not lower the target. The copy and the layout stay in their plugins.

## Output

- Repository: [**ADRenaline Accessibility**](https://github.com/ADRenaline-Suite/plugin-accessibility).
- Folder: `adrenaline/accessibility/`. One named subject goes in `<subject>/`. `<NNN>` is monotonic across the whole folder.

## Not in this plugin

- Interface copy → ADRenaline plugin-ux-writing.
- Layout → [**ADRenaline plugin-ui-ux-design**](https://github.com/ADRenaline-Suite/plugin-ui-ux-design).
- Test scenario → ADRenaline plugin-qa-engineer.
