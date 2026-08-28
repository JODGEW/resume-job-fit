# Evidence Gap Is Not Material Uncertainty

## Test Purpose

Verify that a clearly stated job responsibility not demonstrated by the resume remains an evidence gap rather than being converted into Material Uncertainty.

## Resume Input

```text
Taylor Brooks

Backend Software Engineer

Professional Experience
Software Engineer | 2022–Present

- Built backend services and APIs.
- Deployed backend services to AWS.
- Containerized applications with Docker.

Skills
Backend development, AWS, Docker
```

## Job Description Input

```text
Backend Software Engineer

Responsibilities

- Deploy services to cloud infrastructure.
- Operate and monitor services in production.

Required Qualifications

- Experience developing and deploying backend services.
- Experience supporting reliable production services.
```

## Expected Behaviors

- The demonstrated deployment responsibility should be evaluated based on its actual backend-service and AWS deployment evidence.
- The separate "operate and monitor services in production" responsibility must not be treated as ambiguous merely because the resume is silent about it.
- Resume silence about operation and monitoring must remain `Missing evidence`, or `Adjacent evidence` only if the resume contains meaningfully related evidence.
- The Skill must not create a Material Uncertainty asking whether "operate" or "monitor" is really expected when the JD explicitly states those responsibilities.
- Material Uncertainty is reserved for genuine ambiguity in the supplied evidence or criterion, not for ordinary missing resume evidence.
- `Missing evidence` means only "not demonstrated by the supplied resume," not proof that the candidate lacks the experience.
- Responsibilities with different evidence strengths must remain separate.
- The output must not produce `APPLY`/`HOLD`/`SKIP`.
