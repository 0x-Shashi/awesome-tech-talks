# Customize your SOC with security agents using MCP servers

**Speaker(s):** Sandy · **Channel:** Unlisted Videos · **Date:** 2026-06-10
**Watch:** https://youtu.be/VrB0NCs-CIY · **Format:** Workshop · **Level:** Advanced
**Topics:** AI Agents, Backend/Infra

## TL;DR

Google is committed to leading the AI revolution not only by building the best models, but also by building the best ecosystem for those models and agents to thrive. Join this session to learn how to build and deploy multi-agent systems using the Google Security Operations Model Context Protocol (MCP) server and Agent Development Kit. We will show you how you can create your own security agents, tailored to your organization’s unique needs, using Gemini Enterprise Agent Platform and the Agent2Agent protocol. Discover how you can supercharge your existing security tools and APIs with AI agents and enterprise-grade governance, observability, and scalability.

## Contents

- [Strategic Overview and Core Architecture in Customize your SOC with security agents](#strategic-overview-and-core-architecture-in-customize-your-soc-with-security-agents)
- [System Capabilities, Implementation Details, and Agent Integration](#system-capabilities-implementation-details-and-agent-integration)
- [Operational Workflows, Security Controls, and Scalability](#operational-workflows-security-controls-and-scalability)
- [Enterprise Impact, Practical Takeaways, and Future Directions](#enterprise-impact-practical-takeaways-and-future-directions)

---

## Strategic Overview and Core Architecture in Customize your SOC with security agents

Hi, my name is Sandy and I am a customer engineer for Google Cloud Security and today I'm going to walk you through how to customize your security operations with security agents and MCP servers. Within this model we have build your own security agents. Within the middle you'll have your client which could be
uh Gemini CLI, you can have Gemini enterprise, you can use your agent development kit as well as what we offer
within the Google security operations platform. Within that they're going to have access to MCP servers which we do
host. You'll have the Google secops remote option of the MCP server as well as Google threat intelligence. If you have any other thirdparty solutions that
also have MCP servers or model context protocol they will be available to you as well. Typically when I speak to
customers that's going to be you know your crowd strikes octa whiz any sort of third party which would give you information and help you build those
security workflows that a lot of our customers are asking about. But before we do that, I'd like to take a big step back and just go through what is an
agent?

---

## System Capabilities, Implementation Details, and Agent Integration

What does this
s, 45 secondslook like from an abstraction perspective? I mentioned you know Gemini Enterprise the agent development kit. How does this all
s, 53 secondswork? We'll start with the bottom at the API layer. As I mentioned before, this is going to be heavily communicating with our Google Chronicle
s, 1 secondREST API. We also have the SECO ops wrapper, which is an SDK. Those are two available options in how we programmatically
s, 10 secondsuh interact with Google SECOPS. For this, we will be using the MCP remote servers.

---

## Operational Workflows, Security Controls, and Scalability

We're telling this agent to not take any action by itself. We still want to be in
s, 11 secondsthe loop and have any sort of notification, you know, notify human incident. As you can see here, in case we need to escalate this further to
s, 19 secondsanything else and then what I do like about this is as we keep going, we're able to actually have all the phases
s, 26 secondslisted out in in a lot of detail, but we get an a diagram as well. This diagram indicates to us all the steps that are going to be taken through all
s, 34 secondsthe different phases and the response that we should expect to see back to the user. It tells you all of the findings we need to do, what sort of um
s, 43 secondsexecute any sort of containment steps where we're going from endpoints to IoC to the user and any sort of playbooks that it's going to summize and report
s, 51 secondsback to the user to see if we can identify or be able to do more with that. That's just one example or one
s, 58 secondsuse case. Now we'll flip back to the presentation and kind of walk you through what happens in the background. S, 5 secondsSo now here is more of a visual in how this use case the first use case that we went through went.

---

## Enterprise Impact, Practical Takeaways, and Future Directions

Again, in the future, if I run into this, I can have the agent
s, 53 secondsgo through and say, "Hey, you actually ran into this before and here's the summary of that. Here is all of the relevant information and artifacts from
s, 1 secondthe last time that this happened." And then again, we're having the human in the loop here, the recommended actions. S, 7 secondsIt's telling me I need to isolate this host and I need to audit different artifacts within this and also reset credentials for this user. It's not
s, 15 secondsgoing out and doing that. Maybe the next uh actual demo I do, I'll have it be fully autonomous, but I still want human in
s, 23 secondsthe loop for this. So, I'm going to go through and reset the credentials for J Smith. Again, it's telling me what MCP tools that it actually used to
s, 32 secondsidentify the malicious traffic. Again, I'm going to say, "Wait a minute.

---

## Source

Full cleaned transcript: `DATA/videos/customize-your-soc-with-security-2026.json`
Original YouTube Video: https://youtu.be/VrB0NCs-CIY
