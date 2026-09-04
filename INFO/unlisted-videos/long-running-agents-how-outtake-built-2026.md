# Long Running Agents: How Outtake built a cyber investigator on Claude

**Speaker(s):** Anthropic and Partner Leaders · **Channel:** Unlisted Videos · **Date:** 2026-04-28
**Watch:** https://anthropic.ondemand.goldcast.io/on-demand/d508adb2-979f-4efb-bbec-abd3ad285000?email=devofficialcoma@gmail.com&first_name=dev&last_name=Dev · **Format:** Demo · **Level:** Advanced
**Topics:** AI Agents, Web Development

## TL;DR
This session explores long running agents: how outtake built a cyber investigator on claude, highlighting core architecture, runtime workflows, and practical deployment patterns across AI Agents, Web Development. Speakers analyze technical implementations and share operational best practices for building robust systems with Claude.

## Contents
- [Architectural Overview and System Objectives in Long Running Agents: How Outtake built a cybe](#architectural-overview-and-system-objectives-in-long-running-agents-how-outtake-built-a-cybe)
- [Technical Capabilities, Tooling Integration, and Protocols](#technical-capabilities-tooling-integration-and-protocols)
- [Production Deployment, Verification, and Best Practices](#production-deployment-verification-and-best-practices)
- [Organizational Impact, Scalability, and Industry Outlook](#organizational-impact-scalability-and-industry-outlook)

## Architectural Overview and System Objectives in Long Running Agents: How Outtake built a cybe

AI is making it cheaper and faster for bad actors to operate online. In response, Outtake built a fleet of cyber agents to fight back by identifying and dismantling threat networks across fake executive profiles, cloned websites, and fraudulent apps. In this webinar, they’ll walk through their Recon Agent, built on Claude, which traces a single threat indicator to the full adversarial network behind it in minutes. Join us for a live demo and practical takeaways for builders creating long-running agents and defenders reimagining security workflows. The session details foundational design principles, execution patterns, and operational integration requirements within the AI Agents, Web Development domain.

**Further reading:** Official documentation for Claude and Anthropic platform guides.

## Technical Capabilities, Tooling Integration, and Protocols

Speakers analyze technical capabilities across Claude. The architecture highlights reliable agent tool use, context window optimization, protocol standards, and seamless workflow interoperability.

```mermaid
flowchart TD

 A[User / Application Request] --> B[Model Context Protocol Server]

 B --> C[Claude Reasoning and Decision Loop]

 C --> D[Subagent Execution / Tool Call]

 D --> E[Verification and Final Output]

```

**Further reading:** Official documentation for Claude and Anthropic platform guides.

## Production Deployment, Verification, and Best Practices

Production readiness demands robust evaluation harnesses, state validation, and error-handling loops. Teams implement systematic monitoring and guardrails to ensure reliability across repeated executions.

**Further reading:** Official documentation for Claude and Anthropic platform guides.

## Organizational Impact, Scalability, and Industry Outlook

Deploying agentic systems transforms developer and team workflows by automating high-friction tasks. Organizations scale safely by pairing automated tool orchestration with structured human review.

**Further reading:** Official documentation for Claude and Anthropic platform guides.

## Source
Full cleaned transcript: `DATA/videos/long-running-agents-how-outtake-built-2026.json`
Canonical recording: https://anthropic.ondemand.goldcast.io/on-demand/d508adb2-979f-4efb-bbec-abd3ad285000?email=devofficialcoma@gmail.com&first_name=dev&last_name=Dev