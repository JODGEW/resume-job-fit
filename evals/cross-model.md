# Cross-Model Smoke Test

## Purpose

Verify that the same resume-job-fit policy produces materially consistent evidence classifications across different model families.

## Test Protocol

Each model received the same Sam Kim resume and Platform Software Engineer JD in a clean-room session. Each model was instructed to:

- read `SKILL.md` and `references/`
- not read `evals/`, `examples/`, `README.md`, or baseline files
- not modify files
- use the Skill's normal output format

## Results

| Model           | Reasoning effort | Result |
| --------------- | ---------------- | ------ |
| GPT-5.6 Sol     | High             | PASS   |
| Claude Opus 5   | xhigh            | PASS   |
| Claude Sonnet 5 | High             | PASS   |

## Behaviors Verified

All final runs correctly:

- classified professional Python backend experience as Direct evidence
- classified the 3+ years threshold as Direct for `2022–Present` because every plausible start month satisfies the threshold as of 2026-08-27
- classified Docker/ECS as Adjacent rather than equivalent to production Kubernetes
- preserved the production Kubernetes hard requirement as unmet by the supplied resume
- did not use Mixed or Partial as evidence classes
- did not convert ordinary evidence gaps into Material Uncertainty
- assigned no evidence class when the JD supplied no material role-level criterion
- excluded work-authorization eligibility from fit evidence
- produced no APPLY/HOLD/SKIP recommendation

## Issues Found During Testing

Earlier Claude runs exposed two policy-robustness issues, but these are not current results:

1. Inconsistent handling of output invariants, including mixed evidence-class aggregation and role-level/uncertainty handling.
2. Overly conservative handling of year-only `2022–Present` duration thresholds.

These were addressed by strengthening Output Invariants in `SKILL.md` and clarifying partial-date duration-threshold reasoning in `references/evaluation-rubric.md`.

## Limitations

- This is a qualitative smoke test, not a statistical benchmark.
- Three model configurations are not evidence of universal cross-model consistency.
- The Claude Code runs followed the repository instructions by reading `SKILL.md` and `references/`; this test does not establish native Skill auto-registration or installation compatibility in Claude Code.
