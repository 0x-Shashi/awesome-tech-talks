# Building the quantum-AI future with Hartmut Neven and James Manyika

**Speaker(s):** James Manyika, Hartmut Neven - **Channel:** Google for Developers - **Date:** 2026-05-22
**Watch:** https://youtu.be/yQPnb4gxKRc?si=Z2WEZuDCKp0fhSuV - **Format:** Fireside Chat - **Level:** Intermediate
**Topics:** Research/Papers - Backend/Infra - LLM Fundamentals

## TL;DR

Hartmut Neven (Founder and Head of Google Quantum AI) and James Manyika (President of Research Labs, Technology & Society at Google) discuss the bidirectional synergy between quantum computing and AI. They examine the Willow chip's error-correction breakthroughs, the Quantum Echoes algorithm for molecular structure discovery, shrinking timelines for post-quantum cryptography, and Google's parallel expansion into neutral atom quantum architectures.

## Contents

- [Quantum computing fundamentals and superposition](#quantum-computing-fundamentals-and-superposition)
- [Hardware progress: coherence times and cooling](#hardware-progress-coherence-times-and-cooling)
- [Feynman's killer app and quantum simulation targets](#feynmans-killer-app-and-quantum-simulation-targets)
- [Google's six-milestone roadmap and error correction progress](#googles-six-milestone-roadmap-and-error-correction-progress)
- [Quantum Echoes: first practical quantum machine learning algorithm](#quantum-echoes-first-practical-quantum-machine-learning-algorithm)
- [Bidirectional acceleration: Quantum plus AI equals Quantum AI](#bidirectional-acceleration-quantum-plus-ai-equals-quantum-ai)
- [Fundamental physics discoveries on quantum chips](#fundamental-physics-discoveries-on-quantum-chips)
- [Post-quantum cryptography timelines moving forward](#post-quantum-cryptography-timelines-moving-forward)
- [Quantum noise in generative media and neutral atom architectures](#quantum-noise-in-generative-media-and-neutral-atom-architectures)

## Quantum computing fundamentals and superposition

The computational speedup of quantum hardware stems from **superposition**, the principle in quantum mechanics allowing a physical system to occupy multiple configurations simultaneously that evolve together in time.

- **Willow chip configuration**: Houses 105 physical qubits.
- **State space**: 105 qubits define a Hilbert space of 2^105 distinct bit strings.
- **Parallel processing**: In a single processor clock cycle, the quantum chip operations evaluate across all 2^105 states simultaneously.
- **Macroscopic qubits**: Google uses loops of superconducting wire containing Josephson junctions (pioneered by Nobel laureates Michel Devoret, John Martinis, and John Clarke) to create artificial atoms with quantized energy levels at macroscopic scale, making them engineerable onto standard chip carriers.

## Hardware progress: coherence times and cooling

Quantum states are fragile and subject to decoherence from environmental noise.

- **Coherence time progress**: Has scaled from 20 microseconds in early superconducting systems to over 250 microseconds. Neven notes that coherence time is no longer the primary physics blocker; the bottleneck has transitioned to system-level electronics and modular scaling.
- **Extreme cooling**: Chips operate inside dilution refrigerators cooled to **10 millikelvin** (colder than interstellar space). In physical computing, temperature represents thermal noise that collapses superposition states into classical bits.

## Feynman's killer app and quantum simulation targets

Quantum computers are specialized accelerators rather than drop-in replacements for classical CPUs. As Richard Feynman formulated, simulating quantum physical systems on classical hardware runs into an exponential combinatorial wall.

**Key simulation targets:**
- **Lithium-air batteries**: Possess theoretical energy density exceeding jet kerosene (enabling electrified commercial aviation), but suffer from brittle materials and degradation that classical simulation cannot model accurately.
- **Catalyst discovery**: Modeling complex molecular interactions for clean chemical synthesis and carbon capture.
- **Algorithm growth**: The catalog of documented algorithms with proven quantum speedup has grown from ~60 to over 70, with expectations to scale by an order of magnitude as hardware matures.

## Google's six-milestone roadmap and error correction progress

Google Quantum AI operates against a six-milestone roadmap toward practical fault-tolerant computation:

1. **Milestone 1 (2019)**: Demonstration of quantum computational supremacy on synthetic benchmarks.
2. **Milestone 2 (2022)**: First physical demonstration of quantum error correction reducing error rates (physical to logical qubits).
3. **Willow chip results (2024)**: Below-threshold error correction achieved, cutting logical error rates by a factor of 2 compared to uncorrected baselines.
4. **Milestone 3 (In progress)**: Constructing a single high-fidelity, modular logical qubit block.
5. **Milestone 5 / Milestone 6**: Originally, commercial impact required 1,000,000 physical qubits (Milestone 6). Due to algorithmic improvements, ~100,000 physical qubits (Milestone 5) are now projected to deliver commercial advantage.

`mermaid
flowchart LR
  M1[Milestone 1
Quantum Supremacy 2019] --> M2[Milestone 2
Error Correction Proof 2022]
  M2 --> W[Willow Chip 2024
2x Below Threshold Error Suppression]
  W --> M3[Milestone 3
Modular Logical Qubit Unit]
  M3 --> M5[Milestone 5
100k Qubits: Commercial Quantum Advantage]
`

## Quantum Echoes: first practical quantum machine learning algorithm

Transitioning away from synthetic benchmarks (such as random circuit sampling), Google and UC Berkeley developed **Quantum Echoes**, the first quantum algorithm demonstrating utility on practical experimental data.

- **Application domain**: Nuclear Magnetic Resonance (NMR) and MRI data interpretation.
- **Chemistry breakthrough**: Successfully calculated the relative dihedral angle between the two benzene rings of diphenyl, resolving an unresolved structural measurement in chemistry directly on quantum hardware.

## Bidirectional acceleration: Quantum plus AI equals Quantum AI

Neven and Manyika describe a dual feedback loop uniting DeepMind and Quantum AI:

1. **AI for Quantum**: DeepMind's **AlphaQubit** trains machine learning neural network decoders to detect and correct quantum errors in real time, outperforming traditional heuristic decoding algorithms.
2. **Quantum for AI**: Classical foundation models in biology (such as AlphaFold) require decades of empirical dataset collection (e.g., the 50-year protein data bank). Quantum computers can generate high-fidelity synthetic physical training datasets for material science and molecular dynamics. Google Quantum AI has started delivering early materials science datasets to DeepMind.

## Fundamental physics discoveries on quantum chips

Google's quantum processors serve as hardware testbeds for fundamental physics:
- **Holographic duality and wormholes**: Entangled qubits on-chip simulated traversable wormhole dynamics governed by AdS/CFT correspondence principles.
- **Time crystals**: Synthesized out-of-equilibrium matter that maintains periodic motion indefinitely without absorbing or dissipating environmental energy.
- **Non-abelian anyons**: Validated quasiparticle braiding on-chip where exchanging identical particles alters the overall quantum state.

## Post-quantum cryptography timelines moving forward

Advances in quantum algorithms have dramatically compressed the hardware requirements needed to break standard public-key cryptography:

| Cryptographic Standard | Historical Qubit Requirement | Current Required Qubits (Gidney) | Target Timeline |
|---|---|---|---|
| **RSA-2048** | ~20,000,000 physical qubits | ~1,000,000 physical qubits | Urgency moving inward |
| **ECC-256 (Digital Signatures/Crypto)** | Multi-million | ~100,000 - 300,000 physical qubits | Transition by **2029** recommended |

Due to these optimizations, organizations must accelerate migration to NIST post-quantum cryptography standards.

## Quantum noise in generative media and neutral atom architectures

**Quantum generative art**: Google connected quantum processor noise distributions directly to diffusion model noise tensors. Collaborations with artist Refik Anadol (Quantum Memories) drew over 1.3 million in-person museum attendees.

**Neutral atom expansion**: Google opened a new laboratory in Boulder, Colorado, pursuing neutral atom quantum computing in parallel with superconducting qubits. While superconducting circuits offer superior gate execution speeds, neutral atom systems provide natural coupling with quantum sensing for ultra-high-precision physical instrumentation.

## Source

Full cleaned transcript: DATA/videos/neven-manyika-quantum-ai-2026.json
Raw transcript: RAW/videos/neven-manyika-quantum-ai-2026.md
