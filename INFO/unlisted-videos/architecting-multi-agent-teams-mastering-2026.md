# Architecting Multi-Agent Teams: Mastering the Three Orchestration Patterns

**Speaker(s):** Annie Wang, Christina · **Channel:** Unlisted Videos · **Date:** 2026-08-11
**Watch:** https://www.youtube.com/live/VaEYQU7z68g?si=rNWZpef0kJQPs7_O · **Format:** Talk · **Level:** Advanced
**Topics:** AI Agents, AI Coding Tools

## TL;DR

A deep technical breakdown of Architecting Multi-Agent Teams: Mastering the Three Orchestration Patterns, examining implementation architectures, operational workflows, and scalable cloud patterns utilizing Cloud Run, Google Cloud.

## Contents

- [Strategic Overview and Core Architecture in Architecting Multi-Agent Teams: Masterin](#strategic-overview-and-core-architecture-in-architecting-multi-agent-teams-masterin)
- [System Capabilities, Implementation Details, and Agent Integration](#system-capabilities-implementation-details-and-agent-integration)
- [Operational Workflows, Security Controls, and Scalability](#operational-workflows-security-controls-and-scalability)
- [Enterprise Impact, Practical Takeaways, and Future Directions](#enterprise-impact-practical-takeaways-and-future-directions)

---

## Strategic Overview and Core Architecture in Architecting Multi-Agent Teams: Masterin

Thanks for joining us live and being so patient with us, you know, with the slight delay and all that, but you know, like my grandma always tell me, good
things always takes a little bit more of a time. I'm not sure if it's just she's trying to keep me patient or whatever, but thanks you so much for joining me uh
for the first hands-on workshop for our all things all things agentic hackathons. I'm happy to be joined with me today with Annie Wong. I'm a developer rel relations engineer at Google Cloud. I'm very excited to join you today. So before we kick start, I just want to give you a quick reminder of our hackathon. Our hackathon
is due on August 31st. I know it sounds so far away, but sometimes, you know, things things get in the way, so I
always forget to submit.

---

## System Capabilities, Implementation Details, and Agent Integration

So,
s, 35 secondsif you only have a prompt on its own, it has no tools, no data. Um,
s, 42 secondsso which of this can it actually do? Can it tell you today's weather or tell you what to do with the weather or both? S, 49 secondsIt's a language model. I'm gonna say tell you what to do with the weather because it cannot tell you what is
s, 55 secondstoday's weather because um it doesn't connect to Google search or doesn't connect to uh weather API doesn't
s, 4 secondsconnect to external world it just model trying to making things up but it does it can do the reasoning so it can do um
s, 11 secondswhat you do with the weather so that's why if you put everything in the single uh prompt you you have some limitation
s, 20 secondsRight? You cannot uh one prompt you cannot trust it. You cannot easily test it and you cannot easily swap the step. S, 29 secondsYou need to modify the prompt.

---

## Operational Workflows, Security Controls, and Scalability

But
s, 56 secondsthere you can also choose to wrap the sub agent wrap the agent as a tool. If you're using the agent tool wrapper
s, 5 secondsuh you're basically putting the a you wrapping the agent as a tool and then that way you don't delegate all the
s, 12 secondscontrol to sub agent the the agent tool becomes uh stateless and it can be used as a tool and this is also very powerful
s, 21 secondsbecause um um like also you it's important to understand this so that you understand better about ADK2 uh ADK2
s, 30 secondsconcept So to summarize in the ADK1 the tools we have are LM agent. LMA agent are basically we have this native uh
s, 39 secondshierarchical tree pattern. You can delegate to the sub agent and often time you can use this as a router. ADK1 also
s, 46 secondsprovide sequential agent parallel agent and loop agent. S, 50 secondsUm and also ADK1 provide this agent tool. That those are all available in ADK 1.x. With 1.x X it's already very
spowerful to allow you to build a h build a like a agent system right
s, 7 secondsuh however in the real time situation you could imagine that if you want to build a workflow that you are only so so
s, 17 secondshere with a parallel agent you have three of them what if you have like three three a three agent you only want to run two of them in parallel and
s, 25 secondsanother one you do not you do not need to run them in parallel Or what if u you want to like run the sequential first and then the loop and then the parallel.

---

## Enterprise Impact, Practical Takeaways, and Future Directions

:381 hour, 5 minutes, 38 secondsUm, I'm going to go to the the code to show you
:551 hour, 5 minutes, 55 secondsworkflow. :571 hour, 5 minutes, 57 secondsYeah. Over here you can see that we are creating this workflow and this workflow
:051 hour, 6 minutes, 5 secondsit has three parallel agent this is join node and instead of now I'm going to agent strategy agent to uh make a
:141 hour, 6 minutes, 14 secondsdecision I'm having this route by weather u part this workflow and this workflow is I have this deterministic
:231 hour, 6 minutes, 23 secondsrouter so how does determinate router work is we have this route by uh weather deterministic
:311 hour, 6 minutes, 31 secondslogic. Here I have exact rule over here to decide how I delegate to the different different um specialists. :391 hour, 6 minutes, 39 secondsif it's larger than 70 go to the hot lower than 40 go to the code otherwise go to normal. I
:471 hour, 6 minutes, 47 secondscover all the edge cases and also it's fixed rule. Imagine you can put this to the prompt but again you do not need to
:551 hour, 6 minutes, 55 secondsput them in the prompt. If you put them in the prom it could work but you're basically wasting the token to give a not reliable result right so here we are
:041 hour, 7 minutes, 4 secondsusing this we creating this determinant logic and we're delegate to the corresponding um hot strategy normal
:111 hour, 7 minutes, 11 secondsstrategy and cold strategy agent and let's take a look at um how does that
:181 hour, 7 minutes, 18 secondslook if you go to the uh L2B in the in the lab L2 L2B task six L2B at
:291 hour, 7 minutes, 29 secondsthe deterministic router.

---

## Source

Full cleaned transcript: `DATA/videos/architecting-multi-agent-teams-mastering-2026.json`
Original YouTube Video: https://www.youtube.com/live/VaEYQU7z68g?si=rNWZpef0kJQPs7_O
