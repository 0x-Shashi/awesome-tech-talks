# Koray Kavukcuoglu: This Is How We Are Going to Build AGI

**Speaker(s):** Logan Kilpatrick, Koray Kavukcuoglu - **Channel:** Google for Developers - **Date:** 2025-11-25
**Watch:** https://youtu.be/fXtna7UrL44?si=cwFn4bPyjMNkKVYJ - **Format:** Fireside Chat - **Level:** Intermediate
**Topics:** LLM Fundamentals - AI Agents - Research/Papers

## TL;DR

Koray Kavukcuoglu (CTO of Google DeepMind and Chief AI Architect of Google) and Logan Kilpatrick discuss the launch of Gemini 3, crossing 1500 Elo on LMSYS, co-building AGI through product integration (Antigravity, AI Studio, Search), the convergence of generative media (Nano Banana Pro), and DeepMind's cultural shift from academic publishing to a high-velocity engineering discipline.

## Contents

- [Gemini 3 launch reception and continuous research acceleration](#gemini-3-launch-reception-and-continuous-research-acceleration)
- [Key focus areas: instruction following, internationalization, and tool calls](#key-focus-areas-for-gemini-instruction-following-internationalization-and-tool-calls)
- [Product scaffolding: Antigravity, AI Studio, and real-world signal](#product-scaffolding-antigravity-ai-studio-and-real-world-signal)
- [Role of Chief AI Architect: aligning research with global products](#role-of-chief-ai-architect-aligning-research-with-global-products)
- [From pure research to an engineering mindset: scaling DeepMind](#from-pure-research-to-an-engineering-mindset-scaling-deepmind)
- [Generative media convergence: Nano Banana and Nano Banana Pro](#generative-media-convergence-nano-banana-and-nano-banana-pro)
- [Google's comeback story and the imperative of ongoing innovation](#googles-comeback-story-and-the-imperative-of-ongoing-innovation)

## Gemini 3 launch reception and continuous research acceleration

Koray Kavukcuoglu addresses the state of AI scaling following the Gemini 3 rollout:
- **Scaling momentum**: Research across pre-training, post-training, and reinforcement learning continues to yield major capability leaps without plateauing.
- **Dynamic benchmarks**: As static benchmarks (such as GPQA Diamond) approach saturation, new evaluations like **HLE** (Humanity's Last Exam) and **ARC-AGI-2** define the frontier for advanced reasoning.

## Key focus areas for Gemini: instruction following, internationalization, and tool calls

1. **Instruction Following**: Ensuring strict adherence to complex user constraints and negative instructions.
2. **Internationalization**: Expanding multilingual reasoning for historically under-represented global languages.
3. **Function Calling & Agentic Code**: Enabling the model to execute tools, synthesize new tools dynamically, and orchestrate actions across environments.

## Product scaffolding: Antigravity, AI Studio, and real-world signal

Kavukcuoglu emphasizes that building artificial general intelligence requires tight integration with production applications:
- **Real-world feedback loops**: Products like **Antigravity** (agentic coding harness), **AI Studio**, and **Search AI Mode** channel direct developer usage patterns back to DeepMind researchers.
- **Co-building AGI**: Insights from professional coding workflows expose model reasoning failures that synthetic academic benchmarks cannot capture.

`mermaid
flowchart LR
  M[Gemini 3 Foundation Model] --> P[Product Harnesses
Antigravity, AI Studio, Search]
  P --> U[Developer & Enterprise Usage]
  U --> S[High-Bandwidth Error Signals]
  S --> R[DeepMind Research & Post-Training Loop]
  R --> M
`

## Role of Chief AI Architect: aligning research with global products

- **Bridging research and products**: Synchronizing research roadmaps with Google's major product surfaces to enable Day 1 global launches.
- **Engineering safety from the ground up**: Embedding safety, alignment, and security specialists directly into post-training cycles rather than treating safety as an afterthought.

## From pure research to an engineering mindset: scaling DeepMind

- **Cultural evolution**: DeepMind transitioned from small research cohorts writing isolated academic papers (DQN, AlphaGo, AlphaFold) into an integrated engineering organization shipping frontier model families every 6 months and monthly updates.
- **Shared exploration lines**: High-risk research programs (such as **Deep Think** for competitive mathematics like the IMO) feed algorithmic innovations back into general-purpose Gemini checkpoints.

## Generative media convergence: Nano Banana and Nano Banana Pro

- **Architectural convergence**: The historical split between language models and visual diffusion pipelines is dissolving into unified multimodal architectures.
- **Nano Banana Pro**: Built directly on **Gemini 3 Pro**, combining deep reasoning with pixel-level synthesis to generate complex infographics and diagrams directly from technical source documents.

## Google's comeback story and the imperative of ongoing innovation

- **The underdog phase**: Kavukcuoglu recounts DeepMind's early days (joining in 2012 from Yann LeCun's NYU lab) and acknowledges that Google initially lagged in modern generative LLM development.
- **Innovation over scale**: Google regained frontier leadership - crossing 1500 Elo as the top model on the LMSYS Arena - through algorithmic innovation across data, hardware, and training architectures rather than brute-force scaling alone.

## Source

Full cleaned transcript: DATA/videos/koray-kavukcuoglu-building-agi-2025.json
Raw transcript: RAW/videos/koray-kavukcuoglu-building-agi-2025.md
