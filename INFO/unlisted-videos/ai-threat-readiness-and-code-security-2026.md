# AI threat readiness and code security

**Speaker(s):** Google Technical Leaders · **Channel:** Unlisted Videos · **Date:** 2026-06-10
**Watch:** https://youtu.be/eZ1Fq5n9Rlg · **Format:** Talk · **Level:** Advanced
**Topics:** Backend/Infra, Web Development

## TL;DR

The rapid advancement of AI has dramatically accelerated vulnerability discovery and exploitation, shrinking the response window for security teams. To counter these threats, organizations must adopt a new approach to AI threat readiness focused on speed of action and broad visibility. This session will explore how to reduce external exposure and continuously scan applications with AI, automate patching to rapidly counter zero-day vulnerabilities, use advanced AI models to perform deep code analysis for complex logic flaws, and execute context-aware, automated threat containment in real time. Learn how implementing this continuous operational model allows you to secure your organization's environments at machine speed.

## Contents

- [Strategic Overview and Core Architecture in AI threat readiness and code security](#strategic-overview-and-core-architecture-in-ai-threat-readiness-and-code-security)
- [System Capabilities, Implementation Details, and Agent Integration](#system-capabilities-implementation-details-and-agent-integration)
- [Operational Workflows, Security Controls, and Scalability](#operational-workflows-security-controls-and-scalability)
- [Enterprise Impact, Practical Takeaways, and Future Directions](#enterprise-impact-practical-takeaways-and-future-directions)

---

## Strategic Overview and Core Architecture in AI threat readiness and code security

I lead platform product marketing at Whiz and I'm very excited to be here today to talk a little bit more about security in
an AI world. Now, you heard earlier today a bit more about the threat landscape and why AI threat defense is so important. On this conversation,
we're going to talk a little bit more about specifically what's changed, how we're thinking about AI readiness, as well as what's an overview of AI threat
defense specifically with Whiz. I'll actually end by bringing this to life in a quick demo. Now, we heard this earlier today, right? Hacking has changed and we have to think about security differently as a result. When we say this big bold statement that hacking has been democratized, we look at this from a few different lenses. Now, our research team here at
Whiz actually held a hacking competition in December.

---

## System Capabilities, Implementation Details, and Agent Integration

S, 8 secondsFind the right person to deploy that fix and move as quickly as possible. If we do this right for the first time, we'll achieve a world where fixing can
s, 16 secondsbe as fast as breaking. Now, one of the beauties here of us joining Google here at Whiz is that we're able to harness
s, 23 secondsthe ability of not only the amazing security team at Whiz, but the entire extended team at Google. We've come together to really bring this holistic
s, 31 secondsplaybook to you all to help you start to really put AI threat defense into practice. What I'm going to do is I'm going to walk through each of these four
s, 39 secondsstages where Whis can help you across each stage of this life cycle and then we'll take a look at what it looks like in practice with the demo. So, first
s, 48 secondswe're going to talk a little bit about prepare. Now, what I want to talk about prepare when we talk about eliminating exposures. There's two pieces I want us
s, 56 secondsto keep in mind here.

---

## Operational Workflows, Security Controls, and Scalability

Then we start to layer on
stop of this where do we start to see exposed risk? We can understand what's actually exposed to the internet. We can start to understand where there are misconfigurations, where there are
s, 9 secondsvulnerabilities. Then we start to layer those together to understand where are there actual real attack paths to crown jewels within your organization. S, 18 secondsfinally, what we can do is we can then start to prioritize on top of that, where am I truly exposed to exploitable risk. This is where we start to bring in
s, 27 secondsthe AI agent, our red agent, who is constantly and continuously scanning from the outside to help you prioritize
s, 34 secondsyour most critical risks. Now, we're seeing here that left to right an understanding of what I just walked through, right? Everything first and foremost that we've discovered where I'm
s, 42 secondsexposed, where there's risk, and then where are my priority attack paths I need to tackle first.

---

## Enterprise Impact, Practical Takeaways, and Future Directions

S, 10 secondsIt's organizing it as their services. S, 12 secondsSo, we can see some examples here. There's a number of different ones that maybe our team has built from. I want to
s, 20 secondsunderstand which ones may be a good candidate for one of those deeper code scans. For example, maybe I want to filter this down to only production
s, 28 secondsenvironment services and maybe ones that are using different AI technologies. S, 33 secondsNow, already I've started to focus this list down into just a handful of or of different services so that I know where
s, 41 secondsI want to start with those code scans. I can also pull different tags in. Maybe I want to pull in something like which ones are business critical so that
s, 49 secondsI can make sure that I'm applying the right model for that right use case.

---

## Source

Full cleaned transcript: `DATA/videos/ai-threat-readiness-and-code-security-2026.json`
Original YouTube Video: https://youtu.be/eZ1Fq5n9Rlg
