# Explicit Hard Requirement Classification

## Test Purpose

Verify that the Skill distinguishes ordinary required qualifications from a requirement explicitly marked as non-negotiable, while preserving the difference between Docker and production Kubernetes experience.

## Resume Input

```text
Jordan Lee

Software Engineer

Experience
Software Engineer | 2021–2024

- Built backend APIs in Python.
- Containerized services with Docker.
- Deployed services to AWS.

Skills
Python, Docker, AWS
```

## Job Description Input

```text
Backend Software Engineer

Responsibilities

- Build and maintain backend services in Python.
- Deploy and operate production services in Kubernetes.

Required Qualifications

- 2+ years of software engineering experience.
- Strong Python experience.
- Must have production Kubernetes experience.

Preferred Qualifications

- AWS experience.
```

## Expected Behaviors

- "2+ years of software engineering experience" remains a Required Qualification.
- "Strong Python experience" remains a Required Qualification.
- "Must have production Kubernetes experience" is classified as an Explicit Hard Requirement.
- Docker experience is related but non-equivalent to Kubernetes and must not satisfy production Kubernetes experience as `Direct evidence`.
- Docker may provide `Adjacent evidence` for the Kubernetes criterion.
- AWS experience remains Preferred.
- The output must not produce `APPLY`/`HOLD`/`SKIP`.
