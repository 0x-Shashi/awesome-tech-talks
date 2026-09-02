# Choice and control: Unified access and Agent routing with Gemini Enterprise Agent Platform

**Speaker(s):** Google Technical Leaders · **Channel:** Unlisted Videos · **Date:** 2026-07-22
**Watch:** https://youtu.be/wNDCVaRenSU · **Format:** Talk · **Level:** Intermediate
**Topics:** AI Agents, Product/Startup

## TL;DR

A deep technical breakdown of Choice and control: Unified access and Agent routing with Gemini Enterprise Agent Platform, examining implementation architectures, operational workflows, and scalable cloud patterns utilizing Gemini, Gemini Enterprise, Gemini Enterprise Agent Platform, Google Cloud.

## Contents

- [Strategic Overview and Core Architecture in Choice and control: Unified access and A](#strategic-overview-and-core-architecture-in-choice-and-control-unified-access-and-a)
- [System Capabilities, Implementation Details, and Agent Integration](#system-capabilities-implementation-details-and-agent-integration)
- [Operational Workflows, Security Controls, and Scalability](#operational-workflows-security-controls-and-scalability)
- [Enterprise Impact, Practical Takeaways, and Future Directions](#enterprise-impact-practical-takeaways-and-future-directions)

---

## Strategic Overview and Core Architecture in Choice and control: Unified access and A

I hope you had a good session uh right before this. Now, we're going to be talking about choice and control uh which is around routing
your agents and providing access to them in the Gemini Enterprise Agent Platform. I'm a forward deployed engineer at Google Cloud um working on the Gemini Enterprise Agent Platform. We've we've seen this slide not not too long ago. We'll be focusing on uh the gateway as part of the govern capability
and kind of what powers it and how it all kind of stitches together. Before we really start the important thing is to kind of set the context right as the era of AI has kind of
changed the way we worked and how developers worked there's been a lot of intention to create AI agents and make
them part of everyone's workflow and um part of our enterprise organizations. Now as that technology grew the applications the experiments of different organizations has also gone up
with that but while technology changes exponentially organizations tend to change logarithmically and so there's this gap there's this chasm that we're
trying to fill um and say how do we take all of these advances in technology and
kind of map them to the way we're running our organization and our technical organizations today. When we think about agent governance, there's a lot of things um that that we tend to think about um at a higher level, right?

---

## System Capabilities, Implementation Details, and Agent Integration

Is it for this use case, that use case, etc. Different user personas can make agents. S, 56 secondsUm maybe they could be vendors in your organization. Maybe it could be internal teams. It could be applying to a broad set of people, a smaller set of people,
s, 3 secondscould be connected to some data that some teams can access and other data sources that other teams can't access. There's this massive sprawl in this um incredibly fragmented uh landscape of agents, right? How do
s, 17 secondswe think about creating management layers across that so that we could have some level of control and supervision
s, 25 secondsabout what's happening uh and and how these agents are built. S, 30 secondsSo the first thing we think about especially when we think about agents as first class um citizens in our uh technical organization is agent
s, 39 secondsidentity.

---

## Operational Workflows, Security Controls, and Scalability

S, 17 secondsSo each agent that has its own identity, we want to be able to find out where they are and um how to access them and
s, 24 secondseven just visualize and count them, you know. So we have this thing called an agent registry. All agents deployed directly from Gemini Enterprise or agent
s, 32 secondsruntime will be available within this registry. As we've talked about earlier, you could also register 8way and non-2A agents directly on the registry um
s, 41 secondswithin the console. But we also auto deploy based on like which which technology or which part of the stack you're already using. The agent
s, 50 secondsregistry is basically a single pane of glass where you can see all their agents uh the properties of those agents, their identity, etc. At the same time, it's
s, 58 secondsalso a place where you can check um MCP servers, endpoints, and eventually skills. Oh,
s, 6 secondsnow everything on the registry uh basically is governed by by a certain set of policies meaning um you can say
s, 16 secondsthis agent can access this agent like and make this discussion.

---

## Enterprise Impact, Practical Takeaways, and Future Directions

S, 17 secondsSo, we'll go very quickly through a uh demo on on how this works. S, 24 secondsSo, we have our agent gateway demo within the Gemini Enterprise agent platform. You can think of uh in this demo, we have an orchestrator agent. S, 31 secondsGemini enterprise uh that is have a single agent. The client side will be Gemini enterprise the application. Now agent gateway will
s, 39 secondsensure that the right user can access this agent. The agent is inside agent runtime where it has an existing agent identity
s, 47 secondsand flight and the agent gateway once again will check which then calls if this agent can access certain MCP servers. That's their email MCP
s, 56 secondsserver, their document management MCP server and their income verification additional policies to so all the tools here you'll see will be
s, 3 secondspart of the agent registry and all the policies that are defined will be enforced by that policy saying that as an example this agent can question.

---

## Source

Full cleaned transcript: `DATA/videos/choice-and-control-unified-access-2026.json`
Original YouTube Video: https://youtu.be/wNDCVaRenSU
