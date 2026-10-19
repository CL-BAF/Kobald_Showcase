# Kobald — Public Scientific Architecture

This is a high-level, **proposed** architecture for Kobald's direction as an AI harness for scientific computing and research. It is not a diagram of an already integrated science platform. The public showcase omits private implementation and infrastructure details.

## Target system view

~~~text
Researcher / scientific operator
          |
          v
Experiment workspace / research control plane
          |
          v
AI planning and tool-selection layer
          |
          v
Scientific job manifest (inputs, units, assumptions, versions)
          |
          v
Policy and authorisation / human review
          |
          +----------------------+---------------------+
          |                      |                     |
          v                      v                     v
Simulation adapters      Analysis / dataset tools   Read-only instrument adapter
          |                      |                 (future, supervised)
          +----------------------+---------------------+
                                 |
                                 v
                  Recorded results and execution trace
                                 |
                                 v
                 Provenance / uncertainty / verification
                                 |
                                 v
                   Researcher review and next action
~~~

The model does not replace the physics engine, numerical solver, laboratory instrument or scientific verification process. It coordinates tools and suggests interpretations, subject to permissions and review.

## Scope and maturity

| Component | Status | Notes |
|---|---|---|
| Evidence/provenance and review | Implemented in legacy prototype foundations | Migration/revalidation into canonical KobaldAi pending |
| Local/cloud provider integration | Prototype foundation | Not science-specific |
| Desktop Command Centre | Early development interface | Original conversation-oriented UI may change |
| Scientific job manifest and runner | Planned | Must capture data, parameters, units, tool versions, seeds and outputs |
| Physics-engine or numerical solver integration | Planned | Start with deterministic, independently checked examples |
| Chemical analysis connector | Planned | Begin with offline datasets, not live equipment |
| Instrumentation and sensors | Planned | Synthetic and read-only first; requires device-specific safety review |
| Autonomous physical experiments | Not implemented / not baseline scope | Any future consideration requires qualified oversight, approvals and safety controls |

## Authority and boundaries

AI-generated text, plans, retrieved sources, dataset contents and tool results are untrusted inputs. Each proposed tool action must be validated against typed interfaces and explicit capability grants.

Scientific results must retain their original source, measurement or simulation context. Models may make provisional interpretations but cannot silently rewrite instrument outputs or promote them into independently validated findings.

Physical-device operation requires safeguards outside the model. No general-purpose model instruction grants authority to change hardware state, run hazardous procedures or bypass interlocks.

## Relationship to Domovoi

Kobald's scientific harness is independent of the Domovoi efficiency research initiative. Future Domovoi models may be evaluated on reproducible scientific tasks in Kobald, but no Domovoi model is currently demonstrated or validated.

For technical development status, refer to the [canonical KobaldAi repository](https://github.com/CL-BAF/KobaldAi).