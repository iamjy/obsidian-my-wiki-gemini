# LLM Wiki Schema & Guidelines (GEMINI.md)

This document defines the structure and operational rules for this Obsidian-based Second Brain, managed by Gemini.

## Project Overview
This is a "Second Brain" vault following the **LLM Wiki** pattern. Unlike traditional RAG, this system builds a persistent, compounding synthesis of knowledge in the form of interlinked Markdown files.

## Note Types & Routing
- **concept**: Core ideas, entities, or synthesized topics. → `concepts/`
- **ingest**: Processed summaries and takeaways from external sources. → `ingests/`
- **log**: Chronological record of vault activities. → `logs/`
- **reference**: Bibliographic data or raw source metadata. → `references/`
- **project**: Active goals or specific implementation tasks. → `projects/`

## Frontmatter Schema
All notes must include the following YAML frontmatter:
```yaml
---
title: "Note Title"
date: YYYY-MM-DD
tags: [tag1, tag2]
type: concept | ingest | log | reference | project
status: draft | active | complete | stale
source: "Source URL or Reference Link"
related: ["[[link1]]", "[[link2]]"]
---
```

## Conventions
- **Link Style**: Use `[[wikilink]]` for all internal connections.
- **Naming Rules**: 
  - All filenames must be `kebab-case.md`.
  - Ingest notes must be prefixed with the date: `YYYY-MM-DD-slug.md`.
- **Source Material**: Sources are treated as immutable. The wiki is a persistent synthesis.

## Operations
- **Ingest**: Process a new source into a note in `ingests/`, update `index.md`, and link to related concepts.
- **Query**: Synthesize answers from existing wiki pages and file them back as new notes if valuable.
- **Lint**: Periodically check for contradictions and orphan pages.

## Key Files
- `GEMINI.md`: This schema definition.
- `index.md`: Content-oriented catalog of all notes.
- `logs/log.md`: Chronological activity log.
- `llm-wiki.md`: The original design document.

## Usage
Gemini (the agent) maintains this vault. The user provides sources and asks questions. The agent ensures the wiki remains structured and interlinked.
