# Orchestrating ML/AI Workloads with TPUs on GKE

**Speaker(s):** Yufeng Guo, Kavitha Gowda · **Channel:** Google Cloud Tech · **Date:** 2026-04-10
**Watch:** https://youtu.be/coP5_SmE4AI?si=o79IroUrSluCePZI · **Format:** Talk / Technical Deep Dive · **Level:** Advanced
**Topics:** Backend/Infra, Machine Learning

## TL;DR

A technical masterclass on orchestrating Google Cloud Tensor Processing Units (TPUs) using Google Kubernetes Engine (GKE). Kavitha Gowda (GKE TPU Product Manager) and Yufeng Guo explore TPU ASIC architectures, Matrix Multiplying Units (MXUs), 3D Torus optical interconnects, multi-slice pod scheduling with open-source **Kueue**, and enterprise best practices from leading AI model builders like Anthropic and Moloco.

## Contents

- [TPU hardware architecture: Matrix Multiplying Units (MXUs) and ASICs](#tpu-hardware-architecture-matrix-multiplying-units-mxus-and-asics)
- [Topology and multi-slice architecture: 3D Torus interconnects](#topology-and-multi-slice-architecture-3d-torus-interconnects)
- [Orchestrating TPUs with GKE: Kueue and automated node provisioning](#orchestrating-tpus-with-gke-kueue-and-automated-node-provisioning)
- [Best practices for AI model builders: Anthropic, Moloco, and Lightricks](#best-practices-for-ai-model-builders-anthropic-moloco-and-lightricks)

---

## TPU hardware architecture: Matrix Multiplying Units (MXUs) and ASICs

Google Cloud TPUs are custom **Application-Specific Integrated Circuits (ASICs)** engineered from the ground up for deep learning linear algebra:
- **Matrix Multiplying Units (MXUs)**: Dedicated hardware arrays that compute massive matrix multiplications in a single step rather than serial instruction passes.
- **High Memory Bandwidth**: Tightly coupled High-Bandwidth Memory (HBM) feeds billions of model parameters to compute cores without data starvation.
- **Workload Efficiency**: Delivers superior price-performance and power efficiency for transformer model pre-training, fine-tuning, and high-throughput LLM serving.

---

## Topology and multi-slice architecture: 3D Torus interconnects

Scaling foundation models beyond a single machine requires low-latency inter-chip communication:

```mermaid
flowchart TD
    subgraph TPU Pod Topology
        Slice1[TPU Slice 1\n 3D Torus Interconnect] <--> OCS[Optical Circuit Switches\n Inter-Pod Bandwidth]
        Slice2[TPU Slice 2\n 3D Torus Interconnect] <--> OCS
        Slice3[TPU Slice 3\n 3D Torus Interconnect] <--> OCS
    end
    K8s[GKE Multi-Slice Orchestrator\n Kueue Co-Scheduling] --> TPU Pod Topology
```

- **3D Torus Optical Mesh**: Connects chips in a wrapped three-dimensional grid, eliminating top-of-rack Ethernet bottlenecks.
- **Multi-Slice Pods**: GKE co-schedules multiple TPU slices as a single unified compute fabric to run distributed data, pipeline, and tensor parallelism.

---

## Orchestrating TPUs with GKE: Kueue and automated node provisioning

GKE simplifies large-scale accelerator operations:
- **GKE Node Auto-Provisioning**: Dynamically provisions the exact TPU chip generations (v5p, v6e) and slice shapes requested by Kubernetes workload specs.
- **Kueue Scheduling**: An open-source Kubernetes-native job manager that enforces fair sharing, prioritizes interactive serving over batch jobs, and handles automated job preemption across multi-tenant teams.

---

## Best practices for AI model builders: Anthropic, Moloco, and Lightricks

- **Containerized ML Frameworks**: Run standardized JAX, PyTorch/XLA, and MaxText training containers on GKE.
- **Hardware-Aware Scheduling**: Pin latency-critical inference tasks to dedicated TPU slices with automated health-checking and subsecond failover.

**Related:** [Engineering the future of Kubernetes for AI at scale](./kubernetes-for-ai-at-scale-2026.md)

---

## Source

Full cleaned transcript: `DATA/videos/tpus-on-gke-ml-workloads-2026.json`
Raw transcript: `RAW/videos/tpus-on-gke-ml-workloads-2026.md`
