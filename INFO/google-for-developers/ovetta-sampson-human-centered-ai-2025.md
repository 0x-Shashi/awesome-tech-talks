# Building human-centered AI products with Ovetta Sampson

**Speaker(s):** Ashley Oldacre, Ovetta Sampson - **Channel:** Google for Developers - **Date:** 2025-07-23
**Watch:** https://youtu.be/PALRROM2JWE?si=8EiT1FNB5A04k3mI - **Format:** Fireside Chat - **Level:** Intermediate
**Topics:** Product/Startup - Research/Papers - Career/Advice

## TL;DR

Ovetta Sampson (Director of UX for AI Compute Enablement at Google) sits down with Ashley Oldacre to discuss human-centered machine learning design, grounding algorithmic features in qualitative human heuristics, the dangers of traumatized datasets, and shifting responsible AI enforcement from individual engineers to automated ML platform infrastructure.

## Contents

- [From investigative journalism to machine learning design](#from-investigative-journalism-to-machine-learning-design)
- [Human-centered AI: augmenting human expertise vs. tech-driven capability](#human-centered-ai-augmenting-human-expertise-vs-tech-driven-capability)
- [Sensor fusion and human problem solving: the AI nose case study](#sensor-fusion-and-human-problem-solving-the-ai-nose-case-study)
- [The hazard of traumatized datasets and systemic algorithmic bias](#the-hazard-of-traumatized-datasets-and-systemic-algorithmic-bias)
- [Shifting responsible AI from individual developers to system infrastructure](#shifting-responsible-ai-from-individual-developers-to-system-infrastructure)
- [AI literacy, media ethics, and designing for human vulnerability](#ai-literacy-media-ethics-and-designing-for-human-vulnerability)

## From investigative journalism to machine learning design

Ovetta Sampson details her unique career trajectory:
- **Investigative data journalism**: 22 years in reporting, writing SQL, R, and Python models to analyze crime records and public statistics.
- **Embedded design research**: Earned an MS in Human-Computer Interaction at DePaul University before joining IDEO in 2016, bridging user research with early data science platforms.

## Human-centered AI: augmenting human expertise vs. tech-driven capability

- **Capability vs. Need**: Technology-driven AI starts with raw model affordances and searches for use cases; human-centered AI starts with human problems and applies models to augment human capabilities.
- **The human algorithm**: In building malpractice risk prediction models, the design team extracted core predictive signals by shadowing legal intake coordinators with 20 years of heuristic domain pattern recognition.

`mermaid
flowchart LR
  Expert[Domain Expert Heuristics
20+ Years Qualitative Intuition] --> UserResearch[Human-Centered Design Synthesis]
  UserResearch --> ModelFeatures[ML Model Feature Engineering]
  ModelFeatures --> Model[Predictive ML Model]
  Model --> Decision[Augmented Human Decision Support]
`

## Sensor fusion and human problem solving: the AI nose case study

- **Edge sensor pairing**: Pairing gas sensors with microcontroller ML models to classify gas signatures (the AI nose).
- **Cross-domain transfer**: Initially created to track sourdough bread proofing, a 13-year-old developer adapted the same sensory ML architecture to detect gas biomarkers of respiratory pneumonia in medical clinics.

## The hazard of traumatized datasets and systemic algorithmic bias

Sampson warns against treating models as socially neutral:

| Domain | Biased / Traumatized Source Data | Systemic Risk |
|---|---|---|
| **Predictive Policing** | Historical arrest records (e.g., Strategic Subjects List) | Confounds arrests with criminality, disproportionately targeting marginalized groups |
| **Credit Scoring** | Legacy financial lending data | Perpetuates historical demographic exclusions in credit limits and mortgage approvals |
| **Healthcare Diagnostics** | Homogeneous clinical trials | Fails to generalize across diverse demographic and genetic cohorts |

## Shifting responsible AI from individual developers to system infrastructure

- **Platform-level guardrails**: Rather than relying on individual developers to remember ethical checklists, Google's ML compute infrastructure embeds automatic dataset auditing directly into the developer workflow.
- **Auditable provenance**: Generating automated lineage graphs, demographic distribution alerts, and model evaluation dashboards modeled on banking compliance standards.

## AI literacy, media ethics, and designing for human vulnerability

- **AI Literacy**: Teaching public discernment against deepfake media and voice cloning, paralleling classical media literacy education.
- **ISO Standard Compliance**: Adhering to the ISO human-centered design standard to ensure products actively safeguard users against cognitive, physical, and psychological harm.

## Source

Full cleaned transcript: DATA/videos/ovetta-sampson-human-centered-ai-2025.json
Raw transcript: RAW/videos/ovetta-sampson-human-centered-ai-2025.md
