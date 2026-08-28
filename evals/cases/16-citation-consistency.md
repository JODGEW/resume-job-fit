# Citation Consistency Across Summary Sections

## Test Purpose

Verify that row IDs cited in Core Fit and Overall Qualitative Synthesis agree with the evidence classes recorded in the evaluation tables. This fixture protects against two observed failures: an ID range that sweeps a `Missing evidence` row into a list of demonstrated strengths, and stale or mismatched IDs that point at the wrong row after renumbering. The evidence is deliberately unambiguous so that the case tests citation consistency rather than classification judgment.

## Resume Input

```text
Jordan Patel

Backend Software Engineer

Professional Experience
Backend Software Engineer | 2022–Present

- Built Python backend services and REST APIs for a customer-facing web application.
- Wrote automated unit and integration tests for backend services with pytest.
- Designed and maintained PostgreSQL database schemas for application data.

Skills
Python, REST APIs, pytest, PostgreSQL
```

## Job Description Input

```text
Backend Software Engineer

Responsibilities

- Build Python backend services and REST APIs.
- Write automated tests for backend services.
- Develop React frontend features for the customer web application.
- Design and maintain PostgreSQL database schemas.

Required Qualifications

- Professional Python backend development experience.
```

## Expected Behaviors

- The required professional Python backend development qualification should be classified as `Direct evidence` based on the demonstrated professional Python backend service and API work.
- The four responsibility rows are identified below by JD order and criterion name. The evaluator may assign any valid identifier scheme, such as `A1`–`A4` or `A2a`–`A2d`; the behaviors below apply to whatever IDs the output actually assigns.
- The first responsibility row, Python backend services and REST APIs, should be classified as `Direct evidence`.
- The second responsibility row, automated tests for backend services, should be classified as `Direct evidence`.
- The third responsibility row, the React frontend responsibility row, must be classified as `Missing evidence`; the supplied resume contains no frontend, React, or JavaScript evidence, and backend API work must not be treated as adjacent frontend evidence.
- The fourth responsibility row, PostgreSQL database schemas, should be classified as `Direct evidence`.
- Every row ID cited in Core Fit or Overall Qualitative Synthesis as directly supported or demonstrated must resolve to a `Direct evidence` row.
- When an ID range is cited to support a claim that criteria are directly supported or demonstrated, every row inside that range must be `Direct evidence`. A range used for that purpose must not sweep in an `Adjacent evidence` or `Missing evidence` row. For example, if the output assigns the responsibility rows `A1`–`A4`, then `A1–A4` must not be cited in support of a demonstrated-strength claim because the React frontend responsibility row is `Missing evidence`.
- The React frontend responsibility row must be cited, using the ID the output actually assigned to it, as not demonstrated in both Core Fit and Overall Qualitative Synthesis.
- Core Fit and Overall Qualitative Synthesis must use the correct current row IDs for the same findings and must not contain stale or mismatched IDs; a citation for one finding must not point at a row that records a different finding.
- `Missing evidence` for the frontend responsibility means only "not demonstrated by the supplied resume," not proof that the candidate lacks the skill.
- The output must not produce `APPLY`/`HOLD`/`SKIP`.
