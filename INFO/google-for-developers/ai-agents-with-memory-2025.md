# How to build AI agents with memory

**Speaker(s):** Sita Lakshmi Sangameswaran, Kimberly Milam - **Channel:** Google for Developers - **Date:** 2025-10-07
**Watch:** https://youtu.be/sMtrelDNxIc?si=l8-wTWgukhgLfbQ_ - **Format:** Talk - **Level:** Intermediate
**Topics:** AI Agents - Backend/Infra - Prompt Engineering

## TL;DR

Kimberly Milam (Tech Lead for Vertex AI Memory Bank) and Sita Lakshmi Sangameswaran present the end-to-end architecture for building persistent memory into AI agents using Google's Agent Development Kit (ADK) and Vertex AI Memory Bank. They cover asynchronous background fact extraction, automated memory consolidation, retrieval mechanisms (preload vs. on-demand tool calls), custom topic filtering, and granular Time-to-Live (TTL) lifecycle policies.

## Contents

- [The problem of forgetful agents: volatile vs. persistent memory](#the-problem-of-forgetful-agents-volatile-vs-persistent-memory)
- [ADK memory architecture: BaseMemoryService, InMemory, and Memory Bank](#adk-memory-architecture-basememoryservice-inmemory-and-memory-bank)
- [Memory lifecycle: background extraction and automatic consolidation](#memory-lifecycle-background-extraction-and-automatic-consolidation)
- [Retrieval patterns: Preload Memory Tool vs. Load Memory Tool vs. Callbacks](#retrieval-patterns-preload-memory-tool-vs-load-memory-tool-vs-callbacks)
- [Custom memory extraction: managed topics vs. custom business topics](#custom-memory-extraction-managed-topics-vs-custom-business-topics)
- [Memory governance: Time-to-Live (TTL) and lifecycle management](#memory-governance-time-to-live-ttl-and-lifecycle-management)

## The problem of forgetful agents: volatile vs. persistent memory

Stateless agents that re-request basic user facts inflate token costs and frustrate end users:
- **Volatile in-memory sessions**: Persist turn-by-turn dialogue strictly within active process memory on a local VM. Context vanishes upon server restart.
- **Persistent managed memory**: Stores curated facts across independent conversation sessions, dramatically reducing token usage on long-term user interactions.

## ADK memory architecture: BaseMemoryService, InMemory, and Memory Bank

The ADK abstracts memory orchestration via BaseMemoryService:

| Method | Purpose |
|---|---|
| dd_session_to_memory | Ingests completed conversation sessions, extracts key facts, and persists them |
| search_memory | Performs semantic similarity search over stored user memories using an isolation scope |

- **InMemoryMemoryService**: Local dictionary storage of raw turns; intended strictly for local development and unit testing.
- **Vertex AI Memory Bank**: Managed cloud service that chains LLM calls (e.g., Gemini 2.5 Flash) asynchronously in the background to distill, consolidate, and index semantic facts without blocking user-facing inference.

## Memory lifecycle: background extraction and automatic consolidation

`mermaid
flowchart TD
  S[Raw Session Turns] -->|Async Non-Blocking Call| E[LLM Fact Extraction
Filters Out Chit-Chat]
  E --> C{Consolidation Engine}
  C -->|Duplicate Fact| D[Deduplicate / Update Existing Memory]
  C -->|Complementary Fact| M[Merge & Evolve Stored Context]
  C -->|New Fact| N[Store New Scoped Memory Record]
  D --> MB[(Vertex AI Memory Bank)]
  M --> MB
  N --> MB
`

1. **Extraction**: Background Gemini chains evaluate conversation turns against topic definitions, isolating meaningful facts while discarding conversational filler.
2. **Consolidation**: Compares newly extracted facts against existing memory vectors. Redundant items are deduplicated and related facts are synthesized into unified records.

## Retrieval patterns: Preload Memory Tool vs. Load Memory Tool vs. Callbacks

Developers can choose how agents access stored facts:
- **Preload Memory Tool**: Injects relevant memories deterministically into system instructions prior to agent execution.
- **Load Memory Tool**: An explicit function tool that the LLM invokes on demand only when historical context is required.
- **Custom Callbacks**: Custom pre-execution hooks using the Agent Engine SDK for fine-grained control over similarity search thresholds and prompt formatting.

## Custom memory extraction: managed topics vs. custom business topics

- **Managed Topics**: Out-of-the-box extraction categories (personal profile, user preferences, explicit remember/forget commands, key task outcomes).
- **Custom Topics**: Developers define domain-specific labels, descriptions, and few-shot examples (e.g., extracting structured retail product feedback while ignoring unrelated banter).

## Memory governance: Time-to-Live (TTL) and lifecycle management

Memory Bank supports comprehensive retention policies:
- **Global Default TTL**: Automatically assigns expiration timestamps (e.g., 30 days) to all generated memories.
- **Granular Operational TTL**: Enforces TTL timers strictly upon memory creation, preventing background consolidation updates from inadvertently extending retention windows beyond regulatory compliance limits.

## Source

Full cleaned transcript: DATA/videos/ai-agents-with-memory-2025.json
Raw transcript: RAW/videos/ai-agents-with-memory-2025.md
