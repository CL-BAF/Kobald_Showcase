# NVIDIA DGX Spark Development Plan

This document explains why hardware in the NVIDIA DGX Spark class is relevant to Kobald and how it would be used if hardware support became available.

Kobald does not require DGX Spark to exist. The current software foundation can be developed on more modest hardware. The value of DGX Spark is that it would raise the ceiling for local AI experimentation and reduce the need to move development workloads into cloud systems.

## Why DGX Spark fits the project

NVIDIA describes DGX Spark as a Grace Blackwell desktop AI system with **128 GB of coherent unified memory**, up to **1 PFLOP of FP4 AI performance**, and support for local AI development with models up to **200 billion parameters**.

Official product information:

- https://www.nvidia.com/en-au/products/workstations/dgx-spark/
- https://docs.nvidia.com/dgx/dgx-spark/hardware.html

Those characteristics are relevant to Kobald because the project's next stages increasingly depend on local model capacity rather than only conventional application compute.

## Intended use

### 1. Larger local model evaluation

Kobald would be used to compare larger local models under the same evidence, review and audit workflow.

The aim would not simply be to run the largest model possible. The project would compare useful qualities such as:

- source following
- contradiction handling
- uncertainty communication
- structured output reliability
- tool use behaviour
- latency and memory requirements
- failure behaviour under constrained prompts

### 2. Local agent workloads

Kobald is moving toward longer running agent and research workflows. Higher local AI capacity would make it practical to test these workflows without making cloud access the default requirement.

This is particularly relevant where prompts, project material or future sensor information should remain local.

### 3. Multimodal development

Future Kobald work is intended to include controlled use of vision, audio and sensor data.

DGX Spark would provide a platform for testing multimodal models locally while keeping the same human review and audit principles used elsewhere in the project.

### 4. Model adaptation and fine tuning experiments

Later development may include small scale fine tuning or model adaptation experiments where they are useful and technically appropriate.

This is a future research direction, not a claim that Kobald currently trains its own foundation models.

### 5. Repeatable benchmarking

A dedicated AI development system would make it easier to produce repeatable local benchmark results across model versions and Kobald releases.

Results could include:

- model loading and memory behaviour
- response latency
- structured output success rates
- evidence citation success rates
- contradiction detection performance on controlled evaluation cases
- local versus cloud workflow comparisons

### 6. Privacy preserving development

One of Kobald's design goals is to keep more work local when possible.

More capable local compute would allow a larger share of development, evaluation and future smart systems processing to remain on hardware under the developer's control instead of being sent to an external model provider.

## Proposed development phases

| Phase | Intended work | Public evidence that can be produced |
|---|---|---|
| Initial setup | Validate Kobald and model tooling on DGX OS | Setup notes and compatibility findings |
| Local inference | Evaluate larger local models | Model comparison notes and benchmark tables |
| Agent testing | Run longer research and tool workflows | Demonstration recordings and evaluation summaries |
| Multimodal work | Add controlled vision/audio experiments | Sanitised demos and architecture updates |
| Adaptation experiments | Explore appropriate fine tuning or model adaptation | Method notes and non-sensitive results |
| Ongoing evaluation | Compare Kobald releases and model configurations | Updated testing and benchmark documentation |

## Why not simply use cloud compute

Cloud AI remains useful and Kobald already has a design for consent gated cloud providers. It is not treated as inherently bad.

However, local hardware provides several advantages for this project:

- sensitive development material can remain local
- repeated testing does not depend on per request cloud availability or cost
- model and runtime behaviour can be evaluated in a stable environment
- long running experiments are easier to reproduce
- local model research aligns directly with Kobald's project direction

The intended approach is not "local at all costs". It is to make local operation practical enough that cloud access is a choice rather than a requirement.

## If hardware support is provided

Any donated or sponsored DGX Spark would be used as development infrastructure for Kobald.

Public project material would continue to distinguish clearly between:

- implemented features
- tested development work
- experimental work
- future plans

Hardware support would not be represented as NVIDIA certification, endorsement or validation of unfinished Kobald capabilities unless NVIDIA explicitly stated otherwise.

## Technical review

The complete Kobald source code, private automated test suite and internal developer documentation are maintained separately from this showcase repository.

Appropriate NVIDIA technical reviewers can be given additional evidence privately where required, without publishing the entire implementation.