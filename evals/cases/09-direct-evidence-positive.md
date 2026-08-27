# Direct Evidence for Clearly Matching Experience

## Test Purpose

Verify that the Skill classifies clearly demonstrated professional experience as direct evidence when it matches the JD criterion without relying on unstated context or equivalence.

## Resume Input

```text
Avery Johnson

Software Engineer

Professional Experience
Software Engineer | 2021–Present

- Developed web applications using React and TypeScript.
- Designed REST APIs for backend services.
- Used PostgreSQL to store and query application data.
- Deployed applications to AWS.

Skills
React, TypeScript, REST APIs, PostgreSQL, AWS
```

## Job Description Input

```text
Full-Stack Software Engineer

Responsibilities

- Develop applications using React and TypeScript.
- Design REST APIs.
- Work with PostgreSQL.
- Deploy applications to AWS.

Required Qualifications

- Professional React and TypeScript application-development experience.
- REST API design experience.
- PostgreSQL experience.
- AWS deployment experience.
```

## Expected Behaviors

- Clearly matching professional React and TypeScript experience should be `Direct evidence`.
- Explicit REST API design experience should be `Direct evidence` for a REST API design requirement.
- Explicit PostgreSQL professional usage should be `Direct evidence` for a generic PostgreSQL experience requirement.
- Explicit AWS deployment experience should be `Direct evidence` for a generic AWS deployment requirement.
- The Skill must not invent extra gaps when the JD does not require additional proficiency, scale, duration, ownership, or production context.
- Direct evidence remains limited to the scope actually demonstrated by the resume.
- The output must not produce `APPLY`/`HOLD`/`SKIP`.
