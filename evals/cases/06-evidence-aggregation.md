# Evidence Aggregation for One Criterion

## Test Purpose

Verify that the Skill considers all evidence relevant to a single criterion, preserves the strongest demonstrated context, and does not combine weaker evidence into an unsupported production claim.

## Resume Input

```text
Riley Singh

Software Engineer

Professional Experience
Software Engineer | 2022–Present

- Built backend services in Python.
- Deployed services to Kubernetes in a staging environment.

Projects
Containerized Task Queue

- Built a task-processing application.
- Containerized the application with Docker.

Skills
Python, Kubernetes, Docker, PostgreSQL
```

## Job Description Input

```text
Platform Software Engineer

Responsibilities

- Deploy and operate production services in Kubernetes.

Required Qualifications

- Production Kubernetes experience.
```

## Expected Behaviors

- The Skill should consider all relevant evidence for the same criterion rather than evaluating each item in isolation.
- The professional staging Kubernetes usage is stronger and more specific evidence than a skill listing or Docker project evidence.
- None of the evidence establishes production Kubernetes usage.
- Multiple weaker pieces of evidence must not be combined to manufacture production context that is never stated.
- The criterion should remain non-direct for the production requirement while preserving the strongest demonstrated Kubernetes context.
- Evidence should not be double-counted merely because the same underlying experience appears in multiple resume sections.
- The output must not produce `APPLY`/`HOLD`/`SKIP`.
