# Beyond the GPU: Maximizing goodput with self-healing AI infrastructure

**Speaker(s):** Benazie Fatai · **Channel:** Unlisted Videos · **Date:** 2026-06-16
**Watch:** https://www.youtube.com/live/CE3cAkqvDZA?si=-I21usS-cZlPbhDf · **Format:** Talk · **Level:** Intermediate
**Topics:** Backend/Infra, AI Agents

## TL;DR

A deep technical breakdown of Beyond the GPU: Maximizing goodput with self-healing AI infrastructure, examining implementation architectures, operational workflows, and scalable cloud patterns utilizing Cloud Run, Compute Engine, Gemini, Gemini Enterprise.

## Contents

- [Strategic Overview and Core Architecture in Beyond the GPU: Maximizing goodput with](#strategic-overview-and-core-architecture-in-beyond-the-gpu-maximizing-goodput-with)
- [System Capabilities, Implementation Details, and Agent Integration](#system-capabilities-implementation-details-and-agent-integration)
- [Operational Workflows, Security Controls, and Scalability](#operational-workflows-security-controls-and-scalability)
- [Enterprise Impact, Practical Takeaways, and Future Directions](#enterprise-impact-practical-takeaways-and-future-directions)

---

## Strategic Overview and Core Architecture in Beyond the GPU: Maximizing goodput with

Hello and welcome to the beyond the GPU session. Today this is going to be all
about the model building exercise of what it takes to actually build and produce a high quality model. We'll be
walking you through uh what that journey looks like, how should you be thinking about using the Google AI infrastructure
and the value of a self-healing AI infrastructure. Then uh we are going to close out with some of the learnings
and outcomes that our customers have been able to achieve by using our AI infrastructure and close out with how you can get started. With that, let me quickly introduce myself. I'm a global practice lead for AI at Google
and I'll be joined by Benazie Fatai who is a technical solution manager with our applied AI engineering team u and we'll
be taking us through a deep dive including a demo of what this uh self-managed AI infrastructure looks like and then I will have Kuraj who is
our AI practice lead for Americas and he will walk through some of the customer outcomes and then how do you get started. We'll be now before we talk about what it takes to actually create or um you know build
a genai model, let's talk a little bit about what are we seeing out there from a customer vantage point. So a lot of
uh customers are sort of adopting AI specifically generative AI to produce highquality agents right and a key
pattern that we see is customers sort of using their own proprietary data to create a very domain specific model that
s, 4 secondsis focused on higher efficiency better outcomes and is really their own sort of proprietary right and we see a lot of
s, 13 secondsdifferent use cases.

---

## System Capabilities, Implementation Details, and Agent Integration

S, 30 secondsYou can use a preconfigured cluster setup or you can customize your own DIY cluster for your training workload. We
s, 38 secondshave also created some agentic skills to have your coding agents configure, manage and delete a cluster in an automated and er error-free way. S, 50 secondsTraining clusters support a wide range of accelerators uh which is including but not limited to H100, H200, B200's,
s, 58 secondsGP200s, RTX Pro 6000 as well as TPUs such as V5P, V6 and V7. You can use and combine
s, 9 secondsexisting reservations in your projects with DWS capacity as needed. S, 14 secondsAnd these clusters once they are created, they are preconfigured with optimized networking and storage and topology aware scheduling. S, 24 secondsOnce your cluster is set up, we also have scripts to make the cluster management, cluster deletion or cluster redeployment easy. Our customers have
s, 33 secondsbenefited greatly from these uh C cluster creation and management scripts and they've mentioned that this has brought down their cluster redeployment time from hours to minutes. S, 47 secondsNow let's look at the underlying architecture of this slurm cluster which we provision using a simple API call
s, 55 secondsrather than having you to manually configure dozens of complex individual components.

---

## Operational Workflows, Security Controls, and Scalability

S, 24 secondsSo on the observability pan for panel for GPU you can see for different time
s, 31 secondsuh intervals you can see uh metrics for GPU utilization, memory utilization as well as power
s, 38 secondsconsumption down here. [snorts] now that our cluster is set up uh now we would the next step we would do is we
s, 51 secondswould run an Nvidia u Neotron 3 nano nano model using Megatron bridge. S, 59 secondsSo as step one we will create a Python um u uh virtual environment
s, 6 secondsand then following that we will take the Nvidia Nemo container image and because this is a slurm based cluster
s, 15 secondsuh this image the Nemo container image needs to be converted into an unprivileged sandbox format. S, 22 secondsAs part of our recipes, we provide this script to convert the Nemo container image into uh this uh sandbox image. S, 31 seconds[snorts] And once that is done using the script, you will now then as a next step, you will clone the Megatron Bridge
s, 40 secondsrepository um into your uh CPU login node uh or your workspace. S, 47 secondsOnce that is done, the next step would be to download the Neotron Nano3 30 billion model from hugging face. S, 56 secondsSo you'll download that model from hugging face. Once that model is downloaded, you would be uh converting
s, 3 secondsit into a Megatron core format um in this case um and then using our
s, 11 secondsscript for fine-tuning this Neo Neotron Nano3 model.

---

## Enterprise Impact, Practical Takeaways, and Future Directions

We have pre-created these
s, 28 secondsrecipes which Benzil walked you through that you can leverage and accelerate the time to market. The third one is the capacity utilization. S, 40 secondsOverprovisioning is a very critical uh thing that happens in these kind of training which results in significant
s, 48 secondswastage of both the capex as well as the utilization of the resources. S, 54 secondsFlexible model, consumption models which we spoke about can ensure you are spending the right amount of your
s, 2 secondsresources and the cost for the right job. The last but not the least is the time to market. Because of
s, 10 secondsthe fully managed service that we are able to provide to you, you not only reduce the operational burden but also enable quick deployment as you deliver
s, 19 secondsto your customers. What we have heard from customers on why you know they are choosing Google cloud. All right to
s, 27 secondssummarize people are choosing Google cloud to build the future of AI for five key elements.

---

## Source

Full cleaned transcript: `DATA/videos/beyond-the-gpu-maximizing-goodput-2026.json`
Original YouTube Video: https://www.youtube.com/live/CE3cAkqvDZA?si=-I21usS-cZlPbhDf
