---
title: "MCP Sefaria Server"
type: project
tags: [type/project, domain/torah, domain/open-source]
created: 2026-04-13
status: active
github: https://github.com/mordechaipotash/mcp-sefaria-server
tech_stack: [MCP, Sefaria API, TypeScript]
people: [the author]
source_convs: ["chatgpt/2025-06", "chatgpt/2025-09"]
---

## What It Is

An MCP (Model Context Protocol) server wrapping the Sefaria API, providing AI assistants with direct access to the Jewish text library. Search texts, retrieve passages, explore commentaries -- all through MCP tool calls.

> "please research how to use the sefaria api or alt fix the sefaria mcp"
> -- the author, 2025-12

## Why It Exists

the author doesn't separate Torah from tech. When learning Torah with AI (via [[clawdbot-steve|Steve]] or Claude Code), he needs direct access to source texts. Instead of copy-pasting from Sefaria.org, the MCP server lets the AI pull texts natively.

> "use sefaria mcp"
> -- the author (used repeatedly across sessions, 2025-06 onward)

> "first thing is get to know the sefaria mcp and the sefaria api very well"
> -- the author, 2026-01

## Usage Pattern

the author uses `mcp__sefaria__*` tools during Torah learning sessions, especially in the `#ohr-avraham-chaim` Discord channel. The server is referenced in Claude Desktop MCP configuration and in an AI familiar's cron job `sefaria-followup`.

## Technical

- Access Jewish texts through the Sefaria API
- Search texts, retrieve passages, explore commentaries
- Configured in `~/.claude/mcp.json`
- Part of the [[sefaria-interview]] preparation work (the author applied to Sefaria as AI Engineer)

## Related

- [[torah-corpus]] -- The larger Torah text project
- [[sefer-graph]] -- Graph relationships between sefarim
- [[ohr-avraham-chaim]] -- Torah community project
- [[sefaria-interview]] -- Sefaria AI Engineer application
- an AI familiar -- Primary consumer via sefaria-followup cron
