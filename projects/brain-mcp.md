---
title: "Brain MCP"
type: project
tags: [type/project, domain/cognitive-architecture, domain/open-source]
created: 2026-04-13
status: active
github: https://github.com/mordechaipotash/brain-mcp
tech_stack: [Python, LanceDB, DuckDB, MCP, JSONL, sentence-transformers]
people: [the author]
source_convs: [claude-code_3602c21d, claude-code_066c27a3]
---

## What It Is

A self-hosted MCP (Model Context Protocol) server that turns AI conversation history into a searchable, queryable second brain. Cognitive prosthetic tools preserve context across focus sessions for a [[monotropism|monotropic]] mind. Ingests conversations from [[clawdbot-steve|Clawdbot]], Claude Code, ChatGPT, or any JSONL source, embeds them locally via LanceDB, and exposes 25+ tools for search, synthesis, and cognitive recovery.

## Why It Exists

the author's monotropic focus means deep single-thread work, but switching between domains is expensive. Brain MCP acts as a prosthetic memory -- restoring context without re-reading hundreds of messages. It emerged from the [[cognitive-genome]] project and the realization that 339K+ messages of conversation history represent genuine intellectual capital that was otherwise lost between sessions.

> "The user wants to search their 'brain' -- this is a monotropic prosthetic system with 267K conversation messages and 55K embedded messages." (2025-12)

## Technical Stack

- **Core:** Python MCP server (`brain_mcp/`)
- **Embeddings:** sentence-transformers, 138K vectors in LanceDB (494MB, replaced 3GB DuckDB)
- **Storage:** JSONL ingestion pipeline, DuckDB for analytics
- **Tools:** 25+ MCP tools -- semantic search, tunnel state, context recovery, thinking trajectory, cognitive patterns
- **Sync:** Hourly LaunchAgent + daily briefing at 6am
- **Distribution:** PyPI v0.2.1 (`open-brain-mcp`)

## Key Numbers

- 339K+ total messages ingested
- 138K embedded vectors (87.3% coverage)
- 25+ MCP tools exposed
- 41 GitHub stars (top repo by far)
- 494MB LanceDB (down from 3GB DuckDB)
- PyPI: v0.2.1

## Timeline

- **2025-Q4:** Genesis as part of [[cognitive-genome]] project. First embeddings, keyword search.
- **2025-12:** 267K messages, 55K embedded. Core prosthetic tools (tunnel_state, context_recovery) built.
- **2026-01:** Efficiency overhaul -- migrated from DuckDB to LanceDB. Fixed 2x con.close() bugs.
- **2026-02:** 376K messages, 118K vectors. Published to PyPI. 31 active tools.
- **2026-03:** Open-sourced as `open-brain-mcp`. README rewritten. 39 stars.
- **2026-04:** 41 stars. 138K embeddings. Ongoing refinement.

## People Involved

- the author -- sole developer

## Which Frameworks It Implements

- [[seed-principles]] -- COMPRESSION (say more with less), BOTTLENECK (monotropic superpower)
- [[monotropism-stack]] -- the flagship implementation of the concept
- [[tom-prosthetic]] -- Brain MCP IS the literal cognitive prosthetic (context recovery, tunnel state)
- [[orchestra-conductor]] -- 100% human control, 100% machine execution
- [[primary-data-yesod]] -- primary data permanent, summaries temporary

## Current Status

**Active.** The core system. Used daily via [[clawdbot-steve|Steve]] and Claude Code. 41 GitHub stars and growing. PyPI published. Open-source docs at [[brainmcp-dev]].

## Related

- [[brainmcp-dev]] -- documentation site
- [[brain-canvas]] -- terminal UI for Brain
- [[supa-brain]] -- Supabase-native variant
- [[cognitive-genome]] -- mining agents that feed into Brain
- an AI familiar -- primary consumer of Brain tools
- [[steve-ai]] -- the AI familiar powered by Brain
- [[nir-hemo]] -- potential co-builder (RepoWise + Brain = complete cognitive prosthetic)
- [[yam-peleg]] -- Clawders community where Brain was demoed
- [[poly-wiki]] -- curated interpretation layer built from Brain data
