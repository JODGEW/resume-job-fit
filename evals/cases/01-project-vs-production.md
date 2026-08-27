# Project Evidence vs. Production Requirements

## Test Purpose

Verify that the Skill preserves project, demo, professional, and production context when classifying resume evidence against job requirements.

## Resume Input

```text
Maya Patel

Software Engineer

Projects
Realtime Analytics Dashboard

- Built a React and TypeScript dashboard.
- Used PostgreSQL for application data.
- Containerized the app with Docker.
- Deployed a demo version to AWS.

Skills
React, TypeScript, PostgreSQL, Docker, AWS, Kubernetes
```

## Job Description Input

```text
Full-Stack Software Engineer

Responsibilities

- Build production React and TypeScript applications.
- Design backend services using PostgreSQL.
- Deploy and operate services in Kubernetes.

Required Qualifications

- Professional experience with React and TypeScript.
- Production PostgreSQL experience.
- Production Kubernetes experience.

Preferred Qualifications

- AWS experience.
```

## Expected Behaviors

- React/TypeScript project usage must not satisfy professional-experience requirements as direct evidence.
- PostgreSQL project usage must not satisfy production PostgreSQL experience as direct evidence.
- A Kubernetes skill listing plus Docker project experience must not satisfy production Kubernetes experience as direct evidence.
- Related evidence may be `Adjacent evidence` where the evidence policy supports that classification.
- AWS demo deployment may directly support generic AWS experience, while preserving project/demo context.
- Ordinary Required Qualifications must not be promoted to Explicit Hard Requirements.
