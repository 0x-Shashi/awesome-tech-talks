# Keras Turns 10: A decade of deep learning

**Speaker(s):** Yufeng Guo, François Chollet, Matt Watson - **Channel:** Google for Developers - **Date:** 2026-01-16
**Watch:** https://youtu.be/oekqrCFN7MM?si=QjlOx7afHeY9hiTk - **Format:** Fireside Chat - **Level:** Intermediate
**Topics:** LLM Fundamentals - Research/Papers - AI Coding Tools

## TL;DR

Keras creator François Chollet and Google engineer Matt Watson join Yufeng Guo to celebrate the 10th anniversary of Keras. They trace its journey from 2015 Theano scripts to the modern Keras 3 multi-backend engine (supporting JAX, PyTorch, and TensorFlow), discuss the progressive disclosure of complexity design ethos, explain KerasHub and Kaggle Models integration, and explore the next decade of neuro-symbolic program synthesis.

## Contents

- [The origin of Keras: from Theano chatbot tooling to open-source library](#the-origin-of-keras-from-theano-chatbot-tooling-to-open-source-library)
- [Etymology: the Gate of Horn from Homer's Odyssey](#etymology-the-gate-of-horn-from-homers-odyssey)
- [Evolution of Keras versions: 0.x to 3.0](#evolution-of-keras-versions-0x-to-30)
- [Design philosophy: progressive disclosure of complexity](#design-philosophy-progressive-disclosure-of-complexity)
- [Pre-trained models, KerasHub, and Kaggle integration](#pre-trained-models-kerashub-and-kaggle-integration)
- [Kaggle's role in ML best practices](#kaggles-role-in-ml-best-practices)
- [Advice for ML practitioners: first principles over hype cycles](#advice-for-ml-practitioners-first-principles-over-hype-cycles)
- [The next 10 years: program synthesis and neuro-symbolic AI](#the-next-10-years-program-synthesis-and-neuro-symbolic-ai)

## The origin of Keras: from Theano chatbot tooling to open-source library

François Chollet started developing neural networks in 2013:
- **Early QA research**: In early 2014, while building a question-answering chatbot system using **Theano** (an early precursor to modern RAG), Chollet developed reusable modules for recurrent neural networks and LSTMs.
- **Solving developer friction**: Existing deep learning frameworks in 2014-2015 (such as Caffe) required configuring neural network graphs in rigid YAML files. Chollet designed Keras to enable Pythonic, code-driven model declaration with ergonomics inspired by scikit-learn.
- **Open-source release**: Packaged and published in March 2015 on GitHub, rapidly expanding into a standard machine learning framework.

## Etymology: the Gate of Horn from Homer's Odyssey

The name **Keras** (Greek for *horn*) originates from a classical literary metaphor in Homer's *Odyssey*:
- **Gate of Ivory**: False, deceptive dreams enter the human realm through a gate of polished ivory (*elephas*, wordplay on *elephairo*, to deceive).
- **Gate of Horn**: True, prophetic visions pass through the Gate of Horn (*keras*, wordplay on *kraino*, to fulfill).
- **Metaphor**: Keras was conceived as the architectural gateway to make true visions of artificial intelligence actionable and realizable in software.

## Evolution of Keras versions: 0.x to 3.0

`mermaid
flowchart LR
  K0[Keras 0.x / 1.0
2015-2016
Theano + TensorFlow
Sequential & Functional API] --> K2[Keras 2.0 / tf.keras
2017-2022
Embedded in TensorFlow]
  K2 --> K3[Keras 3.0
2023-Present
Multi-Backend Standalone
JAX + PyTorch + TF + NumPy]
`

- **Keras 0.x (2015)**: Sequential model architecture on Theano, adding TensorFlow support within days of TensorFlow's open-source release.
- **Keras 1.0 (2016)**: Introduced the Functional API, custom callbacks, custom loss functions, and layer abstractions.
- **Keras 2.0 (2017-2018)**: Merged directly into TensorFlow as 	f.keras, dropping multi-backend flexibility due to internal organizational focus.
- **Keras 3.0 (2023+)**: Completely re-architected in two months into a lightweight, standalone engine running natively across **JAX**, **PyTorch**, **TensorFlow**, **NumPy**, **OpenVINO**, and **MLX** without requiring TensorFlow as a dependency.

## Design philosophy: progressive disclosure of complexity

The core design principle guiding Keras is **progressive disclosure of complexity**:
- **Zero-cliff learning curve**: Standard, high-frequency tasks (training a baseline classifier or loading an LLM) require minimal lines of code.
- **Graceful descent into customization**: Advanced requirements (custom loss functions, custom training steps, or bespoke GPU kernels) do not force developers to discard high-level abstractions. Users can drop from Keras high-level APIs directly into native JAX transformations or PyTorch autograd routines.

## Pre-trained models, KerasHub, and Kaggle integration

Matt Watson describes the industry shift toward foundation model fine-tuning:
- **KerasHub**: Unifies prior domain packages (KerasCV, KerasNLP) into a single library supporting vision, language, and multimodal architectures (such as Stable Diffusion and Gemini-class models).
- **Kaggle Models**: Serves as the primary distribution hub for KerasHub pre-trained weights, enabling single-line instantiation across Colab, Kaggle Notebooks, and local infrastructure.

## Kaggle's role in ML best practices

- **Empirical validation**: Kaggle provides a grounded environment where architectures prove their efficacy under competitive constraints rather than social media hype.
- **Historical impact**: Competitions like the 2014 Higgs Boson challenge established gradient-boosted decision trees (**XGBoost**) as the gold standard for tabular data; Keras became the dominant deep learning tool on Kaggle starting in 2016.

## Advice for ML practitioners: first principles over hype cycles

Chollet and Watson encourage developers to distinguish short-term hype from fundamental shifts:
- **Foundational stability**: Core deep learning theory, backpropagation, and transformer architectures have evolved deliberately over multiple years despite weekly social media cycles.
- **First-principles analysis**: Evaluate new models and papers based on verifiable empirical utility and mathematical grounding rather than trending discussions.

## The next 10 years: program synthesis and neuro-symbolic AI

Looking toward 2035, Chollet identifies the fusion of deep learning with symbolic AI as the next frontier:
- **Program synthesis**: Combining differentiable neural networks with discrete program search to autonomously synthesize verifiable algorithms and domain-specific languages.
- **Enduring relevance**: Differentiable optimization and foundational neural abstractions will remain central to software engineering across the coming decades.

## Source

Full cleaned transcript: DATA/videos/keras-10-years-deep-learning-2026.json
Raw transcript: RAW/videos/keras-10-years-deep-learning-2026.md
