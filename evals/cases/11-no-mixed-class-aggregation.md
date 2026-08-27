# No Mixed-Class Aggregation Across Responsibilities

## Test Purpose

Verify that the Skill evaluates material responsibilities separately when their evidence strengths differ, rather than aggregating Direct and Adjacent findings into one Alignment Analysis row with a synthetic or mixed evidence class.

## Resume Input

```text
Morgan Chen

Backend Software Engineer

Professional Experience
Backend Software Engineer | 2021–Present

- Built and maintained Python backend services and REST APIs for customer-facing applications.
- Deployed backend services to AWS and supported their operation in AWS environments.
- Containerized services with Docker and deployed the containers through Amazon ECS.

Skills
Python, REST APIs, AWS, Docker, Amazon ECS
```

## Job Description Input

```text
Backend Platform Engineer

Responsibilities

- Build Python backend services and APIs.
- Work with AWS infrastructure.
- Deploy and operate services in Kubernetes.

Required Qualifications

- Professional Python backend development experience.
- Must have production Kubernetes experience.
```

## Expected Behaviors

- Each material responsibility with a different evidence strength must be evaluated separately.
- The Python backend responsibility may be classified as `Direct evidence` based on the demonstrated professional Python backend and API work.
- The AWS responsibility should receive its own evidence classification based on the wording of the responsibility and the resume's direct AWS deployment and operations evidence.
- The Kubernetes responsibility must remain separate and may be classified as `Adjacent evidence` because Docker and Amazon ECS container deployment are related but non-equivalent to Kubernetes.
- The explicit statement "Must have production Kubernetes experience" must be classified as an Explicit Hard Requirement.
- Docker, Amazon ECS, and AWS deployment evidence must not satisfy production Kubernetes experience as `Direct evidence`.
- The Skill must not emit `Mixed`, `Partial`, or any other evidence class outside `Direct`, `Adjacent`, and `Missing`.
- A single aggregated Alignment Analysis row must not combine Direct and Adjacent findings under one evidence class.
- Cross-references may be used to avoid duplicating evidence across responsibility and qualification findings.
- The output must not produce `APPLY`/`HOLD`/`SKIP`.
