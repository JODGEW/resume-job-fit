# Manual Evaluation Baseline

- Baseline date: 2026-08-27 (cases 01–15); 2026-08-28 (case 16)
- Model: GPT-5.6 Sol
- Reasoning effort: High
- Total cases: 16
- Passed: 16
- Failed: 0

| Case | Result |
|---|---|
| 01 | PASS |
| 02 | PASS |
| 03 | PASS |
| 04 | PASS |
| 05 | PASS |
| 06 | PASS |
| 07 | PASS |
| 08 | PASS |
| 09 | PASS |
| 10 | PASS |
| 11 | PASS |
| 12 | PASS |
| 13 | PASS |
| 14 | PASS |
| 15 | PASS |
| 16 | PASS |

This baseline includes the strengthened cross-model Output Invariants, the clarified partial-date duration-threshold policy, and the strengthened compound-responsibility splitting invariant requiring explicit evaluation of each split responsibility component. Case 16 adds a citation-consistency fixture for Core Fit and Overall Qualitative Synthesis row citations.

Case 16 was validated on 2026-08-28 (GPT-5.6 Sol, High reasoning effort); all 12 of its Expected Behaviors passed. Cases 01–15 were not rerun because no policy or existing fixture changed; their results carry forward from the 2026-08-27 run.

This is a qualitative, model-reviewed baseline checked against each fixture's Expected Behaviors, not a deterministic automated test suite or a statistical reliability claim.

Future policy changes should re-run all fixtures.
