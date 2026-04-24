---
title: "Sefer-Graph"
type: project
tags: [type/project, domain/torah-tech, domain/knowledge-graph]
created: 2026-04-13
status: active
github: https://github.com/mordechaipotash/sefer-graph
tech_stack: [Supabase, PostgreSQL, Python, DuckDB, Claude AI]
people: [the author]
source_convs: [claude-code_28863c52, claude-code_36c6876b]
---

## What It Is

A Torah citation knowledge graph. Maps the web of references between sefarim (Torah texts) -- who cites whom, what depends on what, how ideas flow across centuries. Extracts citations from primary texts using AI, stores them in a Supabase schema (`sefer.*`), and builds a navigable graph of Torah intellectual history.

## Why It Exists

Torah literature is a vast interconnected web of citations spanning 3,000+ years. No existing tool maps these connections computationally. Sefer-Graph makes the implicit citation network explicit -- enabling search, analysis, and discovery across the entire corpus. Built from the [[torah-corpus]] as the relationship layer on top of the text layer.

## Technical Stack

- **Database:** Supabase PostgreSQL (`sefer.*` schema) + local DuckDB
- **Extraction:** Claude AI for citation identification and classification
- **Citation types:** explicit_talmud, explicit_verse, conceptual_dependency, back_reference, named_author, named_position, explicit_mishnah
- **Pipeline:** Python extraction scripts, batch processing per sefer
- **Confidence scoring:** High (>=0.9), Medium (0.7-0.9), Low (<0.7)

## Key Numbers

- 4.5M+ citations (latest: 4,529,877 connecting 731K sources to 354K targets)
- 28+ sefarim processed
- Average confidence: 0.877
- 2.2M citations in Supabase (largest table in [[shelet-renderer|Shelet]] project)
- Top types: explicit_talmud (965K), explicit_verse (649K), conceptual_dependency (636K)
- 1 GitHub star

## Timeline

- **2026-03:** Initial extraction pipeline. First sefarim processed.
- **2026-04-05/06:** Deep session -- fixed tools (timeout 3s->10s, stats_cache), closed pipeline, processed 7 sefarim, Bavli+Bartenura extracting, normalization pass, dead end analysis.
- **2026-04:** Scaled to 4.5M+ citations. 28 sefarim. Ongoing extraction.

## People Involved

- the author -- sole developer

## Which Frameworks It Implements

- [[primary-data-yesod]] -- primary citation data is permanent; interpretations are temporary
- [[orchestra-conductor]] -- human directs which sefarim to process, AI does the extraction
- [[seed-principles]] -- SEEDS transfer thinking; citations transfer Torah

## Current Status

**Active.** Pipeline running. 4.5M+ citations extracted. Ongoing expansion to more sefarim. Integrated with [[shelet-renderer|Shelet]] Supabase project (sefer.citations = 2.2M rows in cloud).

## Related

- [[torah-corpus]] -- the text layer that Sefer-Graph builds on
- [[shelet-renderer]] -- Supabase host for the citation data
- [[ohr-avraham-chaim]] -- Torah learning pipeline
- [[sefaria-interview]] -- Sefaria's citation work was the inspiration
