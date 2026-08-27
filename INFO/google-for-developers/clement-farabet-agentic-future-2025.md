# Season 5 - Shaping the agentic future with Clement Farabet

**Speaker(s):** Ashley Oldacre, Christina Warren, Clement Farabet - **Channel:** Google for Developers - **Date:** 2025-07-24
**Watch:** https://youtu.be/AM3yzTDW65U?si=NXWhzzSEChPauGBq - **Format:** Fireside Chat - **Level:** Intermediate
**Topics:** AI Agents - Research/Papers - LLM Fundamentals

## TL;DR

Clement Farabet (VP of Research at Google DeepMind) joins Ashley Oldacre and Christina Warren to launch Season 5 of People of AI. He traces the evolution from early CNN hardware and NVIDIA AI infrastructure to the agentic era, sharing insights on unified research-product loops, managing fleets of AI virtual interns, append-only OS guardrails for agents, and DeepMind's dual strategy with Gemini and Gemma.

## Contents

- [From CNN hardware to Twitter and NVIDIA AI infrastructure](#from-cnn-hardware-to-twitter-and-nvidia-ai-infrastructure)
- [The scaling hypothesis and the inevitability of transformers](#the-scaling-hypothesis-and-the-inevitability-of-transformers)
- [Unifying research and production into a single feedback loop](#unifying-research-and-production-into-a-single-feedback-loop)
- [Defining agency: from passive text generators to virtual interns](#defining-agency-from-passive-text-generators-to-virtual-interns)
- [Organizational governance, accountability, and agent sandboxing](#organizational-governance-accountability-and-agent-sandboxing)
- [Embodied physical robotics vs. unrestricted web agents](#embodied-physical-robotics-vs-unrestricted-web-agents)
- [Dual model strategy: frontier Gemini APIs and open Gemma weights](#dual-model-strategy-frontier-gemini-apis-and-open-gemma-weights)

## From CNN hardware to Twitter and NVIDIA AI infrastructure

Clement Farabet shares his 20-year trajectory across machine learning:
- **Academic origins**: Completed a PhD under Yann LeCun on real-time computer vision and custom deep learning silicon.
- **Startups and infrastructure**: Co-founded Madbits (acquired by Twitter in 2014) to build early multi-GPU computer vision pipelines, later serving as VP of AI Infrastructure at NVIDIA scaling self-driving vehicle neural networks with Jensen Huang.

## The scaling hypothesis and the inevitability of transformers

- **Compute efficiency unlock**: Transformers accelerated machine learning by offering superior parallelization over distributed compute clusters compared to earlier convolutional architectures.
- **Core scaling dynamics**: Across two decades of neural network research, the fundamental driver remains consistent: feeding massive multimodal datasets into scalable compute infrastructure.

## Unifying research and production into a single feedback loop

`mermaid
flowchart TD
  Research[DeepMind Frontier Research & Pre-Training] --> Foundation[Unified Gemini Foundation Checkpoints]
  Foundation --> APILayer[Managed APIs / AI Studio / Live API]
  APILayer --> Apps[Internal & External Products
Robotics, Coding Assistants, Search]
  Apps --> Usage[Production Interaction Signals & Error Traces]
  Usage --> RLHF[Post-Training & Agentic RL Alignment]
  RLHF --> Research
`

- **Eliminating tech transfer silos**: Rather than shipping academic papers to separate product teams, DeepMind directly trains foundation checkpoints powering real-time APIs.
- **Continuous post-training feedback**: Enterprise developer usage and real-world failure cases feed directly back into reinforcement learning and alignment pipelines.

## Defining agency: from passive text generators to virtual interns

Farabet distinguishes between passive language models and autonomous agents:
- **Agency**: The capability to autonomously formulate sub-goals, invoke external APIs, read screens, and execute financial or real-world transactions.
- **The virtual intern mental model**: Managing agents like entry-level interns: defining clear objectives, expecting exploratory errors, providing bounded sandboxes, and training models to self-critique before finalizing work.

## Organizational governance, accountability, and agent sandboxing

Scaling agentic fleets across enterprises requires rethinking software environments:
- **Manager as conductor**: Human developers act as technical managers guiding fleets of parallel agents rather than inspecting every intermediate line of code.
- **Append-only operating systems**: Designing execution environments where destructive overwrites are impossible, ensuring full auditability and instant state rollback.

## Embodied physical robotics vs. unrestricted web agents

| Dimension | Embodied Physical Robots | Unrestricted Web Agents |
|---|---|---|
| **Operating Domain** | Physical reality (manipulators, cameras) | Open web, APIs, payment gateways |
| **Safety Containment** | Bounded by kinematics and hardware e-stops | Requires strict cryptographic permissions and sandbox policies |
| **Learning Sample Efficiency** | Few-shot visual demonstrations (e.g., peeling a banana) | Multi-step web navigation with stateful recovery |

## Dual model strategy: frontier Gemini APIs and open Gemma weights

- **Frontier API (Gemini)**: Powers complex multi-modal agentic workloads, live streaming (Live API), and deep reasoning behind managed enterprise endpoints.
- **Open Weights (Gemma)**: Provides lightweight, high-performance open checkpoints to empower decentralized developer innovation and local edge deployment.

## Source

Full cleaned transcript: DATA/videos/clement-farabet-agentic-future-2025.json
Raw transcript: RAW/videos/clement-farabet-agentic-future-2025.md
