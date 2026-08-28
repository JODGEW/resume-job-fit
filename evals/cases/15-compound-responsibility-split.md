# Compound Responsibility Split Across Evidence Classes

## Test Purpose

Verify that the Skill splits a compound responsibility when its components have different evidence classes. This fixture protects against silently collapsing the entire responsibility into the strongest evidence class available for only one component.

## Resume Input

```text
Alex Rivera

Backend Software Engineer

Professional Experience
Backend Software Engineer | 2022–Present

- Developed Python backend services and REST APIs for business applications.
- Containerized backend services with Docker.
- Deployed containerized services to Amazon ECS.

Skills
Python, REST APIs, Docker, Amazon ECS
```

## Job Description Input

```text
Backend Software Engineer

Responsibilities

- Develop backend services and APIs.
- Deploy and operate services in Kubernetes.

Required Qualifications

- Professional backend development experience.
```

## Expected Behaviors

- The compound responsibility "Deploy and operate services in Kubernetes" must not be classified as one aggregate evidence row because its deployment and operation components have different evidence classes.
- The deployment component must be evaluated separately from the ongoing service-operation component.
- Docker containerization and Amazon ECS deployment must be classified as `Adjacent evidence` for deployment to Kubernetes because they are related but non-equivalent technologies and deployment contexts.
- Ongoing operation of deployed services must be classified as `Missing evidence` because the supplied resume does not demonstrate monitoring, incident response, reliability, scaling, or other ongoing service-operation work.
- The Missing operation evidence must not be upgraded to `Adjacent evidence` merely because deployment evidence exists.
- The professional backend development requirement should be classified as `Direct evidence` based on the demonstrated professional backend service and API work.
- The Skill must not emit `Mixed`, `Partial`, or any other invented evidence class; only `Direct evidence`, `Adjacent evidence`, and `Missing evidence` are valid evidence classes.
- Ordinary resume silence about service operation is an evidence gap, not Material Uncertainty.
- Because the JD supplies no material role-level criterion, the Role Level Alignment row should state that no material criterion was identified and must not assign an evidence class.
- The output must not produce a numeric fit score.
- The output must not produce `APPLY`/`HOLD`/`SKIP`.
