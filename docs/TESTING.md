# Testing and Verification

> **Scope note (October 2026):** Existing test reports describe the earlier **general evidence-first Kobald prototype**, not the proposed scientific harness. No reported test count should be interpreted as proof that scientific simulation, chemical analysis, instrument integration or automated laboratory work exists or is scientifically valid.


Kobald's complete automated test suite is maintained with the private development codebase rather than in this public showcase repository.

This page explains what the published test status means, what areas are covered and what evidence can be provided for technical review without exposing the full implementation.

## Current published status

For the historically documented v0.9.0 release candidate, the private automated suite reported:

- **604 tests passing**
- **1 skipped opt in live smoke test**
- deterministic offline coverage for the core evidence and review workflow

This is a historical milestone, not a fresh verification of the canonical KobaldAi repository. The public showcase does not claim that this test count proves production readiness. It is evidence that the current development foundation is being exercised systematically and that major project behaviour is not being assessed only through manual demonstrations.

## Areas covered by automated testing

The private suite covers behaviour including:

- controlled ingestion and rejection of unsafe or invalid inputs
- evidence provenance and source tracking
- preservation of supporting and opposing evidence
- contradiction and uncertainty handling
- confidence and research session behaviour
- persistent human review state
- approve, reject and request more evidence decisions
- deterministic offline evaluation cases
- audit record behaviour and secret redaction
- provider validation and bounded model access
- cloud consent and confirmation behaviour
- local and mock provider handling
- source linked response validation
- desktop/server integration behaviour where appropriate

Exact internal test names, fixtures and source code are intentionally not mirrored into this public repository.

## Public evaluation examples

To make the documented behaviour easier to inspect without exposing the private test suite, the showcase now includes public representative material:

- [Public offline evaluation cases](../examples/offline_eval_cases.json)
- [Public demonstration transcript](../examples/demo_transcript.md)

These are sanitised examples built around the behaviours described in this repository. They are **not** a verbatim export of the private automated test fixtures and should not be treated as independent proof that every expected behaviour is production ready.

The evaluation cases show the expected handling of situations such as conflicting evidence, insufficient evidence, source provenance, fabricated source references, duplicate material, invalid local paths, cloud consent, human review boundaries and later evidence changing an earlier conclusion.

The demonstration transcript uses entirely invented solar-installation material to show the evidence and review workflow in a form that can be read without running the private codebase.

## Verification approach

Kobald uses several different forms of verification rather than relying on one number.

### Deterministic offline tests

Core workflows are designed to be exercised without depending on a live cloud service. This makes regressions easier to reproduce and prevents ordinary test runs from silently sending project data to an external provider.

### Invented demonstration data

Public demonstrations use invented material where possible. This allows the project to demonstrate ingestion, evidence handling, review state and audit behaviour without presenting a staged demonstration as proof that a real world claim is true.

### Negative path testing

The project tests not only successful workflows but also rejection paths such as unsafe inputs, fabricated source references, missing consent and invalid provider configuration.

### Human review checks

A model response is not considered equivalent to an approved decision. The review queue and approval boundaries are tested as part of the workflow rather than being treated as a documentation only promise.

## Evidence available for private technical review

Where appropriate, a legitimate reviewer can be provided with additional material such as:

- current test run output
- selected test names and categories
- release candidate verification notes
- selected source excerpts relevant to a specific review question
- architecture and security explanations
- live or recorded demonstrations

This would be provided selectively. The goal is to make technical claims reviewable without publishing the entire private codebase.

## What this showcase does and does not prove

The public repository is intended to show project direction, current capability, interface development and verification practices.

It does **not** claim that:

- every planned feature already exists
- every test represents an independent capability
- the project is production ready
- the private source has been independently audited
- a large automated test count replaces real world validation

Kobald's public documentation deliberately separates implemented capability, tested development work and future goals.