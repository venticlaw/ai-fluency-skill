# Privacy Policy

**Plugin:** ai-fluency
**Maintainer:** venticlaw (josh@buildingourtech.org)
**Last updated:** 2026-04-22

## Summary

The `ai-fluency` plugin is a single Markdown skill file (`skills/ai-fluency/SKILL.md`) loaded into Claude Code to guide how Claude reasons about and produces outputs. **It does not collect, store, transmit, or process any personal data.**

## What the plugin does

- Adds one skill definition (a Markdown file with YAML frontmatter) to your Claude Code installation.
- Influences Claude's internal reasoning when you invoke `/ai-fluency` or when Claude auto-selects the skill based on task description.

## What the plugin does not do

- **No network calls.** The plugin ships no code, no hooks, no MCP servers, no background processes. It cannot make HTTP requests, read files, or execute commands on its own.
- **No data collection.** It does not log your prompts, outputs, file contents, environment variables, credentials, or any other information.
- **No telemetry.** Nothing is reported back to the maintainer or any third party.
- **No third-party services.** The plugin itself does not integrate with, send data to, or receive data from any external service.

## Data handled by Claude Code itself

When you use this plugin, your interaction with Claude Code is still governed by Anthropic's own privacy terms, which apply to any input you send to Claude regardless of whether this plugin is installed:

- [Anthropic Privacy Policy](https://www.anthropic.com/legal/privacy)
- [Claude Code usage terms](https://www.anthropic.com/legal/consumer-terms)

The plugin does not alter, expand, or reduce what Anthropic receives or processes.

## Installation and updates

Installing the plugin copies the skill file from this GitHub repository to your local Claude Code configuration directory. GitHub's own privacy terms apply to the act of cloning or fetching the repository; see [GitHub's Privacy Statement](https://docs.github.com/en/site-policy/privacy-policies/github-general-privacy-statement).

## Changes to this policy

If the plugin ever begins to collect or transmit data — for example, if future versions add hooks, scripts, or MCP servers — this document will be updated before that version is published, and the change will be reflected in the git history of this repository.

## Contact

Questions about this policy: josh@buildingourtech.org
