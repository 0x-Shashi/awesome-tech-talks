# Boost AI Context with Hybrid Search in Spanner

**Speaker(s):** Jeff, Alexander, Girish · **Channel:** Google Cloud Tech · **Date:** 2026-06-25
**Watch:** https://youtu.be/gV5NEo8-LFI?si=Aefu2R44_9JamC8s · **Format:** Talk / Demo · **Level:** Intermediate
**Topics:** Backend/Infra, AI Agents

## TL;DR

A technical exploration of how Google Cloud Spanner's **Hybrid Search** delivers grounded, high-relevance context for AI agents. Combines lexical BM25 token matching with high-dimensional vector embeddings within single SQL statements, supported by Spanner's industry-leading 99.999% availability SLA and multi-model relational, graph, and search capabilities.

## Contents

- [Spanner as a foundational search and AI data platform](#spanner-as-a-foundational-search-and-ai-data-platform)
- [The power of Hybrid Search: BM25 keyword matching plus vector similarity](#the-power-of-hybrid-search-bm25-keyword-matching-plus-vector-similarity)
- [Enterprise search use cases: e-commerce, healthcare, and content management](#enterprise-search-use-cases-e-commerce-healthcare-and-content-management)
- [Integration with Gemini Enterprise Agent Platform](#integration-with-gemini-enterprise-agent-platform)

---

## Spanner as a foundational search and AI data platform

Cloud Spanner provides the core data infrastructure for Google's largest planetary services (Drive, Gmail, YouTube, Google Photos) and global platforms like Uber:
- **Zero-Maintenance Horizontal Scaling**: Shards compute and storage dynamically across global regions.
- **Five-Nines SLA (99.999%)**: Delivers consistent, highly available transactional performance.
- **Multi-Model Unification**: Eliminates synchronization lag by serving relational tables, graph structures (GQL), and vector indexes from a single unified dataset.

---

## The power of Hybrid Search: BM25 keyword matching plus vector similarity

Traditional search architectures force a compromise between precision and semantic comprehension:

```mermaid
flowchart TD
    Query[User Query: 'Replace gasket part #AB-102'] --> Lex[BM25 Full-Text Search\n Exact Part Number Match]
    Query --> Vec[Dense Vector Search\n Semantic Context & Synonyms]
    Lex & Vec --> RRF[Reciprocal Rank Fusion (RRF)\n Unified In-Database Scoring]
    RRF --> Out[Top Grounded Context Results for Agent]
```

- **BM25 Search**: Matches exact keywords, codes, part numbers, and proper nouns.
- **Vector Search**: Captures semantic intent, multilingual matches, and conceptual synonyms.
- **Reciprocal Rank Fusion (RRF)**: Computes a unified ranking directly within Spanner SQL queries, reducing agent latency and pipeline complexity.

---

## Enterprise search use cases: e-commerce, healthcare, and content management

- **E-Commerce Catalogs**: Combines typo-tolerant fuzzy text filtering with multimodal visual embeddings for instant product discovery.
- **Clinical Healthcare**: Cross-references exact pharmaceutical codes with semantic disease classifications across patient medical records.
- **Enterprise Content Systems**: Ingests millions of enterprise documents, allowing agents to execute grounded question-answering in milliseconds.

---

## Integration with Gemini Enterprise Agent Platform

Spanner exposes Hybrid Search directly to autonomous AI agents through **Model Context Protocol (MCP)** endpoints and BQML/SQL ML functions, eliminating the need to maintain external vector databases or brittle ETL synchronization code.

**Related:** [Power intelligent agents with AI-native databases](./ai-native-databases-agents-2026-2.md)

---

## Source

Full cleaned transcript: `DATA/videos/spanner-hybrid-search-context-2026-2.json`
Raw transcript: `RAW/videos/spanner-hybrid-search-context-2026-2.md`
