# Architecting Agent Memory: Session State, Vector Search, and Managed Cloud Memory

**Speaker(s):** Rahman Irani · **Channel:** Unlisted Videos · **Date:** 2026-08-28
**Watch:** https://youtu.be/jGkA3aWzDGA · **Format:** Talk · **Level:** Intermediate
**Topics:** AI Agents, Android/Mobile

## TL;DR

A deep technical breakdown of Architecting Agent Memory: Session State, Vector Search, and Managed Cloud Memory, examining implementation architectures, operational workflows, and scalable cloud patterns utilizing BigQuery, Google Cloud, Vertex AI.

## Contents

- [Strategic Overview and Core Architecture in Architecting Agent Memory: Session State](#strategic-overview-and-core-architecture-in-architecting-agent-memory-session-state)
- [System Capabilities, Implementation Details, and Agent Integration](#system-capabilities-implementation-details-and-agent-integration)
- [Operational Workflows, Security Controls, and Scalability](#operational-workflows-security-controls-and-scalability)
- [Enterprise Impact, Practical Takeaways, and Future Directions](#enterprise-impact-practical-takeaways-and-future-directions)

---

## Strategic Overview and Core Architecture in Architecting Agent Memory: Session State

Thank you for joining us for this uh session today. This is the fourth uh session in our series for architecting real world uh ADK agents. Uh today we are going to be talking about uh you know agent memory. Far we've seen uh you know uh levels of how
we've built out ADK agents using collaborative patterns. Then we've looked at longunning agents. Then we also looked at a self-improving agent
and how do you do agent evaluations and today we'll be looking at agent memory. I work as a develop advocate at Google cloud. I'm happy to take you through today's uh session.

---

## System Capabilities, Implementation Details, and Agent Integration

So that
s, 23 secondsis why uh this scenario is there. For example, you'll see that if the context window gets full on the left side as
s, 30 secondsit's shown, you it might end up that it was able to answer a while back, but now it seems to have dropped it and it's forgotten it because it tried to just
s, 38 secondsfit everything in memory. This problem can be well addressed by a state. So you can see on the right
s, 47 secondsside what it has actually done is that whenever the conversation had relevant pieces that you want to save and which
s, 54 secondsyou actually do that in your code you use your code to create certain kinds of I would say a map or a state variables which you're seeing where you're
s, 2 secondsactually saving you know for example if someone said hey my ticket number is 8841 and I've bought this product and it's flickering has an issue you're
s, 10 secondsactually classifying them into symptoms a product and order number as you're seeing and saving that in your state so
s, 17 secondsthat even if you go successively to more you know a large number of turns later
s, 23 secondson it can your code can still tap into the uh state and get you the values right so that's that's pretty much how
s, 32 secondsuh or or basically why you would need a state in the uh first place now uh the state again as I mentioned it could
s, 39 secondsremain in your memory or you could say I'll persist it to a database so that it's available to me later on even across restarts and so on. That's
s, 48 secondsexactly what we'll see in our first set of uh code examples but I'm just summarizing it over here which is that
s, 56 secondsMaya which is us the user just goes in and says I'm having an issue with this product and this is my order number. S, 4 secondsthe the model or the sorry the agent actually uh takes that information and creates three kinds of uh variables or
s, 13 secondsuh you know the state information. Ticket order number, product and symptom right and it saves it into a state and
s, 20 secondsthat can also be persisted in a database which we will see. Now keep in mind state is just picking out specific
s, 27 secondsvalues.

---

## Operational Workflows, Security Controls, and Scalability

So, now that I've saved this, it just didn't have the right import, and that's what
s, 18 secondsthe error was. Uh, I'm just going to go back here. S, 28 secondsSo, we're going to be starting our ADK web again. This time, if I'll just do a refresh here, uh I could just say create a new session for the R2 handoff. S, 39 secondsAnd um let's go back and pick that prompt again. It's going to again set the right uh you know variables in the state and see a small thing if you noticed
s, 57 secondsthat this time it's a longunning transaction. You'll actually see that it created another sort of a field over
s, 4 secondshere which says if you want you can approve it from here for your testing purposes and that's exactly what this lab actually says that you will see that
s, 13 secondsit appears for a longunning tool. You can uh put the value over here just says approved.

---

## Enterprise Impact, Practical Takeaways, and Future Directions

That at this point in time, we're going to be adding this session to memory. It distills some information from it and adds it to the memory. :161 hour, 6 minutes, 16 secondsSimilarly, recall uh so which is the tool when it is called which is going to be uncommenting out this part. That
:251 hour, 6 minutes, 25 secondsit first gets the you know any past conversations and if yes it actually takes it from there and shows you the
:321 hour, 6 minutes, 32 secondspast conversation. It will not be empty now at least you'll have a past few conversations going on. I'm going to close
:411 hour, 6 minutes, 41 secondsthis uh and I'm going to see what it tells me to do which is to relaunch it after the changes that we've made. :541 hour, 6 minutes, 54 secondsAnd then what does it uh tell you to do? :561 hour, 6 minutes, 56 secondsIt tells you to do the some some of the similar things which is that okay the same one the updated fixed it and uh please close my ticket.

---

## Source

Full cleaned transcript: `DATA/videos/architecting-agent-memory-session-state-2026-2.json`
Original YouTube Video: https://youtu.be/jGkA3aWzDGA
