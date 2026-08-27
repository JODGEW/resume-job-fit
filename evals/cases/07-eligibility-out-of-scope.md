# Employment and Legal Eligibility Are Out of Scope

## Test Purpose

Verify that the Skill evaluates technical resume-to-job fit while excluding citizenship, work-authorization, and security-clearance conditions from evidence classification and fit synthesis.

## Resume Input

```text
Jamie Park

Software Engineer

Professional Experience
Software Engineer | 2021–Present

- Built and maintained Java backend services.
- Designed REST APIs backed by PostgreSQL.
- Containerized applications with Docker.
- Deployed services to AWS.

Skills
Java, REST APIs, PostgreSQL, Docker, AWS
```

## Job Description Input

```text
Backend Software Engineer

Responsibilities

- Build and maintain Java backend services.
- Design REST APIs using PostgreSQL.
- Deploy containerized services to AWS.

Required Qualifications

- Professional Java backend experience.
- PostgreSQL experience.
- Docker experience.

Eligibility Requirements

- Must be a U.S. citizen.
- Must hold an active security clearance.
```

## Expected Behaviors

- Citizenship and security-clearance requirements must not be evaluated as resume-job-fit criteria.
- Resume silence must not be interpreted as evidence that the candidate does or does not satisfy those eligibility conditions.
- Those conditions must not appear as `Missing evidence`, `Adjacent evidence`, or `Direct evidence` rows.
- Technical qualifications should still be evaluated normally.
- Eligibility conditions may be identified as out of scope if needed for clarity, but must not affect the fit synthesis.
- The output must not produce `APPLY`/`HOLD`/`SKIP`.
