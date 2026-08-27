# Defining the agentic AI era

**Speaker(s):** Logan Kilpatrick, Koray Kavukcuoglu, Liz Reid, Josh Woodward, Jeff Dean - **Channel:** Google for Developers - **Date:** 2026-05-22
**Watch:** https://youtu.be/bc4QwDd5jB0?si=6JCnE-EZh0kr5q5o - **Format:** Panel - **Level:** Intermediate
**Topics:** AI Agents - AI Coding Tools - Product/Startup

## TL;DR

Google AI leadership (Jeff Dean, Koray Kavukcuoglu, Liz Reid, Josh Woodward, hosted by Logan Kilpatrick) discuss the shift to proactive agentic architectures. Key topics include TPU v8 inference optimizations, Amdahl's law applying to tool execution speed, machine-readable specifications replacing PRDs (DESIGN.md), 24/7 background agents in Gemini Spark, and how Antigravity powers bespoke software generation inside Search and Google Labs.

## Contents

- [Gemini 3.5 Flash: purpose-built for agentic workflows and coding](#gemini-35-flash-purpose-built-for-agentic-workflows-and-coding)
- [Full-stack AI infrastructure: 8th-generation TPUs and inference optimization](#full-stack-ai-infrastructure-8th-generation-tpus-and-inference-optimization)
- [Rethinking search latency in an agentic paradigm](#rethinking-search-latency-in-an-agentic-paradigm)
- [Gemini Spark: proactive 24/7 background agent workflows](#gemini-spark-proactive-247-background-agent-workflows)
- [Amdahl's law and tool latency: the next performance bottleneck](#amdahls-law-and-tool-latency-the-next-performance-bottleneck)
- [Machine-readable context: DESIGN.md and the elimination of PRDs](#machine-readable-context-designmd-and-the-elimination-of-prds)
- [Organizational transformation: the asynchronous engineering Renaissance](#organizational-transformation-the-asynchronous-engineering-renaissance)
- [Bespoke software generation: shifting from static apps to autonomous tools](#bespoke-software-generation-shifting-from-static-apps-to-autonomous-tools)

## Gemini 3.5 Flash: purpose-built for agentic workflows and coding

Koray Kavukcuoglu (CTO of DeepMind) outlines the engineering intent behind Gemini 3.5 Flash:
- **Long-horizon reasoning**: Purpose-built to navigate extended multi-step tasks without context drift or reasoning breakdown.
- **Internal stress testing**: Built through intensive internal dogfooding across Google's engineering teams for real-world software maintenance and agentic task orchestration.
- **Unified release**: Launched simultaneously across consumer (Gemini App, Spark), developer (Antigravity, API), and infrastructure (Google Search) surfaces.

## Full-stack AI infrastructure: 8th-generation TPUs and inference optimization

Jeff Dean highlights how custom hardware co-design enables agentic execution:
- **TPU v8 architectural separation**: Dedicated hardware split between training throughput and low-latency inference serving.
- **Compounding agent latency**: In multi-agent harnesses, a single top-level user goal triggers dozens of subagent iterations and tool calls. High inference velocity is essential to prevent cumulative delays from making agents unusable.

## Rethinking search latency in an agentic paradigm

Liz Reid discusses the evolving relationship between user expectations and system latency:
- **Task value calibration**: Simple queries require sub-second responses. Complex synthesis (e.g., generating an interactive application or deep comparative research) justifies a 10 to 60-second processing window.
- **Deep integration**: Search integrates Gemini 3.5 Flash alongside the Antigravity SDK to dynamically coordinate backend databases (financial metrics, sports statistics, local entity graphs) through generalized reasoning instead of brittle templates.

## Gemini Spark: proactive 24/7 background agent workflows

Josh Woodward introduces Gemini Spark as an always-on background agent:
- **Scheduled and trigger-based tasks**: Periodic morning syntheses, continuous inbox monitoring, and drafting responses to urgent leadership emails with explicit verification guards (drafting research without auto-sending).
- **Domain adaptation**: Delivers sports updates and topical tracking in conversational tones calibrated to user persona.
- **Artifact synthesis**: Autonomously drafts slide decks, briefing docs, and interactive charts ready for human review.

## Amdahl's law and tool latency: the next performance bottleneck

Jeff Dean presents an architectural insight regarding agent execution bottlenecks:
- **Amdahl's law in agent loops**: As neural network inference accelerates toward near-instant execution, external tool invocations (file system I/O, subprocess execution, API roundtrips) become the primary bottleneck.
- **Tool optimization**: Legacy tools built for human interactive speed must be re-engineered for machine execution.
- **Automated tool translation**: Google engineers used Gemini models to translate slow internal Python utility tools into compiled Go, achieving 10x to 20x speedups in tool runtime over a single evening.

`mermaid
flowchart LR
  U[User Prompt / Agent Goal] --> M[High-Speed Model Inference
TPU v8 Serving]
  M --> T[Tool Invocation Bottleneck
Legacy Python Scripts: High Latency]
  T --> REW[Automated Rewrite to Go / C++
10x-20x Speedup]
  REW --> FAST[Machine-Speed Agentic Loop]
`

## Machine-readable context: DESIGN.md and the elimination of PRDs

Google Labs teams have replaced traditional Product Requirement Documents (PRDs) with structured, machine-interpretable context files:
- **DESIGN.md standard**: Open-sourced via the Stitch project, standardizing app design systems, component tokens, and UX rules in markdown so coding agents can directly implement pixel-perfect user interfaces.
- **Context velocity**: Preparing technical and design constraints in clean, structured formats enables models to execute end-to-end features without human translation overhead.

## Organizational transformation: the asynchronous engineering Renaissance

Leadership workflows across Google have shifted toward asynchronous agentic delegation:
- **Asynchronous iteration**: Leaders and engineers assign complex investigations or refactors to agents during the workday, reviewing completed implementations and benchmarks asynchronously.
- **Democratized engineering**: Product managers adjust UI code and design tokens directly; senior engineers debug performance across unfamiliar monorepo codebases by directing agents to benchmark alternative concurrency models.

## Bespoke software generation: shifting from static apps to autonomous tools

- **Google Flow**: Filmmakers and creative professionals vibe-code custom shaders, lighting routines, and UI panels directly inside the authoring suite.
- **From static to bespoke software**: Historically, high software development costs forced applications to be standardized and rigid. High-speed agentic generation allows on-demand creation of specialized, single-purpose software tools tailored to immediate user tasks.

## Source

Full cleaned transcript: DATA/videos/defining-agentic-ai-era-2026.json
Raw transcript: RAW/videos/defining-agentic-ai-era-2026.md
