# Demis Hassabis on shipping momentum, better evals and world models

**Speaker(s):** Logan Kilpatrick, Demis Hassabis - **Channel:** Google for Developers - **Date:** 2025-08-11
**Watch:** https://youtu.be/njDochQ2zHs?si=jyW6558bNmAoKQ70 - **Format:** Fireside Chat - **Level:** Intermediate
**Topics:** Research/Papers - LLM Fundamentals - AI Agents

## TL;DR

Demis Hassabis (CEO of Google DeepMind) joins Logan Kilpatrick to discuss thinking models (Deep Think), solving jagged intelligence, the physics of world models with Genie 3, synthetic training loops with SIMA, transitioning evaluation to Kaggle Game Arena, and the ultimate convergence of Gemini, Veo, and Genie into a single unified Omni model.

## Contents

- [DeepMind shipping momentum: Deep Think and thinking models](#deepmind-shipping-momentum-deep-think-and-thinking-models)
- [Jagged intelligence: why frontier models still fail at basic tasks](#jagged-intelligence-why-frontier-models-still-fail-at-basic-tasks)
- [Genie 3 and the physics of world models](#genie-3-and-the-physics-of-world-models)
- [AI inside AI: SIMA playing within Genie-generated worlds](#ai-inside-ai-sima-playing-within-genie-generated-worlds)
- [Kaggle Game Arena: moving past saturated static benchmarks](#kaggle-game-arena-moving-past-saturated-static-benchmarks)
- [Tool integration vs. core capabilities in foundation models](#tool-integration-vs-core-capabilities-in-foundation-models)
- [The convergence path: from specialized tools to a single Omni model](#the-convergence-path-from-specialized-tools-to-a-single-omni-model)

## DeepMind shipping momentum: Deep Think and thinking models

DeepMind's deployment cadence combines deep reinforcement learning with test-time reasoning compute:
- **Thinking models**: Harking back to AlphaGo and AlphaZero, thinking architectures explore parallel search trees, critique preliminary reasoning steps, and collapse rollouts into verified final decisions.
- **Deep Think IMO milestone**: Achieving gold-medal performance on International Mathematical Olympiad problems using general Gemini foundation checkpoints enhanced with reasoning search.

## Jagged intelligence: why frontier models still fail at basic tasks

Hassabis explains the structural unevenness in modern models:
- **Asymmetric capabilities**: Models can solve PhD-level mathematics yet fail simple high school logic puzzles or board game rule variations.
- **Consistency as the AGI benchmark**: True general intelligence requires resolving reasoning brittleness, spatial planning, and robust memory rather than continuing naive pre-training scaling alone.

## Genie 3 and the physics of world models

AGI systems must comprehend the physical world to power embodied robotics and universal assistants like **Project Astra**:
- **World models**: Simulate intuitive physics, material interactions, fluid dynamics, and spatial permanence.
- **Spatiotemporal consistency**: Genie 3 maintains object and scene consistency when the camera perspective rotates away and returns.

`mermaid
flowchart LR
  Prompt[Text / Image Prompt] --> Genie[Genie 3 World Model
Dynamic 3D Simulation Engine]
  Genie -->|Generates Environment| SIMA[SIMA Agent
Embodied AI Player]
  SIMA -->|Sends Action Commands| Genie
  SIMA --> Data[(Infinite Synthetic Training Data)]
  Data --> Robot[Robotics & Embodied Models / Astra]
`

## AI inside AI: SIMA playing within Genie-generated worlds

- **Synthetic exploration loops**: DeepMind pairs **SIMA** (Scalable Instructable Multiworld Agent) with Genie 3, where SIMA navigates dynamic 3D environments generated on the fly by Genie.
- **Next-generation entertainment**: Enables emergent interactive digital experiences bridging video games and cinema.

## Kaggle Game Arena: moving past saturated static benchmarks

With traditional benchmarks like AIME nearing ceiling effects (Deep Think at 99.2%), static exam datasets are vulnerable to contamination:
- **Dynamic competitive evaluation**: Kaggle Game Arena pits leading models against one another across thousands of game environments (starting with chess).
- **Self-scaling difficulty**: Matches yield dynamic Elo ratings where difficulty scales naturally with opponent capability.

## Tool integration vs. core capabilities in foundation models

| Domain | Architectural Placement | Rationale |
|---|---|---|
| **Math & Coding** | Core Model Weights | Broadly elevates general cognitive and reasoning capabilities |
| **Specialized Engines (e.g., Stockfish, Physics Sims)** | External Tool Invocations | Prevents catastrophic forgetting and avoids polluting core representations |

## The convergence path: from specialized tools to a single Omni model

Hassabis outlines the convergence roadmap:
- **Current state**: Specialized models for video synthesis (Veo 3), world simulation (Genie 3), and reasoning language understanding (Gemini).
- **The Omni model**: A unified multimodal architecture capable of perceiving, simulating, reasoning over, and interacting with arbitrary modalities and physical dynamics in a single foundation model.

## Source

Full cleaned transcript: DATA/videos/demis-hassabis-evals-world-models-2025.json
Raw transcript: RAW/videos/demis-hassabis-evals-world-models-2025.md
