# Build a Self-Evolving Agent: Autonomous Self-Improvement

**Speaker(s):** Annie Wang, Christina, Annie · **Channel:** Unlisted Videos · **Date:** 2026-08-20
**Watch:** https://www.youtube.com/live/nU2CnYbqI98?si=ARMTjIeA4ds7Hq9Y · **Format:** Talk · **Level:** Intermediate
**Topics:** AI Agents, Product/Startup

## TL;DR

A deep technical breakdown of Build a Self-Evolving Agent: Autonomous Self-Improvement, examining implementation architectures, operational workflows, and scalable cloud patterns utilizing Google Cloud.

## Contents

- [Strategic Overview and Core Architecture in Build a Self-Evolving Agent: Autonomous](#strategic-overview-and-core-architecture-in-build-a-self-evolving-agent-autonomous)
- [System Capabilities, Implementation Details, and Agent Integration](#system-capabilities-implementation-details-and-agent-integration)
- [Operational Workflows, Security Controls, and Scalability](#operational-workflows-security-controls-and-scalability)
- [Enterprise Impact, Practical Takeaways, and Future Directions](#enterprise-impact-practical-takeaways-and-future-directions)

---

## Strategic Overview and Core Architecture in Build a Self-Evolving Agent: Autonomous

Hello, welcome to the third episode of all things agent hackathon workshop where we deep dive into the technical
concepts to help you build better agents. Tell us uh where you are coming from joining us from. I'm Christina the
Google advocate from Boston and today we'll be going through the another super exciting 90 minutes of hands-on workshop
on evolving agents. My wonderful colleague Annie Wong will be taking you through the workshop. Annie, you want to come and say hi? My name is Annie and very excited to be here today. I'm very excited to have the self involving agent session with you today. Just a quick reminder for everyone um about the all things agentic hackathon.

---

## System Capabilities, Implementation Details, and Agent Integration

But the lab is only available for today. S, 48 secondsLooks like it takes a while for the setup to go through. While I'm waiting since you don't have more
s, 56 secondsquestions um I will come I will like direct back to my to my lab to
s, 5 secondsuh direct to my slide so that we can ex go through more concept
s, 13 secondsright so back to the theory part we just talked about how to evaluate the agent
s, 20 secondsand then uh we what we talked about before is we want to care about the agent trajectory because trajectory
s, 28 secondsmatters right you can you shouldn't only evaluate the result so ADK does provide
s, 35 secondsyou with tools to evaluate both the final response and the trajectory so if you take a look at this screen
s, 44 secondsthose are ADK's uh builtin metrics for you and on the left column it is uh
s, 51 secondsresponse match score and trajectory average score. Response score is basically to evaluate the response how
sdoes this response match the answer. You can see they have this title says needs a golden answer. On the left
s, 8 secondsleft hand uh side you need to have like a a golden data set basically your expected result and then you want to
s, 17 secondscompare the final answer with the expected result and then you want to evaluate how close the actual result
s, 24 secondscompared to the golden data set like the expected result. You want to evaluate the final response and we have another
s, 32 secondsthing called two trajectory average score that is to evaluate how the tool is used and what is the order that agent
s, 39 secondsis using the tool. You will also have a golden answer golden data set to say this is how I expect it to use 2 a use 2
s, 48 secondsfor later and then you will compare your actual to use to the expected to use and
s, 55 secondssee how close they are.

---

## Operational Workflows, Security Controls, and Scalability

You can like you can have many different type of input like many
s, 8 secondsdifferent group of people they have all different group of uh constraints restriction how do you know like it's
s, 15 secondsvery hard for you to generate a golden data set for all the different uh use
s, 22 secondscase right so in this scenario the final response is not sufficient in our uh
s, 31 secondsagent system we want to create our own evaluator to to measure how good the system is. Again, if we zoom out, we
s, 41 secondsneed to know how good the system is to keep involving the agent. I don't
s, 47 secondsthink this final response way is uh like if you keep good like if you're using this is like a very optimal way to
s, 56 secondsevaluate the system. That's why we want to create our own judge create our own
s, 4 secondsmetrics. Before we before we um going uh to this part I
s, 12 secondswant to like quickly check the group chat to see if you guys have any question. S, 18 secondsUh so I see Supria mentioned that for production environment for evaluation
s, 25 secondsany apart from ADK web and I think that's a good question. If you have it deployed you can also using ADK web
s, 33 secondsfor the production environment but it's not through the uh command. But for today's lab, if you get time to get to
s, 41 secondsthe later step, we also going to show you the evaluation for production agent.

---

## Enterprise Impact, Practical Takeaways, and Future Directions

So, I'm gonna go to this this page. :361 hour, 8 minutes, 36 secondsI'm going to copy this uh I'm going to copy this results. :451 hour, 8 minutes, 45 secondsI'm going to come into this. :511 hour, 8 minutes, 51 secondsOkay. So, if you have the same issue, you uh I'm currently do a hard refresh. :571 hour, 8 minutes, 57 secondsI'm doing a um to refresh the cache and let me paste it again. :061 hour, 9 minutes, 6 secondsagain like is it's generating a better restaurant that is supposed to fit for this group of people. The
:141 hour, 9 minutes, 14 secondswhole thing is we want to showcase a better instruction will have a better um
:201 hour, 9 minutes, 20 secondsgive a better uh result because um currently we're saying that uh we're creating the metric the everybody at
:281 hour, 9 minutes, 28 secondsmetric and then we are improving our agent by having a better instruction so that we have more test pass um than
:361 hour, 9 minutes, 36 secondsbefore.

---

## Source

Full cleaned transcript: `DATA/videos/build-a-self-evolving-agent-2026.json`
Original YouTube Video: https://www.youtube.com/live/nU2CnYbqI98?si=ARMTjIeA4ds7Hq9Y
