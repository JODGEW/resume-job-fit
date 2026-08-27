# Evaluation Procedure

The eval fixtures are under `evals/cases/`. Each fixture contains **Resume Input**, **Job Description Input**, and **Expected Behaviors**.

1. Read `SKILL.md` and all files under `references/` before evaluating.
2. Run each fixture independently.
3. Compare the model output against every Expected Behavior.
4. Mark a case **PASS** only if every expected behavior is satisfied. Otherwise, mark it **FAIL** and record the exact violated behavior.
5. Do not modify the Skill while running the baseline.

`evals/baseline.md` records the latest committed qualitative baseline. This is currently a model-reviewed qualitative evaluation, not a deterministic automated test suite. After any policy or rubric change, rerun all cases and update `baseline.md` only after reviewing the results.

## Reusable Evaluator Prompt

```text
Read SKILL.md and every file under references/. Evaluate each fixture in evals/cases/ independently. For each fixture, run the Skill using its Resume Input and Job Description Input, then compare the output against every Expected Behavior. Mark the case PASS only if every behavior is satisfied; otherwise mark it FAIL and list each exact violated behavior. Do not modify the Skill during this baseline run. Report the result and concise evidence for each case. After reviewing all results, update evals/baseline.md only if requested.
```
