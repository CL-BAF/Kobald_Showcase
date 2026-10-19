<p align="center">
  <img src="assets/kobald-banner.svg" alt="Kobald scientific AI harness — research and evidence-led development" width="760" />
</p>

# Kobald — Scientific AI Harness

**Kobald is an early-stage AI harness being developed for scientific investigation: connecting interchangeable AI models with simulations, scientific software, structured data and, eventually, properly authorised research instruments.**

The goal is **not** to build another everyday personal assistant. The goal is to create a system through which researchers can specify a question, select tools, run traceable analyses, inspect the results, challenge the evidence and decide what experiment to perform next.

Physics engines, computational chemistry and instrument-connected analysis are examples of the *intended direction*, not features being advertised as complete today.

> **Principle: evidence before authority.** A model's confident answer is not a measurement, a simulation result is not automatically ground truth, and no AI-generated action grants itself permission to operate laboratory equipment.

> **This is the public showcase**, not the complete implementation. The [current source repository](https://github.com/CL-BAF/KobaldAi) is undergoing a deliberate rebuild and migration from an earlier prototype.

## At a glance

| | |
|---|---|
| **Research focus** | Scientific computing, reproducible experiments, data and evidence provenance, AI-assisted analysis |
| **Long-term vision** | A modular AI orchestration harness for scientific software, simulators and controlled equipment interfaces |
| **Present state** | Early prototype foundations and a new canonical codebase; scientific engines and instrument integrations remain planned |
| **Model strategy** | Interchangeable local and optional cloud models rather than dependency on a single AI provider |
| **Separate research effort** | [Domovoi](https://github.com/CL-BAF/Domovoi-Kobald_showcase), a proposed long-term AI-efficiency research initiative |

## Why build this?

AI can help propose hypotheses, write analysis code or interpret research papers. But actual scientific work depends on more than generating convincing text.

A research-grade workflow needs to know:

- Which dataset, observation, instrument or simulation produced a result?
- Which tool version, parameters, initial conditions and units were used?
- Can another person rerun the calculation or reproduce the experiment?
- What uncertainty, limitations, errors or contradictory evidence remain?
- Which actions were approved by a qualified human and which were merely proposed?

Kobald is being designed around those questions. Its central goal is a **verifiable process around AI** rather than expecting researchers to trust model output on its own.

## Intended scientific applications

These are **proposed integrations**, not currently working capabilities.

| Domain | Example workflow | Intended interface |
|---|---|---|
| **Physics and engineering** | Set up a numerical or physics-engine simulation, record assumptions, run it and inspect outputs | Simulation/solver adapters with repeatable run manifests |
| **Chemistry** | Analyse chemical datasets, compare computed properties, process instrument-exported measurements | Computational chemistry and analysis connectors |
| **Biology and environmental science** | Analyse time-series, microscopy or environmental datasets with explicit provenance | Data and analysis pipelines |
| **Mathematics and statistics** | Execute numerical methods, inspect error bounds and compare models | Typed computational tools |
| **Laboratory measurements** | Import readings from compatible instruments under institutional supervision | Initially synthetic and read-only connectors |
| **Cross-disciplinary research** | Coordinate independent tools, compare outputs and assemble an evidence record | Research job orchestration and human review |

The aim is not to have an AI invent scientific truth. It is to give researchers a controlled way to use real computational tools and observable data while retaining independent verification.

## How a future Kobald research session could work

~~~text
Researcher defines a question or hypothesis
        |
        v
Choose datasets, simulation tools and analysis methods
        |
        v
Check permissions, tool capabilities and safety constraints
        |
        v
Execute an isolated simulation or read-only analysis
        |
        v
Capture parameters, units, versions, observations and errors
        |
        v
Compare with evidence, references and alternative results
        |
        v
Present traceable findings, uncertainties and discrepancies
        |
        v
Researcher reviews and determines the next step
~~~

This is an **architectural target**, not a completed end-to-end workflow.

A result should be traceable to its inputs and methods. Re-running a seeded simulation may establish computational reproducibility; it does not by itself establish empirical validity.

## What has been built so far?

Earlier Kobald development produced an experimental, evidence-focused AI platform. Demonstrated and documented development foundations include:

- a developing local Knowledge Vault and source/evidence handling;
- provenance, contradiction comparison and provisional conclusions in legacy workflows;
- human review and policy/audit foundations;
- bounded model-provider access and deterministic offline test scaffolding;
- an early Command Centre desktop interface;
- experimental, constrained cybersecurity tooling in the older prototype.

These foundations may be reused, redesigned or retired as the [canonical KobaldAi codebase](https://github.com/CL-BAF/KobaldAi) is built out. That newer repository currently contains **foundation scaffolding**, not the full migrated legacy runtime.

**Not yet demonstrated:** integrated physics engines, production scientific solvers, chemical instrument analysis connectors, real lab control, autonomous experiment execution or independently validated scientific outcomes.

The long-term scientific direction is substantially more difficult than a general chat assistant, and the project makes no fixed delivery or research-success guarantee.

## Engineering principles

**Reproducibility.** Every execution should record tool and environment versions, input identity, assumptions, numerical units, parameters and output artifacts.

**Evidence and uncertainty.** Models may suggest interpretations, but evidence, measurements, tool results and counterexamples must remain inspectable and distinguishable.

**Modularity.** Models and scientific tools should be interchangeable; the harness should not depend on Domovoi succeeding.

**Researcher control.** An AI model must not authorise its own actions. External changes, especially on physical equipment, require explicit permitted scope and suitable independent safety controls.

**Local-first where practical.** Research data should be kept under the operator's control; optional cloud use must be explicit and appropriate for the data.

## Scientific hardware and laboratory integration

Instrument support is a **future research and engineering objective**, not a claim that Kobald can currently operate laboratory devices.

Development should begin with offline datasets, simulated instruments, software-only tools and read-only measurements. Any later physical actuation needs device-specific interlocks, approval from appropriate operators and institutional safety review. AI instructions are not a substitute for laboratory protocols.

## Where Domovoi fits

Kobald and Domovoi solve different problems.

| Project | Scientific question |
|---|---|
| **Kobald** | How can AI models reliably interact with scientific tools, data and research workflows? |
| **Domovoi** | Can AI architectures deliver substantially more useful capability per byte, operation and watt? |

Domovoi is **conceptual/pre-experimental**; there is no validated new Domovoi model or breakthrough to report. Should future models become available, Kobald could provide scientific workflows for practical evaluation. Kobald will also work toward supporting existing models.

[Read the combined Kobald and Domovoi overview](https://github.com/CL-BAF/Domovoi-Kobald_showcase).

## Development interface

These images show **early development builds** of the previous general AI interface, not a finished scientific research interface.

### Command Centre

<p align="center">
  <img src="assets/kobald-command-centre.webp" alt="Earlier Kobald Command Centre development interface" width="900" />
</p>

### Settings

<p align="center">
  <img src="assets/kobald-settings.webp" alt="Earlier Kobald Command Centre settings window" width="475" />
</p>

### Diagnostics

<p align="center">
  <img src="assets/kobald-diagnostics.webp" alt="Earlier Kobald diagnostics development view" width="768" />
</p>

The interface may be redesigned to prioritise experiments, datasets, instrumentation, analysis runs and evidence trails rather than everyday conversation.

## Technical information and project history

- [Public architecture overview](docs/ARCHITECTURE.md)
- [Testing and verification](docs/TESTING.md)
- [NVIDIA DGX Spark development plan](docs/DGX-SPARK-PLAN.md) — an earlier hardware exploration, not a current requirement
- [Public project history](docs/PROJECT-HISTORY.md)
- [Public offline evaluation examples](examples/README.md)
- [Current source repository](https://github.com/CL-BAF/KobaldAi)
- [Combined Kobald + Domovoi research overview](https://github.com/CL-BAF/Domovoi-Kobald_showcase)

## Research support and collaboration

The project is seeking meaningful **research collaboration, specialist technical review, access to scientific tools and computing resources, and possible long-term funding pathways**. Of particular interest are researchers or organisations experienced in numerical simulation, scientific software, computational chemistry, reproducibility, analytical instrumentation and safe system integration.

This is an independent, early-stage project based in Mount Gambier, South Australia, led by Cameron Lonnie while completing secondary school.

Support and collaboration would help investigate technical feasibility; it should not be interpreted as third-party verification, institutional endorsement or a promise of commercial success.

> **Build it. Measure it. Challenge it. Improve it.**