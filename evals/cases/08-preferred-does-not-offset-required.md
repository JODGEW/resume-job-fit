# Preferred Strengths Do Not Offset a Required Gap

## Test Purpose

Verify that the Skill keeps required and preferred qualifications separate when a resume strongly supports several preferences but provides no meaningful evidence for a central required qualification.

## Resume Input

```text
Casey Nguyen

Backend Software Engineer

Professional Experience
Backend Software Engineer | 2020–Present

- Designed and operated backend services using PostgreSQL.
- Containerized production applications with Docker.
- Deployed and monitored services on AWS.
- Improved database reliability and automated cloud deployments.

Skills
Python, PostgreSQL, Docker, AWS
```

## Job Description Input

```text
Full-Stack Software Engineer

Responsibilities

- Build and maintain production user interfaces with React.
- Collaborate with backend engineers to deliver full-stack features.

Required Qualifications

- Professional React experience.

Preferred Qualifications

- AWS experience.
- Docker experience.
- PostgreSQL experience.
```

## Expected Behaviors

- Required and preferred qualifications must remain separate.
- Strong preferred-qualification evidence must be recognized.
- Preferred strengths must not erase, compensate for, or convert the missing required React evidence into alignment.
- The React requirement should remain `Missing evidence` if no meaningful direct or adjacent React evidence exists.
- The overall synthesis should preserve both the preferred strengths and the material required-qualification gap.
- The output must not produce `APPLY`/`HOLD`/`SKIP`.
