---
title: "Supa-Brain"
type: project
tags: [type/project, domain/cognitive-architecture, domain/supabase]
created: 2026-04-13
status: active
github: null
tech_stack: [Supabase, PostgreSQL, Edge Functions, MCP]
people: [the author]
source_convs: [claude-code_355ef47f]
---

## What It Is

A Supabase-native MCP server variant of [[brain-mcp]]. 21 tools exposed via Supabase Edge Functions operating on a `brain.*` schema. Cloud-first complement to the local-first Brain MCP -- same cognitive prosthetic concept, different infrastructure.

## Why It Exists

Brain MCP runs locally (LanceDB + DuckDB). Supa-Brain runs in the cloud (Supabase). Different tradeoffs: local = fast, private, offline; cloud = accessible from anywhere, shared, integrated with other Supabase projects like [[shelet-renderer|Shelet]] and [[epicagents-viter|a workspace]].

## Technical Stack

- **Database:** Supabase PostgreSQL (`brain.*` schema)
- **Functions:** Supabase Edge Functions (Deno)
- **Protocol:** MCP server
- **Tools:** 21 exposed tools
- **Integration:** Part of the broader Shelet Supabase project

## Key Numbers

- 21 tools
- `brain.*` schema in Supabase
- Cloud-native complement to local Brain MCP

## Timeline

- **2025-H2:** Concept explored -- "why not use supabase mcp tools directly"
- **2026-Q1:** Schema designed and deployed. Edge functions built.
- **2026-04:** Part of Shelet Supabase ecosystem (16 schemas, ~108 tables).

## People Involved

- the author -- sole developer

## Which Frameworks It Implements

- [[monotropism-stack]] -- cloud variant of the cognitive prosthetic
- [[primary-data-yesod]] -- same primary data, different access pattern

## Current Status

**Active.** Running in Supabase alongside [[sefer-graph]] and client consulting work schemas. 21 tools operational.

## Related

- [[brain-mcp]] -- the local-first original
- [[shelet-renderer]] -- shared Supabase project
- [[brainmcp-dev]] -- documentation covers both variants
