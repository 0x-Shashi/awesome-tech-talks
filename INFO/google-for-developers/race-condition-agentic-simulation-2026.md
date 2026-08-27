# Fireside chat on an agentic simulation: Race Condition

**Speaker(s):** Tom Greenaway, Casey West - **Channel:** Google for Developers - **Date:** 2026-04-24
**Watch:** https://youtu.be/WYPdz3OZfuQ?si=bB7MJSEG80CFE9Pg - **Format:** Fireside Chat - **Level:** Intermediate
**Topics:** AI Agents - Backend/Infra - AI Coding Tools

## TL;DR

Tom Greenaway and Casey West discuss Race Condition, an open-source reference architecture for high-scale agentic simulations built for the Google Cloud Next developer keynote. They explain how multiplayer game loops, the Agent-to-Agent (A2A) protocol, GKE-hosted open-weight Gemma 4 models (via vLLM), Google Cloud Pub/Sub message buses, and Model Context Protocol (MCP) security controls enable massive concurrent agent orchestration.

## Contents

- [Race Condition overview: reference architecture for agentic simulations](#race-condition-overview-reference-architecture-for-agentic-simulations)
- [Core components of an agent: model, instructions, and tools](#core-components-of-an-agent-model-instructions-and-tools)
- [Multi-agent communication: A2A protocol, Agent Cards, and Message Bus](#multi-agent-communication-a2a-protocol-agent-cards-and-message-bus)
- [Game development patterns in agentic distributed architectures](#game-development-patterns-in-agentic-distributed-architectures)
- [Hybrid scaling: deterministic agents vs. open-weight Gemma 4 models](#hybrid-scaling-deterministic-agents-vs-open-weight-gemma-4-models)
- [Context management and subagent token optimization](#context-management-and-subagent-token-optimization)
- [Enterprise agent security: Agent Gateway, Identity, and MCP permissions](#enterprise-agent-security-agent-gateway-identity-and-mcp-permissions)

## Race Condition overview: reference architecture for agentic simulations

Race Condition is an open-source simulation demonstrating large-scale multi-agent coordination by simulating a full marathon along the Las Vegas Strip.
- **Frontend client**: 3D visualization of the Las Vegas Strip running in the browser.
- **Backend harness**: Distributed agent services orchestrated across the **Gemini Enterprise Agent Platform**.
- **Reference architecture**: Designed to provide enterprise developers with production-tested blueprints for high-throughput, multi-agent systems.

## Core components of an agent: model, instructions, and tools

The architecture leverages the **Agent Development Kit (ADK)**, where every agent is defined by three primitives:
1. **Model**: Neural network backend generating reasoning and actions (Gemini or Gemma).
2. **Instructions**: System prompts establishing operational boundaries, goals, and behavioral personas.
3. **Tools**: Executable integrations enabling interactions with databases, APIs, and simulation state.

**Agent roles in Race Condition:**
- **Planner Agent**: Synthesizes municipal constraints (traffic impact, legal rules) and calculates marathon routing.
- **Simulator Agent**: Coordinates sampling frequency, time steps, and event loops.
- **Runner Agents**: Model individual marathon participants navigating the course.

## Multi-agent communication: A2A protocol, Agent Cards, and Message Bus

- **Agent-to-Agent (A2A) Protocol**: Standardized communication layer where agents discover capabilities via machine-readable **Agent Cards** published to an **Agent Registry**.
- **Message Bus Pattern**: To prevent HTTP connection saturation during high-frequency simulation ticks, state updates stream across **Google Cloud Pub/Sub** and **Cloud Memorystore (managed Redis)**, broadcasting real-time agent telemetry to the frontend client.

`mermaid
flowchart TD
  P[Planner Agent / Simulator] -->|Pub/Sub Message Bus| MB[Cloud Pub/Sub + Redis]
  MB -->|Real-time Telemetry Stream| C[3D Visualization Client]
  R1[Runner Agent 1: Gemma 4 / GKE] -->|State Updates| MB
  R2[Runner Agent 2: Deterministic ADK] -->|State Updates| MB
  REG[Agent Registry / A2A Protocol] -.->|Agent Cards| P
`

## Game development patterns in agentic distributed architectures

- **Authoritative server state**: The backend server controls the primary game loop, executing simulation ticks every 5 to 10 seconds.
- **Client-triggered interrupts**: The frontend detects spatial events (e.g., runners colliding with 3D water station replenishment spheres) and emits interrupt payloads back to the backend.
- **Dual interaction formats**: Agents parse natural-language instructions or structured JSON payloads interchangeably.

## Hybrid scaling: deterministic agents vs. open-weight Gemma 4 models

Scaling thousands of agent interactions simultaneously introduces token cost and latency challenges. The team implemented a hybrid strategy:

| Agent Mode | Brain Implementation | Use Case | Performance / Cost Profile |
|---|---|---|---|
| **Deterministic ADK** | Rule-based code without LLM | High-volume baseline traffic | Sub-millisecond latency, zero token cost |
| **Private Inference LLM** | Open-weight **Gemma 4** on GKE (vLLM) | Emergent behavior, internal thoughts, decisions | Fixed infrastructure cost, high throughput |

## Context management and subagent token optimization

Accumulating full conversation histories causes token bloat and response latency:
- **Subagent context isolation**: Runner agents receive only immediate environmental state (current mile, fatigue level, nearest water point) without historical baggage.
- **History compaction**: Long-running simulations periodically compact past session logs into compact summaries, keeping token windows small and predictable.

## Enterprise agent security: Agent Gateway, Identity, and MCP permissions

- **Agent Identity**: Every agent is assigned a unique cryptographic principal within Google Cloud.
- **Agent Gateway**: Enforces network-layer access policies on **Model Context Protocol (MCP)** tool endpoints. For example, a planner agent can query read-only municipal data without possessing credentials to invoke budget-altering tools on connected enterprise backends.

## Source

Full cleaned transcript: DATA/videos/race-condition-agentic-simulation-2026.json
Raw transcript: RAW/videos/race-condition-agentic-simulation-2026.md
