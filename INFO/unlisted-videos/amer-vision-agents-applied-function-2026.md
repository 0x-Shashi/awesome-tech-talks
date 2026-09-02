# [AMER] Vision Agents & Applied Function Calling

**Speaker(s):** Google Technical Leaders · **Channel:** Unlisted Videos · **Date:** 2026-06-16
**Watch:** https://www.youtube.com/live/hhm-mfWefNY?si=kQxvoyULycdzpZDT · **Format:** Talk · **Level:** Intermediate
**Topics:** AI Agents, Product/Startup

## TL;DR

An agent must be able to take action. In our second intermediate class, we bridge the gap between processing information and executing workflows. We will explore how to implement bidirectional Vision capabilities, allowing your agent to ""see"" specific external web pages - like a user profile or a complex report - to instantly extract structured information. We will then tie this to real-time function calling, teaching you how to build human-in-the-loop systems where the AI seamlessly triggers backend workflows and automatically updates your application's database based on what it sees and hears.

## Contents

- [Strategic Overview and Core Architecture in [AMER] Vision Agents & Applied Function](#strategic-overview-and-core-architecture-in-amer-vision-agents-applied-function)
- [System Capabilities, Implementation Details, and Agent Integration](#system-capabilities-implementation-details-and-agent-integration)
- [Operational Workflows, Security Controls, and Scalability](#operational-workflows-security-controls-and-scalability)
- [Enterprise Impact, Practical Takeaways, and Future Directions](#enterprise-impact-practical-takeaways-and-future-directions)

---

## Strategic Overview and Core Architecture in [AMER] Vision Agents & Applied Function

Are you ready for the next startup school? Good morning, good afternoon, good evening from wherever you are joining us today. This is Dimmon, your host, your MC. Um, and this
is Startup School week two. I'm super happy to welcome you and I'm super happy to see so many of you again. I'm happy
you're still with us. Uh, we are kicking off the second week as I said with vision agents and applied function calling. That's the topic for today's
class.

---

## System Capabilities, Implementation Details, and Agent Integration

You can
s, 16 secondsprovide your own names um with like the same API schema we use for like the built-in agents. An agent can have um instruction. S, 26 secondsThe environment can be scaffolded with sources. Files from a GCS bucket, files from a GitHub repository or you
s, 34 secondscan create agents from a previous environment. If you have one like scaffolding agent which does all of the
s, 41 secondsheavy lifting on like installing a CLI, setting up um some folders, some files like the structure you want to have it,
s, 48 secondsyou can like use the the created environment from that agent as the base environment for new agents. When you define it as the base environment for
s, 57 secondsnew agent, every new request will basically fork from that uh pre-built environment and has like a clean uh environment for it to use. S, 7 secondsAnd to make all of that work easier for you, we um also created a small Gemini API CLI. S, 16 secondsThat's a a CLI for you to call the Gemini API or to create agents or to test agents using other coding agents.

---

## Operational Workflows, Security Controls, and Scalability

We're kind of like a
s, 10 secondsspecial team inside of Google Cloud where we basically build relationships with founders out there and we also get to talk a lot about technology like some of the stuff I'll talk about today. S, 22 secondsLet me just jump right in. So, I'm going to give a slight recap to session two and uh as you may know if you've been
s, 30 secondsfollowing the series uh uh Shai and and some of the other folks were working on building the hero app and uh they the
s, 37 secondsthe last session was about adding memory and I'll show a little bit about that in a second. But now we are trying talking about vision and we're going to
s, 45 secondsget into how we can add vision to the hero application. We're going to show some use of vision inside of AI Studio and we're going to show what the new
s, 53 secondshero app looks like with vision. We're going to talk about the vision architecture and we're going to talk a little bit about applied function calling towards the end. S, 1 secondSo in in in in part two um basically uh what we're what we're looking at is that
s, 9 secondssoftware is now very different than where it was before. Um, not only are we able to talk to software systems now,
s, 17 secondsbut now they're able to listen and take action and now they're able to uh
s, 24 secondsactually remember things about us as we communicate with them.

---

## Enterprise Impact, Practical Takeaways, and Future Directions

:491 hour, 4 minutes, 49 secondsYeah. Do you see anything else interesting in the background behind me? :531 hour, 4 minutes, 53 secondsFor sure. I can also see a white bowl and that round black object, maybe a speaker. The built-in shelving has a
:021 hour, 5 minutes, 2 secondsreally nice natural wood texture. You seem to really appreciate aesthetics, actually. But you don't see a soccer ball back there. :121 hour, 5 minutes, 12 secondsLike, oh my gosh, yes.

---

## Source

Full cleaned transcript: `DATA/videos/amer-vision-agents-applied-function-2026.json`
Original YouTube Video: https://www.youtube.com/live/hhm-mfWefNY?si=kQxvoyULycdzpZDT
