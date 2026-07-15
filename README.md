<p align="center">
  <img src="assets/kobald-banner.svg" alt="Kobald - evidence-focused AI and smart-systems project" width="760" />
</p>

---

# Kobald

Kobald is a student-led, locally operated AI and smart-systems project based in Mount Gambier, South Australia. It gathers and compares evidence, identifies contradictions, preserves where information came from, communicates uncertainty, and keeps important decisions and external actions under human control.

**Governing principle: evidence before authority.**

Kobald is intended to assess claims using available evidence rather than social status, popularity or authority. It does not claim to be completely unbiased. Evidence, models, sensors, questions and human rules may all contain bias; Kobald is designed to make those limitations, contradictions and decisions more visible and auditable.

## The Problem

Most AI systems ask people to trust an answer. Kobald asks them to inspect the evidence and reasoning behind it.

## Current Project Stage

Kobald is an early working software foundation, not a finished product or deployed industry system. Its evidence workflow and human-review controls are implemented and covered by an offline automated test suite.

**Current documented build:** v0.8.1  
**Test status:** 295 passing, 1 skipped opt-in live smoke test  
**Runtime:** Python standard library; offline demonstrations require no cloud service

## What Works Now

- Controlled ingestion from allowlisted local sources
- Evidence provenance and transparent quality signals
- Separate preservation of evidence for and against a conclusion
- Explicit contradictions, uncertainty and bounded confidence
- Human-readable evidence briefs
- Persistent human review queue
- Approve, reject or request-more-evidence decisions
- Cross-session evidence linking and confidence tracking
- Nine deterministic offline evaluation cases
- Complete deterministic offline demonstration using invented public-safe data
- Structured audit records and secret redaction

## Evidence Flow

```text
Question or material
    -> controlled ingestion
    -> evidence retrieval with provenance
    -> evidence for and against kept separately
    -> contradiction and uncertainty analysis
    -> provisional conclusion
    -> human review
    -> approved knowledge or no action
```

## Human Review and Safety

- No autonomous approval
- No unrestricted shell access
- No arbitrary file editing outside controlled Kobald records
- No live device control
- No automatic messages, purchases, Git pushes or other external actions
- No model training or fine-tuning
- New evidence begins unreviewed and is not automatically treated as truth
- Demonstrations use invented data and run offline
- High-impact decisions remain subject to human review

## Current vs Future

| Implemented foundation | Potential future application |
|---|---|
| Evidence provenance and quality signals | Agriculture and environmental monitoring |
| Evidence briefs for human review | Education and research assistance |
| Confidence calibration without model training | Small-business knowledge systems |
| Offline evaluation harness | Trades and maintenance documentation |
| Controlled local ingestion | Logistics and operational analysis |
| Cross-session evidence linking | Cybersecurity evidence triage |
| Human review queue | Controlled sensor integration |
| Deterministic offline demonstration | Semantic similarity retrieval |

Future possibilities are not current deployments.

## Demonstration

Kobald includes a repeatable offline demonstration covering controlled ingestion, duplicate and unsafe-path rejection, evidence analysis, provisional confidence, human review, a second evidence session, cross-session comparison, evaluation and preserved audit history.

The demonstration uses invented solar-panel material, mock AI responses and no live hardware or network access. It demonstrates the workflow and safety boundaries; it does not prove that every conclusion is true or that Kobald is production-ready.

## Potential Local Applications

These are possible future directions, not claims of present deployment:

- **Agriculture:** comparing sensor readings, weather and historical observations before suggesting the next inspection
- **Education:** helping students examine supporting and opposing evidence
- **Small business:** preserving procedures, decisions and project handovers
- **Trades and maintenance:** recording service evidence, outcomes and lessons
- **Logistics:** comparing operational records and identifying contradictions
- **Cybersecurity:** organising evidence from multiple alerts while leaving action with a person

## Project Direction

The next stage is a controlled local prototype using suitable computing hardware, reliable storage, power protection, an isolated sensor network and a small number of read-only environmental sensors. Real-world capability will be introduced gradually, tested separately and kept behind explicit human approval.

The complete technical source, test suite and developer documentation are maintained separately and can be made available to appropriate reviewers on request.
