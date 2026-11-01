<p align="right">Language:&emsp;<img alt="English" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-en-on.svg" align="middle" style="vertical-align:middle"> <a href="README.es.md" style="vertical-align:middle"><img alt="Español" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-es-off.svg" align="middle" style="vertical-align:middle"></a></p>

# Accessibility (`plugin-accessibility`)

Audits a design or a built screen against WCAG 2.2, and writes the requirement before the screen is coded. The target is AA unless the product set another.

The instructions are in English. The file the plugin saves follows the language of the request. Files go in `adrenaline/accessibility/`.

## /a11y-design

The handoff or the mock, checked before code. A missing contrast note stays a gap.

## /a11y-implementation

A URL or a screenshot. An automated scan is a hint, not conformance.

## /a11y-requirements

One WCAG 2.2 criterion and what a pass looks like.

## /a11y-notes

The name, the focus, the contrast, and the target size the builder must keep.

## Help

## /a11y-help

The catalog of this plugin. It does not write a file.

## Who it is for

Someone who needs a check a builder can meet. The words stay with `plugin-ux-writing`. The layout stays with `plugin-ui-ux-design`. The test scenario stays with `plugin-qa-engineer`. This plugin does not copy their skills.

## What it includes

Portable, for any agent that follows [Agent Skills](https://agentskills.io/specification):

- `audit-accessibility` audits a design or a built screen.
- `specify-accessibility` writes the requirement and the note the builder must keep.

Cursor and Claude Code: the commands above. In Cursor, `/a11y-design`. In Claude Code, `/plugin-accessibility:a11y-design`.

Cursor only: rules `output-folder`, `wcag-not-reinvented`. Claude Code does not load rules. The same restrictions are in the skills.

## Install

In Cursor, install the plugin from this repository in Customize.

In Claude Code:

```text
claude plugin marketplace add ADRenaline-Suite/plugin-accessibility
claude plugin install plugin-accessibility@plugin-accessibility
```

To try a local copy, start Claude Code with `claude --plugin-dir <path to this repository>`.

## Example

Ask `/a11y-implementation` and give a URL. The file cites the criterion that fails. A second language that was not checked stays a gap.

## Configuration

Files go in `adrenaline/accessibility/`. One named screen goes in `<subject>/`. The target is WCAG 2.2 AA unless the product set another.

## License

MIT. Copyright (c) 2026 Ricardo Plascencia.

