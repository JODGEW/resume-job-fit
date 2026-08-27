# Experience-Duration Ambiguity

## Test Purpose

Verify that the Skill preserves uncertainty when a year-only employment date range does not establish whether a candidate meets a precise experience-duration requirement.

## Resume Input

```text
Alex Rivera

Software Engineer

Professional Experience
Software Engineer | 2024–Present

- Built and maintained Python backend APIs.
- Implemented backend integrations and automated tests.

Skills
Python, REST APIs, PostgreSQL
```

## Job Description Input

```text
Backend Software Engineer

Responsibilities

- Build and maintain Python backend services.

Required Qualifications

- 2+ years of professional software engineering experience.
- Python backend experience.
```

## Expected Behaviors

- The Skill must not assume that "2024–Present" satisfies 2+ years when the start month is absent.
- Relevant professional experience should still be recognized.
- The duration requirement should remain unresolved or otherwise clearly unconfirmed from the supplied resume.
- Total employment tenure must not be converted into years with Python unless the resume explicitly supports that duration.
- Resume silence must not be interpreted as proof that the candidate lacks the required duration.
- The output must not produce `APPLY`/`HOLD`/`SKIP`.
