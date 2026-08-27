# Digital health with Dr. Oliver Aalami

**Speaker(s):** Ashley Oldacre, Dr. Oliver Aalami - **Channel:** Google for Developers - **Date:** 2025-07-23
**Watch:** https://youtu.be/sgx7-NAJJ0g?si=JHqkKCSxB-cSWZJc - **Format:** Fireside Chat - **Level:** Intermediate
**Topics:** Product/Startup - Research/Papers - Android/Mobile

## TL;DR

Dr. Oliver Aalami (Vascular Surgeon at Stanford University and Palo Alto VA, and Director of Stanford Biodesign for Digital Health) joins Ashley Oldacre to discuss translating medical research into digital applications. He shares the needs-driven Biodesign process, the open-source Stanford Spezi framework, unlocking patient health data via FHIR APIs, and using conversational LLMs to demystify clinical records for post-operative patients.

## Contents

- [Clinical vascular surgery and the origins of Stanford Biodesign](#clinical-vascular-surgery-and-the-origins-of-stanford-biodesign)
- [Needs finding beyond hospital walls: remote chronic disease management](#needs-finding-beyond-hospital-walls-remote-chronic-disease-management)
- [Spezi: open-source modular infrastructure for mobile health research](#spezi-open-source-modular-infrastructure-for-mobile-health-research)
- [The 21st Century Cures Act: democratizing patient electronic health records](#the-21st-century-cures-act-democratizing-patient-electronic-health-records)
- [LLM on FHIR: conversational clinical records and patient discharge synthesis](#llm-on-fhir-conversational-clinical-records-and-patient-discharge-synthesis)
- [Incentive alignment: value-based care, Medicare Advantage, and cross-functional teams](#incentive-alignment-value-based-care-medicare-advantage-and-cross-functional-teams)

## Clinical vascular surgery and the origins of Stanford Biodesign

- **Needs-driven innovation**: The Stanford Biodesign methodology mandates identifying clinical problems across all stakeholders before designing solutions.
- **Need statement anatomy**: Every project requires a structured need statement defining a precise problem, specific target population, and measurable clinical outcome.

## Needs finding beyond hospital walls: remote chronic disease management

- **Decentralizing care**: Connected edge sensors (smart scales, blood pressure cuffs, continuous cardiac patches like the Zio Patch) shift routine clinical management into patients' homes.
- **Continuous telemetry**: Replacing intermittent annual clinic visits with high-frequency physiological monitoring.

## Spezi: open-source modular infrastructure for mobile health research

`mermaid
flowchart LR
  Wearable[Wearable Sensors & Edge Devices] --> MobileApp[Spezi Mobile Framework
iOS & Android]
  MobileApp --> HL7[HL7 FHIR Interoperability Standard]
  HL7 --> Firebase[Serverless Cloud Backend
Firestore Database]
  Firebase --> Analysis[Spezi Data Pipeline
Google Colab & Python Telemetry]
`

- **Modular architecture**: Replaces monolithic application templates with composable modules for Bluetooth sensor streaming, user onboarding, and scheduled surveys.
- **Standards compliance**: Stores data natively in HL7 FHIR to ensure seamless interoperability with institutional electronic health record systems.

## The 21st Century Cures Act: democratizing patient electronic health records

- **API mandates**: Federal regulations require certified health record systems (e.g., Epic) to expose FHIR APIs directly to patients.
- **On-device privacy**: Utilizing frameworks like Android Health Connect allows patients to pull health records locally to run private on-device intelligence without third-party data broker exposure.

## LLM on FHIR: conversational clinical records and patient discharge synthesis

| Feature | Legacy Health Records | LLM on FHIR Implementation |
|---|---|---|
| **Format** | Opaque clinical discharge notes and raw lab values | Conversational dialogue with context-grounded citations |
| **Health Literacy** | Technical jargon provoking patient anxiety | Dynamic simplification to a 5th-grade reading level |
| **Multimodal Review** | Text-only summary reports | Foundation models highlighting specific anomalies on diagnostic X-rays |

## Incentive alignment: value-based care, Medicare Advantage, and cross-functional teams

- **Value-based alignment**: Payers operating under fixed capitation (Medicare Advantage, Kaiser Permanente) and self-insured employers benefit financially from digital prevention over fee-for-service hospital procedures.
- **Transdisciplinary training**: Stanford is conducting 22-person cluster hires bridging computer science faculty with clinical physicians to accelerate bedside AI deployment.

## Source

Full cleaned transcript: DATA/videos/oliver-aalami-digital-health-2025.json
Raw transcript: RAW/videos/oliver-aalami-digital-health-2025.md
