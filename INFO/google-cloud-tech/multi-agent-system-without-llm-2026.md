# How to Design a Multi-Agent System That Skips the LLM

**Speaker(s):** Casey West, Annie Wang · **Channel:** Google Cloud Tech · **Date:** 2026-06-06
**Watch:** https://youtu.be/Fzd0BWMH65s?si=bKyJ75VM6jfjKbCT · **Format:** Talk / Architecture Deep Dive · **Level:** Advanced
**Topics:** AI Agents, Backend/Infra, AI Coding Tools

## TL;DR

An architectural deep dive into **Race Condition**, a 1,000-agent marathon simulation built on Google's Agent Development Kit (ADK) where almost none of the agents invoke an LLM. Casey West explains how to balance LLM creativity against deterministic code, using the `before_model_callback` hook to bypass model inference entirely, solving NP-hard route planning with the Spine & Sprout algorithm, and maintaining 1,000 concurrent runner states in Redis.

## Contents

- [The core architectural dilemma: LLM reasoning vs. deterministic code](#the-core-architectural-dilemma-llm-reasoning-vs-deterministic-code)
- [The before_model_callback technique: keep the agent, skip the model](#the-before_model_callback-technique-keep-the-agent-skip-the-model)
- [Deterministic pathfinding: NP-hard route planning and the Spine & Sprout algorithm](#deterministic-pathfinding-np-hard-route-planning-and-the-spine-sprout-algorithm)
- [Scaling 1,000 stateless agent sessions with Redis](#scaling-1000-stateless-agent-sessions-with-redis)

---

## The core architectural dilemma: LLM reasoning vs. deterministic code

A common architectural failure in agent development is forcing every state transition and mathematical computation through generative models.

In the **Race Condition** simulation:
- **LLM Workload**: Persona generation (runner name, backstory, training history) and course milestone narrative descriptions.
- **Deterministic Workload**: Physics simulation, GPS coordinate calculation, pacing splits, heart rate degradation, and hydration decay.
- **Result**: Routing physics calculations to deterministic algorithms saved millions of tokens, reduced execution latency from seconds to microseconds, and avoided non-deterministic calculation hallucinations.

```mermaid
flowchart TD
    Task[Agent Simulation Event] --> Check{Is Action Mathematical / Algorithmic?}
    Check -->|Yes| Fast[Deterministic Python Code\n before_model_callback]
    Check -->|No: Creative / Linguistic| LLM[Gemini Model Inference]
    Fast --> Out[Instant Structured State Update (0 Tokens)]
    LLM --> Out
```

---

## The before_model_callback technique: keep the agent, skip the model

The Google Agent Development Kit (ADK) includes a powerful hook: `before_model_callback`.

```python
def before_model_callback(agent_context, session_state):
    if session_state.is_autopilot_tick():
        # Compute runner physics deterministically
        updated_state = calculate_runner_physics(session_state)
        # Short-circuit execution: return result immediately without calling LLM
        return ShortCircuitResponse(updated_state)
    return None  # Fall through to LLM reasoning
```

This pattern preserves all agent routing, session tracking, and tool registry advantages of ADK while skipping token costs and model latency when deterministic logic suffices.

---

## Deterministic pathfinding: NP-hard route planning and the Spine & Sprout algorithm

Plotting an exact 26.2-mile marathon course through designated urban waypoints is an NP-hard graph problem:
1. **High-Level Agent**: LLM selects cultural landmarks and road themes.
2. **Spine & Sprout Algorithm**: Mathematical graph algorithm creates a central route spine and generates deterministic detour sprouts until the exact 26.2-mile distance constraint is satisfied.

---

## Scaling 1,000 stateless agent sessions with Redis

- Decouples agent runner loops from local container memory.
- All 1,000 runner agents persist state snapshots (coordinates, pace, energy) in **Redis**.
- Background worker processes pull state, execute deterministic physics ticks, and broadcast real-time updates via WebSockets with minimal CPU overhead.

**Related:** [Build a multi-agent system | Hands On AI (Part 1)](./hands-on-multi-agent-part1-2026.md)

---

## Source

Full cleaned transcript: `DATA/videos/multi-agent-system-without-llm-2026.json`
Raw transcript: `RAW/videos/multi-agent-system-without-llm-2026.md`
