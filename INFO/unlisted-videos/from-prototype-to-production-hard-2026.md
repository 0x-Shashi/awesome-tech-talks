# From prototype to production: Hard-won lessons for advanced, reliable, and secure agents

**Speaker(s):** Isuru Raja · **Channel:** Unlisted Videos · **Date:** 2026-07-22
**Watch:** https://youtu.be/bZk6KCoTxMQ · **Format:** Talk · **Level:** Advanced
**Topics:** AI Agents, AI Coding Tools

## TL;DR

A deep technical breakdown of From prototype to production: Hard-won lessons for advanced, reliable, and secure agents, examining implementation architectures, operational workflows, and scalable cloud patterns utilizing Gemini, Gemini Enterprise, Gemini Enterprise Agent Platform, Google Cloud.

## Contents

- [Strategic Overview and Core Architecture in From prototype to production: Hard-won l](#strategic-overview-and-core-architecture-in-from-prototype-to-production-hard-won-l)
- [System Capabilities, Implementation Details, and Agent Integration](#system-capabilities-implementation-details-and-agent-integration)
- [Operational Workflows, Security Controls, and Scalability](#operational-workflows-security-controls-and-scalability)
- [Enterprise Impact, Practical Takeaways, and Future Directions](#enterprise-impact-practical-takeaways-and-future-directions)

---

## Strategic Overview and Core Architecture in From prototype to production: Hard-won l

My name is Isuru Raja Karuna. I'm a customer engineer at Google Cloud specialized in applied AI
and generative AI. In this session, we're going to cover very interesting topic which is about how do you move an
agentic use case from prototype to production and especially we are going to zoom in to that last mile gap
filling. These are the hard hardborn lessons from more than 70 plus customers and let's see what these uh real life use cases actually teach us. If you look at the challenges landscape, we can actually put everything into three buckets. Everyone almost everyone face uh faces challenges in uh when they integrate tool and data in a secure and
authenticated way. It's always a hard thing and people feel friction there. The other one is about agent evaluation.

---

## System Capabilities, Implementation Details, and Agent Integration

S, 17 secondsRather, I would like to stress this point and show you some examples how things can innocently go really wrong. So, let's get into some examples. S, 30 secondsThe first example that I picked out of the three examples that I uh chose for this session is the classic state
s, 38 secondssynchronization issue. This can happen a lot because you might end up deploying
s, 44 secondsan agentic uh application sharing states with existing applications in the text
s, 51 secondsstack. In this case uh I want to take a human in the loop scenario but this is not limited to just human in the loop. And this scenario is about an e-commerce company. Let's say an e-commerce company who got some
s, 8 secondswarehouses across the country like warehouse A, warehouse B like one is in Seattle, the other one is in Chicago and you have
s, 17 secondsjust deployed this nice agentic application who will uh which will produce a purchase order when the stocks
s, 24 secondsare running like when they are getting empty. In this case, let's say warehouse A got
s, 33 secondsthis zero out of 10,000 units for some item.

---

## Operational Workflows, Security Controls, and Scalability

They can write, read,
s, 52 secondsupdate from the state. This is a classic example of that and let's look at also how do we go about these kind of
sthings and and again this is not a golden solution but a way to avoid these kind of things
s, 7 secondsfor this uh we can make sure that all the references that goes into the agent goes into the human in the loop approval
s, 15 secondsprocess they are referring to a a refreshing state and and we have an
s, 22 secondsunderlying event-driven architecture to really synchronize across the different events. S, 29 secondsAnd even after approving, even after approving at the time of approval, the tool itself which is handling the
s, 38 secondsapproval process can revalidate if this state got a new update and what is their
s, 46 secondsnew condition and probably throw some error message and warning. You see that these kind of scenarios might not
s, 53 secondsbe captured right away in um in in your evaluation uh scenario set. To
s, 3 secondsgive you another example, let's look at uh attention think. This is another classic example of micro architectural problems. S, 13 secondsSay that um you are a developer who implement a really nice retrieval augmented generation based rag based
s, 21 secondssearch to search lot of low legal documents like there's a big repository of legal documents and this application
s, 28 secondsworks perfectly searching legal documents the performance is really good and let's say user wants to check if
s, 37 secondscertain type of considering certain type of agreements can we do this action a okay so this rag
s, 45 secondssystem actually went through everything and it found the perfect document to answer this question so once you found
s, 53 secondsthe document as an engineer you thought okay the we got the document so why not the top answer like why we can we can
s, 1 secondactually load that to Gemini model because it supports 1 million tokens why not right so see this graph shows you
s, 11 secondslike the xax axis is number of pages and the y-axis is attention. You can see that around 100 the page 152 there's a specific clause prohibiting this action.

---

## Enterprise Impact, Practical Takeaways, and Future Directions

S, 14 secondsOne is developers to end user journey around Gemini enterprise app. Gemini
s, 21 secondsenterprise app acts as a hub for your agentic use cases for your search use cases and even the applications like
s, 29 secondsnotebook lm. Not only that, you can actually deploy customuilt agent on agent platform runtime and connect
s, 38 secondsaccess wire Gemini enterprise. The governance and everything security is handled through that app which is the front uh front end for the users. As you
s, 48 secondscan see here, it got connectivity to agent garden uh other third party framework and uh support with agent protocols like A2A, MCP and so on. SBut the big picture looks like this. If you want to really remember what we do uh as Gemini enterprise agent platform,
s, 9 secondsyou can simply remember these four layers. At the build layer, you got
s, 16 secondsthe LLMs, third party models, agent development kit, and even we we have support for other agent frameworks.

---

## Source

Full cleaned transcript: `DATA/videos/from-prototype-to-production-hard-2026.json`
Original YouTube Video: https://youtu.be/bZk6KCoTxMQ
