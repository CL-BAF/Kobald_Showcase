<p align="center">
  <img src="assets/kobald-banner.svg" alt="Kobald, evidence focused AI and smart systems project" width="760" />
</p>

# Kobald

A student led project focused on transparent evidence, accountable decisions and controlled local AI development.

Kobald is an independently developed local AI and smart systems project based in Mount Gambier, South Australia. It is being developed by a 16 year old student developer and is focused on gathering and comparing evidence, identifying contradictions, preserving where information came from, communicating uncertainty, and keeping important decisions and external actions under human control.

**Governing principle: evidence before authority.**

Kobald is intended to assess claims using available evidence rather than social status, popularity or authority. It does not claim to be completely unbiased. Evidence, models, sensors, questions and human rules may all contain bias; Kobald is designed to make those limitations, contradictions and decisions more visible and auditable.

> **This repository is the public showcase, not the complete Kobald source repository.** The implementation, private automated test suite, internal developer documentation and infrastructure configuration are maintained separately. Appropriate technical reviewers can be given additional evidence privately where required.

## Technical overview

For reviewers who want more than the project summary:

- [Public architecture overview](docs/ARCHITECTURE.md)
- [Testing and verification](docs/TESTING.md)
- [NVIDIA DGX Spark development plan](docs/DGX-SPARK-PLAN.md)
- [Public project history](docs/PROJECT-HISTORY.md)

## The Problem

Most AI systems ask people to trust an answer. Kobald asks them to inspect the evidence behind it, see where information conflicts, and keep consequential decisions reviewable by a person.

## Current Project Stage

Kobald is an early working software foundation, not a finished product or deployed industry system. Its evidence workflow and human review controls are implemented and covered by an offline automated test suite.

| Item | Current public status |
|---|---|
| Tagged release baseline | v0.8.0 |
| v0.8.0 test status | 295 passing, 1 skipped |
| Latest documented development candidate | v0.9.0 release candidate at commit `84ad876` |
| Candidate test status | 604 passing, 1 skipped opt in live smoke test |
| Candidate release status | Private `main`, not tagged; no remote CI result claimed here |
| Runtime | Python standard library for the documented offline foundation |
| Public source status | Showcase only; full implementation remains private |

The test count is not presented as proof of production readiness. It is evidence that the development foundation is exercised systematically rather than being demonstrated only through hand picked examples.

## What Works Now

- Controlled ingestion from allowlisted local sources
- Evidence provenance and transparent quality signals
- Separate preservation of evidence for and against a conclusion
- Explicit contradictions, uncertainty and bounded confidence
- Human readable evidence briefs
- Persistent human review queue
- Approve, reject or request more evidence decisions
- Links between research sessions and confidence tracking
- Nine deterministic offline evaluation cases
- Complete deterministic offline demonstration using invented safe public data
- Structured audit records and secret redaction
- Early desktop Command Centre with conversation, model, settings and diagnostics views

## v0.9 Release Candidate Additions

The latest documented development candidate adds a bounded provider layer for deterministic mock responses, local Ollama and consent gated cloud models. These additions are covered by the offline test suite.

- Persistent cloud permission plus confirmation for each invocation
- Loopback only local provider URLs and trusted host cloud validation
- Redirect and environment proxy blocking for provider requests
- Strict source linked response validation that rejects fabricated references
- Metadata only live audit records without raw prompts or responses
- Read only AI connectivity checking that sends no evidence
- Invented evidence live demonstration that never approves its own result

The current public documentation does not claim a successful live Ollama request for this specific v0.9 release candidate unless that result is separately verified and published.

## Evidence Flow

```text
Question or material
    → controlled ingestion
    → evidence retrieval with provenance
    → evidence for and against kept separately
    → contradiction and uncertainty analysis
    → provisional conclusion
    → human review
    → approved knowledge or no action
```

A more complete system level view is available in the [architecture overview](docs/ARCHITECTURE.md).

## Desktop Interface

Kobald has an early desktop Command Centre under active development. The interface is intended to provide one place to view system state, interact with Kobald, select models, configure local audio devices and inspect diagnostics.

The screenshots below are development builds. They show the interface as it exists now rather than a finished product.

### Command Centre

<p align="center">
  <img src="assets/kobald-command-centre.webp" alt="Kobald Command Centre development interface" width="900" />
</p>

The current desktop interface exposes local system information, conversation controls, model selection areas, permissions and runtime status. The captured build shown here was disconnected from the Kobald server at the time of the screenshot.

### Settings

<p align="center">
  <img src="assets/kobald-settings.webp" alt="Kobald Command Centre settings window with server address redacted" width="475" />
</p>

The settings view provides server configuration, local speech output, microphone selection, audio output selection and background tray behaviour. The server address is redacted from the public screenshot.

### Diagnostics

<p align="center">
  <img src="assets/kobald-diagnostics.webp" alt="Kobald Desktop diagnostics development view" width="768" />
</p>

The diagnostics view is still under development and is intended to expose runtime and connection information in a dedicated view.

## Human Review and Safety

The documented foundation intentionally keeps a number of boundaries in place:

- No autonomous approval
- No unrestricted shell access in the documented release candidate
- No arbitrary file editing outside controlled Kobald records in the documented release candidate
- No live device control represented here as a finished capability
- No automatic messages, purchases, Git pushes or other external actions represented here as approved autonomous behaviour
- No model training or fine tuning claimed as a current capability
- New evidence begins unreviewed and is not automatically treated as truth
- Demonstrations use invented data where possible
- High impact decisions remain subject to human review
- Evidence is not sent to a cloud provider without the documented permission and confirmation controls
- Conclusions from live providers remain provisional until reviewed

These boundaries describe the documented public development state. Future controlled tool and computer interaction is a development direction, not something this showcase presents as already production ready.

## Current vs Future

| Implemented foundation | Potential future application or development |
|---|---|
| Evidence provenance and quality signals | Agriculture and environmental monitoring |
| Evidence briefs for human review | Education and research assistance |
| Confidence calibration without model training | Small business knowledge systems |
| Offline evaluation harness | Trades and maintenance documentation |
| Controlled local ingestion | Logistics and operational analysis |
| Cross session evidence linking | Cybersecurity evidence triage |
| Human review queue | Controlled sensor integration |
| Deterministic offline demonstration | Semantic similarity retrieval |
| Early desktop Command Centre | Broader local system and model orchestration |
| Bounded model provider layer | Larger local models and multimodal testing |

Future possibilities are not current deployments.

## Why More Compute Matters

The current Kobald foundation can be developed and tested on comparatively modest hardware, but the next stages of the project are intended to move more AI work onto local systems.

More capable local compute would make it practical to:

- run substantially larger models locally rather than depending as heavily on cloud services
- compare multiple models and configurations under the same controlled workflow
- experiment with model adaptation and fine tuning in later development stages
- support future multimodal work involving vision, audio and sensor data
- test longer running research and agent workflows locally
- preserve more sensitive development and project data on local infrastructure
- produce repeatable local benchmarks across models and Kobald versions
- explore distributed AI workloads as the project matures

These are development goals, not claims of functionality already implemented in Kobald.

### Why NVIDIA DGX Spark is relevant

NVIDIA DGX Spark is particularly relevant because its high memory local AI design provides a substantially larger development ceiling than the project's current hardware. It creates room for larger local models, demanding agent experiments, multimodal work and later model adaptation without requiring enterprise scale infrastructure.

The intended use is documented separately in the [DGX Spark development plan](docs/DGX-SPARK-PLAN.md), including proposed phases and public evidence that could be produced from the work.

## Demonstration and Verification

Kobald includes a repeatable offline demonstration covering controlled ingestion, duplicate and unsafe path rejection, evidence analysis, provisional confidence, human review, a second evidence session, links between research sessions, evaluation and preserved audit history.

The demonstration uses invented solar panel material, mock AI responses and no live hardware or network access. It demonstrates workflow and safety boundaries; it does not prove that every conclusion is true or that Kobald is ready for production.

The testing approach and limits of the public claims are described in [Testing and Verification](docs/TESTING.md).

## Potential Local Applications

These are possible future directions, not claims of present deployment:

- **Agriculture:** comparing sensor readings, weather and historical observations before suggesting the next inspection
- **Education:** helping students examine supporting and opposing evidence
- **Small business:** preserving procedures, decisions and project handovers
- **Trades and maintenance:** recording service evidence, outcomes and lessons
- **Logistics:** comparing operational records and identifying contradictions
- **Cybersecurity:** organising evidence from multiple alerts while leaving action with a person

## Project Direction

The next stage is a controlled local prototype using suitable computing hardware, reliable storage, power protection, an isolated sensor network and a small number of read only environmental sensors. Real world capability will be introduced gradually, tested separately and kept behind explicit human approval.

Kobald's development direction also includes broader local model orchestration, multimodal work, controlled tool use and computer interaction. These areas will only be represented as current capability when they have actually been implemented and verified.

## Private Technical Review

The complete Kobald source code, automated test suite and internal developer documentation are maintained separately from this showcase.

For a legitimate technical or sponsorship review, additional evidence can be made available selectively, such as:

- current test run output
- selected test categories and verification notes
- architecture and security explanations
- selected implementation excerpts relevant to a review question
- live or recorded demonstrations

This allows technical claims to be reviewed without publishing the entire private codebase.

## Support and Sponsorship

Kobald is developed independently by Cameron Lonnie in Mount Gambier, South Australia.

Hardware support, technical mentorship and project review can directly help expand local AI development, testing and future smart systems work. Any donated or sponsored hardware would be used as development infrastructure for Kobald rather than represented as evidence that unfinished capabilities already exist.

For project enquiries or technical review, contact can be made through the GitHub profile associated with this repository.