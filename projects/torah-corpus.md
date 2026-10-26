---
title: "Torah Corpus"
type: project
tags: [type/project, domain/torah-tech, domain/data-pipeline]
created: 2026-04-13
status: active
github: null
tech_stack: [Python, DuckDB, Parquet, Sefaria API, Otzaria]
people: [the author]
source_convs: [claude-code_torah-corpus]
---

## What It Is

A local-first Torah text corpus containing 4.88M+ segments across 7,015+ works. Ingests from multiple sources (Sefaria, MoreBooks, Otzaria, KSK) into a unified Parquet + DuckDB pipeline with full-text search over Hebrew. The text layer underneath [[sefer-graph]].

## Why It Exists

No single source has all Torah texts in a computationally accessible format. Sefaria covers ~6K works but misses many. Otzaria has additional texts but in different formats. Torah Corpus unifies them all into one queryable local database -- no network, no API costs, no rate limits. Primary data permanence.

> "primary data permanent, summaries temporary, invest in structural layer not more interpretation pipelines" (2026-04-10)

## Technical Stack

- **Storage:** Parquet files (segments_enriched_v2.parquet at 2GB+), DuckDB with FTS
- **Sources:** Sefaria API, MoreBooks, Otzaria (Sivan22/otzaria-library GitHub), KSK (37 volumes)
- **Pipeline:** Python scripts in `~/torah-corpus/scripts/`
- **FTS:** DuckDB full-text search index over Hebrew (~75s to build)
- **Catalog:** works_enriched_v2.parquet with metadata per work

## Key Numbers

- 4,883,763 segments (latest count)
- 7,015 works
- 6,549,483 citations (via [[sefer-graph]])
- 2,587M Hebrew characters
- 13 data sources, 14 categories
- By source: Sefaria 2.9M segs, MoreBooks 682K, Otzaria KSK 445K, Otzaria staging 402K

## Timeline

- **2025-H2:** Initial Sefaria ingestion. Core pipeline built.
- **2026-03:** MoreBooks and KSK ingestion. 4.25M segments.
- **2026-04 (early):** Otzaria staging ingest -- +302K segments / 77 works (Pninei Halakha, Pri Megadim, Yalkut Yosef, Reb Chaim, Reb Elchonon, Rav Kook, Sdei Chemed). Phase 4 scripts.
- **2026-04 (mid):** 4.88M segments, 7,015 works. DuckDB rebuilt with FTS.

## People Involved

- the author -- sole developer

## Which Frameworks It Implements

- [[primary-data-yesod]] -- the canonical example: primary text data is permanent
- [[orchestra-conductor]] -- orchestrating multiple data sources into one corpus
- [[seed-principles]] -- COMPRESSION (one database, all sources)

## Current Status

**Active.** Growing. Latest merge: 4.88M segments from 7,015 works. DuckDB FTS operational. Pipeline scripts ready for additional Otzaria staging directories.

## Related

- [[sefer-graph]] -- the citation/relationship layer built on top
- [[ohr-avraham-chaim]] -- Torah learning that uses this data
- [[sefaria-interview]] -- the Sefaria connection
- [[shelet-renderer]] -- cloud hosting for derived data
- [[torah-transcription]] -- audio transcription feeds into the corpus
- [[mcp-sefaria-server]] -- Sefaria API access for Torah texts
- [[rav-weinberger]] -- shiurim being transcribed for the corpus
- [[dyslexia]] -- the Torah corpus compensates for Hebrew reading difficulty
