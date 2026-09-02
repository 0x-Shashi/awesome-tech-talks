# Build a Self-Evolving Agent: Autonomous Self-Improvement 2

**Speaker(s):** Rahman Irani · **Channel:** Unlisted Videos · **Date:** 2026-08-21
**Watch:** https://www.youtube.com/live/GYfVyl-Kpuw?si=ZgFsdABALQp4-YH- · **Format:** Talk · **Level:** Intermediate
**Topics:** AI Agents, AI Coding Tools

## TL;DR

A deep technical breakdown of Build a Self-Evolving Agent: Autonomous Self-Improvement 2, examining implementation architectures, operational workflows, and scalable cloud patterns utilizing BigQuery, Gemini, Google Cloud.

## Contents

- [Strategic Overview and Core Architecture in Build a Self-Evolving Agent: Autonomous](#strategic-overview-and-core-architecture-in-build-a-self-evolving-agent-autonomous)
- [System Capabilities, Implementation Details, and Agent Integration](#system-capabilities-implementation-details-and-agent-integration)
- [Operational Workflows, Security Controls, and Scalability](#operational-workflows-security-controls-and-scalability)
- [Enterprise Impact, Practical Takeaways, and Future Directions](#enterprise-impact-practical-takeaways-and-future-directions)

---

## Strategic Overview and Core Architecture in Build a Self-Evolving Agent: Autonomous

Thank you for joining us for another session today in how we see how to build out uh you know real world
agents. We've been seeing so far uh how we've uh built out agents using different uh patterns in ADK. We've also
looked at state management and today we'll be looking at another interesting uh you know area in which what we are calling as self-evolving agents with
ADK. But if you break down this a bit uh it's also about um you know just understanding what it means to build out
an agent uh which is uh you know uh working well which we know is meeting our requirements and what does it mean
also to see how that agent can evolve itself over time with new edge cases correct itself uh into a whole thing
with workflow. I work as a Google cloud uh developer advocate and I'm happy to take you through this
session today. Let's get started with it and uh first up right we're going to be discussing what is it that we are
going to be solving today using our agents. If you look at this it's a dinner party and uh they're going to be
uh you know the party would consist of a few uh you know friends meeting together. Our goal is going to be to
build out an agent that helps uh you know select the right you know uh hotel or restaurant uh for this party to
happen where they can have their uh dinner.

---

## System Capabilities, Implementation Details, and Agent Integration

You will see there are different steps 01 02 03. That's how we will go and see many things. We will see initially how the whole thing works. S, 39 secondsThen we will see how do we create uh these evaluations. How do we create the optimize loop using ADK optimize and
s, 48 secondsthen of course uh reward hacking. If we set the wrong criteria you will end up seeing that everything is successful. S, 54 secondsSo how to avoid those situations and then of course we'll also be seeing the whole workflow and then finally pushing
s, 2 secondsit into production and harvesting any errors from that point. We'll see all of this code in a while.

---

## Operational Workflows, Security Controls, and Scalability

But if you've got many answers uh and probably there's a different way to evaluate that
s, 56 secondsthen you might need a judge that checks the answer that you can't do like a simple comparison out here. That's what this says that in in case there are
s, 4 secondsmany answers or probably a different criteria like whether everyone ate or no then obviously you need a judge that is
s, 11 secondschecking whether you know it's meeting the criteria or not. That's really the next level we want to go to. Here is
s, 18 secondsuh what the next task says that we are going to be building out this judge. We we're going to be building out our own
s, 25 secondscustom uh you know metric and as I told you uh there is this whole method that we've created earlier I showed you in
s, 34 secondsworld.py called everyone 18 but in 02 let's see for a moment and it should become clear. We go to editor and uh
s, 42 secondswe are in 02 as you can see over here and if you go to the world.py file you
s, 50 secondswill also see something called everyone ate and this is a key function that we have written. We've said here's a party
s, 57 secondsID, here's a restaurant, here's a time, then you know please go through each of
s, 4 secondsthose persons in the party and then find out whether they ate or not. If the each
s, 11 secondsone of them has eaten obviously the Y would be empty but if not they're going to be appending all these Y reasons that
s, 18 secondsmaybe could not due to food not being there of the kind they wanted or maybe the timing did not work or the budget did not work could be a variety of
s, 27 secondsreasons.

---

## Enterprise Impact, Practical Takeaways, and Future Directions

:591 hour, 10 minutes, 59 secondsSo, if I just go back to the lab, it says ideally we should be seeing all of this. Basically every table every seat the judge never moved right. Uh
:081 hour, 11 minutes, 8 secondsit it's really what is the lever we use we use the thinking budget now to see now again is this the right way to do it
:161 hour, 11 minutes, 16 secondsalways that again is a is a thing you should be looking at whether it's indeed the way you would want this to do you
:231 hour, 11 minutes, 23 secondswant some other evaluations you'll have to probably see it on uh those factors also correct so let's go to that and
:321 hour, 11 minutes, 32 secondshere you see that the tests have passed so we basically change the we took an optimized instruction set and instead of
:411 hour, 11 minutes, 41 secondschanging we didn't change the judge we didn't change our evaluation criteria we did something more to the agent which is to give it a little bit more reasoning
:491 hour, 11 minutes, 49 secondsto make sense of the optimized instruction and see if it's able to meet the criteria and that's indeed what the results out here say. Again, this
:581 hour, 11 minutes, 58 secondssummarizes stuff very well that though this is ending at a real 88, right? :031 hour, 12 minutes, 3 secondsThere were three ways to turn the six that we got into an 88. We change the level, which is what we did. It's really probably one of the okay ways to do it. :141 hour, 12 minutes, 14 secondsWe did not change the exam.

---

## Source

Full cleaned transcript: `DATA/videos/build-a-self-evolving-agent-2026-2.json`
Original YouTube Video: https://www.youtube.com/live/GYfVyl-Kpuw?si=ZgFsdABALQp4-YH-
