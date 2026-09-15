# Kobald Public Demonstration Transcript

This is an **invented, offline demonstration scenario** for the public Kobald showcase. It is designed to show the intended evidence, contradiction, uncertainty and human-review workflow without relying on a real organisation, real incident or live cloud model.

The exact wording below is a public example, not a verbatim export of a private production conversation or private test fixture.

## Scenario

A fictional community facility is preparing to approve a new solar installation. Several documents appear to disagree about whether commissioning is actually complete.

The user asks Kobald to review the available evidence before a decision is made.

---

## Evidence provided

### SRC-A — Commissioning Summary

> All required commissioning tests for the South Ridge solar installation were completed successfully on 4 August. The system is ready for final approval.

### SRC-B — Electrical Review Note

> Two inverter shutdown tests remain outstanding. Final sign-off should not occur until these tests have been completed and recorded.

### SRC-C — Site Monitoring Note

> During the afternoon inspection the battery enclosure reached 43 C. No shutdown or alarm was recorded during the observation period.

### SRC-D — Battery Manufacturer Sheet

> Recommended battery operating temperature is 0 C to 45 C.

---

## User

Is the South Ridge solar installation ready for final approval?

## Kobald

The available evidence does **not** support a confident conclusion that the installation is ready for final approval yet.

### Evidence supporting approval

- **SRC-A — Commissioning Summary** states that all required commissioning tests were completed successfully and describes the system as ready for final approval.
- **SRC-C — Site Monitoring Note** reports that the battery enclosure reached 43 C without a shutdown or alarm during the observation period.
- **SRC-D — Battery Manufacturer Sheet** gives a recommended operating range of 0 C to 45 C, so the recorded 43 C observation is within the stated range.

### Evidence against approval

- **SRC-B — Electrical Review Note** states that two inverter shutdown tests remain outstanding and says final sign-off should not occur until they are completed.

### Contradiction

SRC-A says all required commissioning tests are complete, while SRC-B says two required shutdown tests remain outstanding. These statements cannot both be accepted as complete descriptions of the current testing status without further evidence.

### Provisional conclusion

**Not ready for final approval based on the current evidence.**

This does not mean the installation has failed. It means the evidence about commissioning status is unresolved. The safest next step is to confirm whether the two shutdown tests identified in SRC-B were completed after that note was written and obtain the resulting test records.

### Confidence

**Moderate.**

The reason confidence is not high is that the central disagreement concerns whether required testing is complete, and the supplied evidence does not establish which document reflects the latest verified state.

### Recommended next evidence

1. Results of the two inverter shutdown tests identified in SRC-B.
2. A dated final commissioning record showing whether those tests were completed.
3. Confirmation of whether SRC-A or SRC-B is the later document if document timestamps are available.

### Review state

**Provisional — human review required.**

No approval action should be taken automatically from this conclusion.

---

## Human reviewer

**Decision:** Request more evidence

**Reason:** The commissioning documents conflict. Obtain the two shutdown test results and confirm the latest commissioning state before approval.

---

## Additional evidence received

### SRC-E — Shutdown Test Record

> Inverter shutdown tests 1 and 2 were completed successfully on 6 August. No unresolved shutdown-test items remain.

### SRC-F — Final Commissioning Record

> Final commissioning review completed on 7 August. All required commissioning tests, including inverter shutdown testing, are complete.

---

## User

Does the new evidence change the conclusion?

## Kobald

Yes. The new evidence materially changes the earlier assessment.

### New evidence

- **SRC-E — Shutdown Test Record** directly addresses the two outstanding tests described in SRC-B and states that both were completed successfully on 6 August.
- **SRC-F — Final Commissioning Record** states that the final commissioning review was completed on 7 August and that all required testing is complete.

### Relationship to the earlier contradiction

The earlier conclusion was cautious because SRC-A and SRC-B disagreed about whether commissioning was complete.

SRC-E and SRC-F provide later evidence that directly resolves the outstanding issue identified in SRC-B. The earlier research state should remain preserved, but the current assessment can now be updated using the newer evidence.

### Revised provisional conclusion

**The available evidence now supports the installation being ready for final approval, subject to human review.**

### Confidence

**High, within the limits of the supplied documents.**

### Review state

**Provisional — human approval still required.**

Kobald should not convert this conclusion into an approved decision automatically.

---

## Human reviewer

**Decision:** Approve

**Reason:** The later shutdown-test record and final commissioning record resolve the previously identified contradiction.

---

## What this demonstration is intended to show

This example demonstrates the public project goals of:

- keeping source provenance visible
- preserving evidence for and against a conclusion separately
- identifying contradictory information rather than hiding it
- communicating uncertainty
- asking for missing evidence instead of inventing an answer
- allowing later evidence to revise a conclusion without erasing earlier research history
- keeping the final approval decision with a person

It does **not** demonstrate a real solar engineering assessment and must not be used as one. All project names, documents, measurements and events in this transcript are invented.
