# Secure AI from Code to Cloud: Automating Your Defenses with Wiz

**Speaker(s):** Google Technical Leaders · **Channel:** Unlisted Videos · **Date:** 2026-08-06
**Watch:** https://www.youtube.com/live/mwHL8wcJoqQ?si=kRwCEm6WorOI-0HH · **Format:** Talk · **Level:** Intermediate
**Topics:** Backend/Infra, AI Coding Tools

## TL;DR

Innovation Shouldn’t Come at the Cost of Security

As your team innovates with AI, Large Language Models (LLMs), and autonomous agents, the attack surface is growing faster than your security team can keep up.

Lean teams wearing multiple hats often face the following challenges: 

The "Shadow AI" Risk: Unvetted models and tools are running in your environment without your knowledge.
Cloud Visibility Gaps: Your security tools see the cloud, but they don't understand your AI pipelines.
Development Bottlenecks: Security reviews are slowing down your deployment cycles with limited time to operationalize solutions.
In this session, you’ll learn how to implement an automated security operating model that keeps pace with your developers.

What you will learn:

Full-Stack AI Inventory: Automatically generate an "AI-BOM" to discover every model, agent, and service running in your GCP environment.
Toxic Combination Detection: Use the Wiz Security Graph to identify the critical paths - where an AI model’s access meets a vulnerable data bucket - that actually pose a real threat.
Developer-Led Remediation: See how to provide your developers with "Code-to-Cloud" context, allowing them to fix risks at the source before they reach production.

## Contents

- [Strategic Overview and Core Architecture in Secure AI from Code to Cloud: Automating](#strategic-overview-and-core-architecture-in-secure-ai-from-code-to-cloud-automating)
- [System Capabilities, Implementation Details, and Agent Integration](#system-capabilities-implementation-details-and-agent-integration)
- [Operational Workflows, Security Controls, and Scalability](#operational-workflows-security-controls-and-scalability)
- [Enterprise Impact, Practical Takeaways, and Future Directions](#enterprise-impact-practical-takeaways-and-future-directions)

---

## Strategic Overview and Core Architecture in Secure AI from Code to Cloud: Automating

Hello and welcome to secure AI from code to cloud. I'm a
solutions engineer here at Whiz. I'm based out of Northeast Pennsylvania. Over the past three and a half years,
I've specialized in helping growth and the SMB segment clients solve complex cloud security challenges and scale their security posture effectively. Outside of the tech space, I'm also an active leader in my community serving as captain on my local fire department. What we're going to cover today is really a quick overview of Whiz and really talk around the problem statement of why we created Whiz in the first
place. Then let's dive in to talk about the challenges in securing AI, automating defenses with Whiz, and we're
going to give a quick AI focused demo within the tool itself. From there, we'll flip back and talk around next steps and how we could continue this conversation.

---

## System Capabilities, Implementation Details, and Agent Integration

We are introducing whiz AI
s, 29 secondssecurity agents that work together seamlessly. We have our red agent which is a red teamer. It reasons like a real
s, 37 secondsattacker to discover and validate exploitable risks before our adversaries do. We have our blue agent or the sock
s, 45 secondsanalyst. It automates threat hunting and clears threat cues by validating alerts against full whiz telemetry. Then we
s, 53 secondshave our green agent. That's the S sur on our team. It converts security findings into actionable remediation strategies and automated code fixes to accelerate things like MTR.

---

## Operational Workflows, Security Controls, and Scalability

S, 35 secondsWe see a couple findings here as well, namely this authentication bypass via an arbitrary bearer token on databot API. S, 46 secondsSo, let's go ahead and take a look into that. This is where we start introducing our first agent, the red agent. Again, the red agent is that
s, 55 secondsautonomous redte teamer. It's looking at how we are externally exposed. It's probing all the different points of
s, 3 secondsexposure and then it's laterally moving uh or pivoting much like we would expect a thread actor to. So, as we open this
s, 13 secondsup, we could get a full view of what our red agent did. It looks like it's checking uh an API and it's checking for bearer token validation.

---

## Enterprise Impact, Practical Takeaways, and Future Directions

As we scroll further
s, 31 secondsdown, we're also once again seeing this investigation graph, right? What happened on this particular instance and
s, 40 secondswhat kicked off here that we need to remediate further. S, 44 secondsWe can see all the different detections here that our sensor, our runtime sensor picked up on just by monitoring at the
s, 52 secondsunderlying demon set level or at the underlying OS level. It looks like we went ahead, we correlated all these
s, 1 seconddifferent detections together and produced this cohesive threat. S, 7 secondsAs we move further up though, right, when we tell the story of a threat, seconds really matter. We want to make
s, 16 secondssure that we've done as much prep work as possible. By the time we're making a decision of do we potentially wake up at
s, 25 secondspeople at 3 in the morning, do we have a threat actor in our systems right now? S, 32 secondsAnd this is where we are going to introduce our final agent, the blue agent.

---

## Source

Full cleaned transcript: `DATA/videos/secure-ai-from-code-to-2026.json`
Original YouTube Video: https://www.youtube.com/live/mwHL8wcJoqQ?si=kRwCEm6WorOI-0HH
