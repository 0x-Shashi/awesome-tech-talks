# Physical AI: the new era of robotics

**Speaker(s):** Jacklyn Dallas, Kanishka Rao, Alberto Rodriguez - **Channel:** Google for Developers - **Date:** unknown
**Watch:** https://youtu.be/jn3iypY-cN4?si=mZcYAxibt6K5PkhY - **Format:** Panel - **Level:** Intermediate
**Topics:** Research/Papers - AI Agents - LLM Fundamentals

## TL;DR

Kanishka Rao (Head of Robotics, Google DeepMind) and Alberto Rodriguez (Head of Robotics Behavior, Boston Dynamics) explain why 2026 is a genuine inflection point for embodied AI. Their core thesis: general-purpose digital AI breakthroughs (VLMs, world models, thinking tokens) are now flowing into robotics, locomotion is largely solved, and dexterity is the remaining hard problem standing between current robots and household usefulness in 5-10 years.

## Contents

- [Why 2026 is a breakthrough year for robotics](#why-2026-is-a-breakthrough-year-for-robotics)
- [Why humanoid robots: hardware and data arguments](#why-humanoid-robots-the-hardware-and-data-arguments)
- [Two training paradigms: simulation and teleoperation](#two-training-paradigms-simulation-for-locomotion-teleoperation-for-dexterity)
- [Why dexterity is the hardest remaining problem](#why-dexterity-is-the-hardest-remaining-problem)
- [Vision-based models and the tactile gap](#vision-based-models-and-the-tactile-gap)
- [Thinking tokens in the Gemini robotics model](#thinking-tokens-in-the-gemini-robotics-model)
- [Robotics roadmap: timeline and remaining blockers](#robotics-roadmap-timeline-and-remaining-blockers)
- [What robots are very good at today](#what-robots-are-very-good-at-today)
- [Vision for robotics in 10 years](#vision-for-robotics-in-10-years)

## Why 2026 is a breakthrough year for robotics

Kanishka Rao describes the mechanism: breakthroughs in general-purpose digital AI are now flowing into the physical world. The key move: adapting large vision-language models (VLMs) for robotics by adding a third modality - action - represented as physical tokens alongside the standard vision and language tokens. The result is a **VLA (Vision-Language-Action) model**.

VLAs give robots human-world understanding for free from pretraining, without that understanding needing to be re-learned in robotics-specific data. A live demonstration: a robot asked to pick up the extinct animal, with no robotics training on that concept, correctly identified and grasped a toy dinosaur from a collection of toys. The concept of extinct animal existed only in the vision-language pretraining.

## Why humanoid robots: the hardware and data arguments

**Data scaling argument (Rodriguez)**: The simplest and most scalable path to large training datasets for robot intelligence is human demonstration. A robot with a human body form factor can learn from humans most directly.

**Hardware capability argument (Rodriguez)**:
- Two arms: superior to one arm for load balancing and object repositioning
- Two legs: access to any place a human can reach, plus dynamic form factor adaptation (becoming thin to fit through gaps, or stable to resist forces)
- Dynamic foot placement: adjusts ground friction for faster, more efficient acceleration and deceleration than wheeled robots

**Physical AGI argument (Rao)**: AGI is typically defined as matching or exceeding human capability across tasks. The humanoid form factor is the right substrate for testing that claim, because it maps directly to the definition.

## Two training paradigms: simulation for locomotion, teleoperation for dexterity

Robot training splits into two fundamentally different regimes:

**1. Simulation + reinforcement learning (locomotion)**
Tasks that can be simulated with high fidelity are trained in simulation with verifiable reward loops, then transferred to the real world. Locomotion, balance, whole-body dynamics, and motion under load are all in this category. Boston Dynamics leads in this area. The new Atlas generation was designed specifically for mass manufacturing (hardware simplicity, reliability) to enable data collection and deployment at scale.

**2. Real-world teleoperation (dexterity)**
Manipulation tasks cannot be simulated at sufficient fidelity because the full variety of real-world objects and contact mechanics is impossible to capture. Human pilots wearing VR headsets see through the robot's cameras, then control the robot to perform manipulation tasks. The VR embodiment constraint ensures pilots can only use information the robot would have during autonomous operation, making the demonstrations as clean as possible.

`mermaid
flowchart LR
  L[Locomotion tasks:
whole-body balance
walking, running, load carrying] --> SIM[Simulation + RL
best path for simulatable tasks]
  D[Dexterity tasks:
fine manipulation
object grasping] --> TELE[Real-world teleoperation
human pilot in VR headset]
  SIM --> TRANSFER[Sim-to-real transfer]
  TELE --> VLA[VLA model training
physical tokens + vision + language]
`

## Why dexterity is the hardest remaining problem

Rao states plainly: AI can code an operating system in 24 hours or solve advanced math, but cannot scramble eggs. The gap between digital intelligence and physical dexterity is real.

**Why fine manipulation is hard:**

1. **Demonstration difficulty**: pilots trying to control a robot hand to unscrew a bottle cap cannot feel what the fingers are feeling. The quality of the demonstration data is fundamentally limited by the absence of haptic feedback to the demonstrator.

2. **Simulation difficulty**: the contact mechanics of skin compression and fingertip sensing are extremely difficult to simulate with the fidelity required for learning fine manipulation.

3. **Generalization narrowness**: a robot trained to unscrew a specific bottle type does not automatically generalize the verb unscrew to other objects the way a human does. Humans learn a skill once and transfer it broadly; robots learn it narrowly and transfer it to a few near-neighbor objects.

Rodriguez's benchmark: picking up a single object from a cluttered bin (not zero, not two, but exactly one), especially objects wedged in corners - is still genuinely hard. So is handling cables (deformable), using power tools (requires calibrated grip force), and other industrial manipulation tasks that require combined skill.

## Vision-based models and the tactile gap

All state-of-the-art manipulation models are currently vision-based, despite the intuition that touch should be primary. The reasons:

- **Data scale**: internet-scale vision pretraining data dwarfs any available tactile dataset
- **Wrist cameras as tactile proxies**: cameras on robot wrists or end effectors provide close-up pixel-level views of contact points. Compression and deformation visible in pixels serves as a proxy for what a human would feel. This works better than expected.

Rodriguez's key observation: eye-tracking studies of humans doing everyday tasks show that people almost never look at their hands while manipulating objects. Most manipulation is driven by tactile and proprioceptive feedback. The brief glance is just for orientation. This tells us where the future is: once reliable tactile hardware exists, robots will shift vision to common-sense understanding (high-level, low-frequency) and tactile sensing to high-frequency control loops - mirroring the actual human architecture.

Current state: vision works better than it should for manipulation. An origami-folding robot using only vision successfully reads crease patterns and folds angles - a task that seems to require touch - by inferring force states from visual signals.

## Thinking tokens in the Gemini robotics model

Standard VLA models are purely reactive: observe image, output action. They cannot explain their decisions. Rao describes this as the muscle memory regime of robotics - fast, effective, but not interpretable.

The Gemini robotics model introduces **thinking tokens**: before generating each action token, the model generates a natural-language reasoning trace about what it observes and what it plans to do.

**Example reasoning traces:**
- Without thinking tokens: [observe image] -> [output: close hand] (no intermediate step)
- With thinking tokens: I am close enough to close my hand and will grasp the bottle -> [output: close hand]
- After trace edit: I am not close enough, I need to go lower -> [output: move down, then close hand]

Editing the thought trace produces different actions in predictable ways. This makes the model both **interpretable** (you can read why it is doing something) and **steerable** (you can correct behavior by adjusting the thought process). The laundry sorting demo showed an unprogrammed emergent behavior: the model thought adjust the black bin a little bit so I can pick up the cloth and then acted on it, despite never being explicitly trained for that specific sequence.

## Robotics roadmap: timeline and remaining blockers

Rao's timeline: **5-10 years** before robots capable of general household and daily-life tasks become realistic. Not next year.

**Three remaining blockers:**

1. **Dexterity and object generalization**: the key unsolved manipulation problems
2. **Tactile hardware**: current sensors lack the reliability and sensitivity for industrial-scale deployment
3. **Safety AI**: Rao compares robotics to autonomous driving, where safety is a core requirement, not an add-on. Unsafe robots are useless robots regardless of their intelligence.

Rodriguez's current research focus at Boston Dynamics: **multi-frequency decision architecture**. Robots need to make decisions at radically different frequencies simultaneously:
- Low-frequency (~1 Hz): what to interact with, what approach to use
- High-frequency (50-100 Hz): contact accommodation, balance corrections, grasp adjustments

The architecture that serves both frequencies simultaneously, and the right combination of demonstration vs. trial-and-error training to populate it, is the central open research question.

## What robots are very good at today

| Capability | Status |
|---|---|
| Whole-body balance and locomotion | Solved |
| Walking, running, stairs | Solved |
| Carrying heavy loads (Atlas: fridge; Stretch: 50-60 lb boxes) | Working |
| Basic pick and place | Good (imitation learning) |
| Repetitive industrial inspection (Spot) | Deployed and operational |
| Origami folding (vision-only) | Working |
| Laundry sorting with thinking tokens | Early research, working |
| Cable handling | Still hard |
| Power tool use with calibrated grip | Still hard |
| Bin picking of single objects from clutter | Still hard |
| Opening a bottle cap with a robot hand | Not reliably solved |
| Picking keys from a pocket or purse | Not attempted |

## Vision for robotics in 10 years

**Rao**: dexterity and safety solved means robots handling the boring, repetitive, dangerous, and dull physical tasks of daily life. The goal is to benefit humanity by taking the work that nobody wants to do.

**Rodriguez**: eliminating arduous physical labor at scale.
- Stretch already eliminates the need for humans to unload boxes from trucks in 100-degree trailers
- Spot eliminates the need for humans to do 500 consecutive identical inspections to catch 1 anomaly
- Atlas targets heavier industrial labor where physical demands are high and error tolerance is low

Commercial roadmap: industrial manufacturing is the entry point (controlled environments, manageable safety constraints, established cost tolerance for automation). Residential and consumer deployments follow as safety approaches mature.

## Source

Full cleaned transcript: DATA/videos/physical-ai-robotics-2026.json
Raw transcript: RAW/videos/physical-ai-robotics-2026.md
