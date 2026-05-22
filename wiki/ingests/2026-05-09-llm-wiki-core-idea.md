---
title: "LLM Wiki Core Idea: Persistent Synthesis vs RAG"
date: 2026-05-09
tags: [architecture, llm, rag, wiki]
type: ingest
status: complete
source: "llm-wiki.md"
related: ["[[index]]"]
---

# LLM Wiki Core Idea: Persistent Synthesis vs RAG

The core differentiator of the LLM Wiki pattern is the shift from ephemeral retrieval (RAG) to **persistent, compounding synthesis**.

## Summary
Most RAG systems rediscover knowledge from scratch on every question. The LLM Wiki pattern builds a structured, interlinked collection of markdown files that sits between the user and raw sources.

## Key Insights
- **No Rediscovery**: Knowledge is compiled once and kept current, not re-derived on every query.
- **Persistent Artifact**: The wiki is a persistent, compounding artifact where cross-references and contradictions are already flagged.
- **LLM as Maintainer**: The LLM does the grunt work of summarizing, cross-referencing, and bookkeeping.
