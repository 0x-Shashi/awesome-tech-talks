# Agents, AI & The Next Wave: Mike Clark on Vertex AI at DevFest Silicon Valley

**Speaker(s):** Frank van Puffelen, Mike Clark - **Channel:** Google for Developers - **Date:** 2025-11-21
**Watch:** https://youtu.be/9oYHU1hdDog?si=6tJa6SYQq0apwmL6 - **Format:** Fireside Chat - **Level:** Intermediate
**Topics:** AI Agents - Backend/Infra - AI Coding Tools

## TL;DR

Mike Clark (Google Director of Product Management, AI Agents) and Frank van Puffelen discuss transitioning AI agents from experimental demos to production environments using Vertex AI Agent Builder, Agent Engine, and the open-source Agent Development Kit (ADK). They explore the Build-Scale-Govern lifecycle, outcome-based software evaluation, and open protocols (A2A, A2UI, A2P) contributed to the Linux Foundation.

## Contents

- [DevFest energy and the democratizing reset of AI](#devfest-energy-and-the-democratizing-reset-of-ai)
- [Shifting from syntax mastery to creative intent and business outcomes](#shifting-from-syntax-mastery-to-creative-intent-and-business-outcomes)
- [Rethinking code quality: outcome-driven evaluation vs. traditional PRs](#rethinking-code-quality-outcome-driven-evaluation-vs-traditional-prs)
- [Vertex AI Agent Platform: ADK, Agent Engine, and runtime hosting](#vertex-ai-agent-platform-adk-agent-engine-and-runtime-hosting)
- [The Build-Scale-Govern lifecycle for enterprise agents](#the-build-scale-govern-lifecycle-for-enterprise-agents)
- [Open standards: A2A, A2UI, A2P, and Linux Foundation contributions](#open-standards-a2a-a2ui-a2p-and-linux-foundation-contributions)

## DevFest energy and the democratizing reset of AI

Mike Clark reflects on the developer landscape at DevFest Silicon Valley:
- **Leveling the playing field**: Historically, building advanced software required specialized compute access and deep systems programming knowledge. Modern generative AI abstracts computational complexity, enabling developers of all experience levels to build sophisticated systems.
- **Cross-discipline reset**: Product managers, researchers, and engineers are simultaneously redefining their daily practices around agentic workflows.

## Shifting from syntax mastery to creative intent and business outcomes

- **Historical evolution**: Drawing parallels from early Unix, Photobucket server scaling, and Firebase full-stack empowerment, Clark notes that every computing inflection point expands the developer pool.
- **Intent over syntax**: Low-code and vibe coding tools (such as AI Studio and ADK) enable citizen developers and domain specialists (e.g., marketing teams deploying production logic) to solve problems directly without waiting on traditional engineering queues.

## Rethinking code quality: outcome-driven evaluation vs. traditional PRs

- **Outcome metrics**: In production environments, system success is determined by whether the software securely and reliably delivers the intended business outcome rather than stylistic code aesthetics.
- **Continuous pull requests**: Traditional static code reviews are evolving into automated, multi-step agent validation loops where models continuously evaluate intermediate steps for safety, policy adherence, and functional correctness.

`mermaid
flowchart LR
  U[User Goal / Prompt] --> A[Agentic Step Execution]
  A --> V{Continuous Validation Loop
Safety, Policy & Functional Checks}
  V -->|Pass| E[Execute Tool / Next Step]
  V -->|Fail| R[Corrective Loop / Trace Log]
  E --> OUT[Verified Business Outcome]
`

## Vertex AI Agent Platform: ADK, Agent Engine, and runtime hosting

Google Cloud provides an integrated end-to-end stack for building and managing production agents:

| Component | Functionality | Deployment Surfaces |
|---|---|---|
| **Agent Development Kit (ADK)** | Open-source SDK orchestrating models, instructions, and tools | Local development, Cloud Run, GKE |
| **Agent Engine** | Managed runtime offering authentication, observability, and evaluation | Vertex AI, Google Cloud |
| **OpenTelemetry Integration** | Comprehensive execution tracing and latency monitoring | Cloud Logging, Cloud Monitoring |

## The Build-Scale-Govern lifecycle for enterprise agents

1. **Build**: Rapid prototype construction, prompt engineering, and tool binding using the ADK.
2. **Scale**: Production deployment across managed runtimes with automated autoscaling and distributed tracing.
3. **Govern**: Enforcing granular access control, cryptographic agent identity, and regulatory compliance.
   - *Example*: **Color Health** uses the full stack to deploy cancer screening adherence agents under strict healthcare governance constraints.

## Open standards: A2A, A2UI, A2P, and Linux Foundation contributions

To avoid closed vendor lock-in and enable cross-platform agent coordination, Google Cloud open-sources foundational protocols and contributes them to the Linux Foundation:
- **A2A (Agent-to-Agent)**: Direct inter-agent communication, discovery, and skill advertisement.
- **A2UI (Agent-to-UI)**: Real-time generation and streaming of dynamic user interfaces from agent state.
- **A2P (Agent-to-Payment)**: Protocol definitions for authenticated agent-mediated commercial transactions.

## Source

Full cleaned transcript: DATA/videos/mike-clark-vertex-ai-devfest-2025.json
Raw transcript: RAW/videos/mike-clark-vertex-ai-devfest-2025.md
