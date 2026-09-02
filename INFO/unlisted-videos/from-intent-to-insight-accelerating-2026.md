# From intent to insight: Accelerating outcomes with Data Agent Kit

**Speaker(s):** Google Technical Leaders · **Channel:** Unlisted Videos · **Date:** 2026-07-21
**Watch:** https://www.youtube.com/live/u7AOVe11HeA?si=hM996eSYkG3JU-Io · **Format:** Talk · **Level:** Intermediate
**Topics:** AI Agents, Backend/Infra

## TL;DR

A deep technical breakdown of From intent to insight: Accelerating outcomes with Data Agent Kit, examining implementation architectures, operational workflows, and scalable cloud patterns utilizing BigQuery, Gemini, Google Cloud, Spanner.

## Contents

- [Strategic Overview and Core Architecture in From intent to insight: Accelerating out](#strategic-overview-and-core-architecture-in-from-intent-to-insight-accelerating-out)
- [System Capabilities, Implementation Details, and Agent Integration](#system-capabilities-implementation-details-and-agent-integration)
- [Operational Workflows, Security Controls, and Scalability](#operational-workflows-security-controls-and-scalability)
- [Enterprise Impact, Practical Takeaways, and Future Directions](#enterprise-impact-practical-takeaways-and-future-directions)

---

## Strategic Overview and Core Architecture in From intent to insight: Accelerating out

Good morning everyone or good afternoon, good evening wherever you may be and welcome to today's webinar from intent
to insight exhilarating outcomes with data agent kit from Google cloud. My name is Arun Nyer and I am the product manager for data agent kit. Today's webinar is quite hands-on and we will be spending most of the time on a detailed demo of data agent kit. I will
kick things off with a quick introduction of what data agent kit is for those of you who may not be familiar. We will then describe a very
representative data engineering/data science scenario that you may run into in your job as data practitioners. We will then demo how you can use data agent kit to tackle the scenario with ease. Finally, we will wrap things up
with the recap of the presentation and Q&A. So, what is data agent kit?

---

## System Capabilities, Implementation Details, and Agent Integration

Here we see that the um the
s, 8 secondswhole DBT pipeline is being uh generated for us. As you see the source and
s, 16 secondsthe models are being added as SQL and YAML files on the left side to my uh project folder. S, 35 secondsNow the next step for me would be to compile and build that DBT pipeline. What I wanted to do is make sure that I
s, 43 secondsactually have the DBT um tool installed in my uh in my local Python environment. I created a
s, 52 secondsvirtual Python virtual environment. I pip installed the dbt tool and then now I'm ready to run dbt build to build that
s, 59 secondsdbt pipeline. Here the dbt pipeline is been built and if engine has done a great job the
s, 7 secondsthe dbt pipeline compiles and uh builds with no error. S, 22 secondsAll right, as you can see the pipeline completed successfully.

---

## Operational Workflows, Security Controls, and Scalability

Then uh we train an ML model on a spark to detect fraudulent
s, 17 secondstransactions. Then we use that chain model to do batch inferencing again on a
s, 23 secondsspark and deposit uh fraudulent transactions or potentially fraudulent transactions in in a review queue in a
s, 32 secondsspanner. Finally, we orchestrated the entire pipeline using manager flow. S, 39 secondsSo you can start getting your hand dirty with data agent kit. It's actually very easy to use it if you're using VS code
s, 47 secondsanti-gravity cursor or any other VS code fork. You can download it uh by searching for data agent kit in the
s, 56 secondsextension marketplace. You don't need to directly download and install it. You can just go to the extension marketplace
s, 2 secondsfor your ID.

---

## Enterprise Impact, Practical Takeaways, and Future Directions

S, 34 secondsYou describe what you wanted to do your use case and agent navigates you through
s, 41 secondsa scaffolding you know the go the golden architecture or the optimal architecture for that. Once you have the architecture, you have to usually either
s, 49 secondsmigrate the code, rewrite the code or migrate the data and
s, 56 secondsdata agent kit has facilities to help you with this task. For example, you
s, 2 secondshave code that's written in another SQL dialect. Now you wanted to convert it to
s, 9 secondsrun on BigQuery and data agent kit can help you with that. The same for other type of workloads that you have. For
s, 17 secondsexample, you have PIS spark code that's written for another spark uh for another spark provider. You wanted to update it to run and manage service for Apache Spark that Google data cloud offers. S, 28 secondsAgent is capable of that and we are constantly adding uh skills to it that helps you migrate a
s, 37 secondsspecific workloads from a specific providers to Google Cloud.

---

## Source

Full cleaned transcript: `DATA/videos/from-intent-to-insight-accelerating-2026.json`
Original YouTube Video: https://www.youtube.com/live/u7AOVe11HeA?si=hM996eSYkG3JU-Io
