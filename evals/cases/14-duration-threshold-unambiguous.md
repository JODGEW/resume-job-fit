# Experience-Duration Threshold Unambiguous

## Test Purpose

Verify that a year-only start date paired with `Present` does not create unresolved duration when the omitted start month cannot change whether the candidate satisfies the job description's experience-duration threshold.

## Evaluation Context

```text
Evaluation date: 2026-08-27
```

## Resume Input

```text
Morgan Chen

Software Engineer

Professional Experience
Software Engineer | 2022–Present

- Built and maintained backend services and APIs.
- Wrote automated tests and resolved production defects.

Skills
Python, REST APIs, PostgreSQL
```

## Job Description Input

```text
Software Engineer

Responsibilities

- Build and maintain production software services.
- Test, troubleshoot, and improve software systems.

Required Qualifications

- 3+ years of professional software engineering experience.
```

## Expected Behaviors

- The evaluator may anchor `Present` to the evaluation date of 2026-08-27.
- Missing month precision must not create unresolved duration because every possible start month in 2022 still satisfies the 3+ year threshold as of 2026-08-27.
- The 3+ year professional software engineering requirement should be classified as `Direct evidence`.
- The duration finding must not be downgraded to `Adjacent evidence` merely because the start month is absent.
- The missing start month must not be reported as Material Uncertainty when it cannot affect the threshold result.
- Duration must be attributed only to the professional `Software Engineer` role and must not be converted into years of Python, REST APIs, PostgreSQL, or any other specific technology.
- This case is intentionally different from a boundary case in which the missing month could change whether the duration threshold is met.
- The output must not produce `APPLY`/`HOLD`/`SKIP`.
