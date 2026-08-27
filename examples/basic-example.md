# Basic Backend/Platform Example

This synthetic example shows an end-to-end, evidence-based evaluation of a software engineer resume against a backend/platform job description.

## Resume Input

**Maya Chen — Software Engineer**

**Summary:** Software engineer with 6 years of professional backend development experience.

**Harbor Metrics — Software Engineer (January 2022–Present)**

- Built and operated Go REST services backed by PostgreSQL on AWS ECS for a multi-tenant analytics product.
- Designed Kafka consumers for billing events and participated in the backend on-call rotation, including incident reviews and service monitoring.
- Led a database-schema migration with the payments and analytics teams and presented the rollout plan in engineering design reviews.
- Packaged services with Docker and maintained GitHub Actions deployment workflows.

**Vector Library — Backend Developer (July 2020–December 2021)**

- Developed Python APIs and PostgreSQL data jobs for an internal inventory application.

**Skills:** Go, Python, PostgreSQL, Kafka, Docker, AWS ECS, GitHub Actions.

## Job Description Input

**Senior Backend Platform Engineer — Northstar Cloud**

**Core responsibilities**

- Design and operate reliable Go services and APIs for an internal developer platform.
- Improve observability, deployment safety, and incident response for platform services.
- Lead technical projects across application and infrastructure teams.

**Required qualifications**

- 4+ years of professional backend software engineering experience.
- Demonstrated production experience with Go and PostgreSQL.
- Experience building event-driven systems with Kafka or an equivalent message broker.
- **Must have at least 2 years of hands-on experience operating Kubernetes clusters in production.**

**Preferred qualification**

- Experience managing infrastructure with Terraform.

**Employment condition**

- Must be legally authorized to work in the United States without current or future employer sponsorship.

The employment condition is intentionally excluded from evidence evaluation because work authorization is a legal/employment eligibility matter outside the Skill's scope.

## Representative Evaluation Output

# Resume–Job Fit Evaluation

## Context

- Target role: Senior Backend Platform Engineer at Northstar Cloud
- Source limitations: No material source limitation was identified; both synthetic inputs are complete for this example.

## Core Fit

The resume directly demonstrates the role's central backend experience, production Go/PostgreSQL work, event-driven systems, service operation, and incident response (R1–R3, A2a). Its service monitoring and deployment-workflow experience is relevant, but does not explicitly demonstrate improving observability or deployment safety (A2b). Backend SaaS work is transferable to an internal developer platform, but that specialization and the expected senior platform scope are only adjacent (A1, A5). Docker and AWS ECS are relevant container experience, but they do not establish the non-negotiable Kubernetes requirement or its duration (H1).

## Required Qualifications

| ID | JD requirement and evidence | Evidence class | Resume evidence | Evaluation |
|---|---|---|---|---|
| R1 | 4+ years of professional backend software engineering experience (Required qualifications) | Direct evidence | Summary states 6 years of professional backend development; backend roles run from July 2020 to Present. | The stated experience directly supports the duration and professional-backend context required. |
| R2 | Demonstrated production experience with Go and PostgreSQL (Required qualifications) | Direct evidence | Harbor Metrics role: built and operated Go REST services backed by PostgreSQL for a multi-tenant analytics product. | The described professional operation of the services directly supports production use of both technologies. |
| R3 | Event-driven systems using Kafka or an equivalent broker (Required qualifications) | Direct evidence | Harbor Metrics role: designed Kafka consumers for billing events. | The resume directly demonstrates Kafka-based event processing in professional experience. |

## Explicit Hard Requirements

| ID | JD hard requirement and evidence | Evidence class | Resume evidence | Evaluation |
|---|---|---|---|---|
| H1 | “Must have at least 2 years” operating Kubernetes clusters in production (Required qualifications) | Adjacent evidence | Harbor Metrics role: packaged services with Docker and operated Go services on AWS ECS. | Docker and ECS show related container and service-operation experience, but they are not Kubernetes and do not establish two years operating production Kubernetes clusters. |

## Important Preferred Qualifications

| ID | JD preference and evidence | Evidence class | Resume evidence | Evaluation |
|---|---|---|---|---|
| P1 | Experience managing infrastructure with Terraform (Preferred qualification) | Missing evidence | No relevant evidence identified in the supplied resume. | Terraform-based infrastructure management is not demonstrated by the supplied resume. This does not prove that the candidate lacks the skill, and it remains a preferred—not required—qualification. |

## Alignment Analysis

| ID | Dimension | JD evidence | Evidence class | Resume evidence | Evaluation |
|---|---|---|---|---|---|
| A1 | Specialization | Internal developer platform services (Core responsibilities) | Adjacent evidence | Harbor Metrics role: backend services for a multi-tenant analytics product. | The backend service work is transferable, but internal developer-platform specialization is not demonstrated. |
| A2a | Responsibilities | Operate reliable services and support incident response (Core responsibilities) | Direct evidence | Harbor Metrics role: operated Go services and participated in the backend on-call rotation, including incident reviews. | The resume directly demonstrates service operation and incident-response responsibilities. |
| A2b | Responsibilities | Improve observability and deployment safety (Core responsibilities) | Adjacent evidence | Harbor Metrics role: performed service monitoring and maintained GitHub Actions deployment workflows. | Monitoring and deployment-workflow maintenance are relevant, but the resume does not explicitly demonstrate improving observability or deployment safety. |
| A3 | Experience duration | 4+ years of professional backend engineering (Required qualifications) | Direct evidence | See R1. | The documented duration supports the requirement. |
| A4a | Primary technology or language | Go and PostgreSQL in production (Required qualifications) | Direct evidence | See R2. | The primary language and database requirement is directly supported. |
| A4b | Primary technology or language | Production Kubernetes operations for at least 2 years (Explicit hard requirement) | Adjacent evidence | See H1. | Related container experience does not establish Kubernetes or the required duration. |
| A5 | Role level | Lead technical projects across application and infrastructure teams (Core responsibilities) | Adjacent evidence | Harbor Metrics role: led a schema migration with payments and analytics teams and presented its rollout in design reviews. | This supports cross-team technical leadership on one project, but ongoing senior platform ownership across application and infrastructure teams is not demonstrated. |

## Material Uncertainties

No material uncertainty was identified from the supplied inputs. The Kubernetes and Terraform findings are evidence gaps or adjacent evidence, not ambiguities.

## Overall Qualitative Synthesis

Direct evidence supports the core backend duration, production Go/PostgreSQL work, Kafka experience, service operation, and incident response (R1–R3, A2a, A3–A4a). Adjacent evidence includes monitoring and deployment-workflow maintenance, which do not explicitly demonstrate improving observability or deployment safety; SaaS backend work and one cross-team migration also leave developer-platform and senior-scope differences (A1, A2b, A5). Most materially, Docker/ECS experience does not establish the explicit production Kubernetes requirement or its two-year duration (H1, A4b). Terraform is not demonstrated by the supplied resume, which means only that the provided document supplies no evidence for that preference—not that the candidate necessarily lacks the skill (P1).
