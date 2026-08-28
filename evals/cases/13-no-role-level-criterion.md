# No Material Role-Level Criterion

## Test Purpose

Verify that the Skill does not assign an evidence classification for Role Level when the job description contains no material criterion concerning seniority, leadership, scope, autonomy, ownership, or decision-making.

## Resume Input

```text
Jordan Lee

Software Engineer

Professional Experience
Software Engineer | 2019–Present

- Implemented Python backend services and REST APIs.
- Built database queries and background processing jobs.
- Wrote automated tests and fixed application defects.
- Deployed backend service updates using Docker and AWS.

Skills
Python, REST APIs, PostgreSQL, Docker, AWS
```

## Job Description Input

```text
Backend Software Engineer

Responsibilities

- Implement and maintain backend services and REST APIs.
- Develop database integrations and background processing jobs.
- Write automated tests and troubleshoot application defects.
- Deploy backend service updates using Docker and AWS.

Required Qualifications

- 3+ years of professional software engineering experience.
- Hands-on experience developing backend services and REST APIs.
- Experience with relational databases, automated testing, and cloud deployment.
```

## Expected Behaviors

- The Skill must not infer a material role-level criterion from the job title alone.
- The Skill must not infer a material role-level criterion from the experience-duration requirement alone.
- The `Role Level Alignment` row should state that no material role-level criterion was identified.
- No `Direct evidence`, `Adjacent evidence`, or `Missing evidence` classification should be assigned to the `Role Level Alignment` row.
- Hands-on backend responsibilities should still be evaluated normally elsewhere in the analysis.
- The resume's `Software Engineer` title and employment duration must not be used to manufacture a role-level match.
- The normal experience-duration requirement may be evaluated on its own terms, without converting it into a seniority or role-level criterion.
- The output must not produce `APPLY`/`HOLD`/`SKIP`.
