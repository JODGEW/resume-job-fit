# Specialization Mismatch Despite Tooling Overlap

## Test Purpose

Verify that the Skill distinguishes supporting technology overlap from alignment with a role whose core specialization is embedded and low-level systems engineering.

## Resume Input

```text
Morgan Chen

Software Engineer

Professional Experience
Software Engineer | 2021–Present

- Built Python backend services and REST APIs.
- Containerized backend applications with Docker.
- Deployed and operated services on AWS.
- Designed database integrations and asynchronous processing workflows.

Skills
Python, REST APIs, Docker, AWS, PostgreSQL
```

## Job Description Input

```text
Embedded Systems Software Engineer

Responsibilities

- Develop embedded systems software in C and C++.
- Design and maintain device drivers.
- Integrate software with sensors and peripherals through low-level hardware interfaces.
- Build Python tools and REST APIs that support device testing and diagnostics.

Required Qualifications

- Professional embedded-systems development experience.
- Strong C and C++ programming experience.
- Experience developing device drivers and interacting with hardware at a low level.

Preferred Qualifications

- Docker and AWS experience.
```

## Expected Behaviors

- Generic tooling overlap must not be treated as direct evidence of the target specialization.
- The Skill should identify the specialization mismatch as material because the JD centers on embedded/low-level systems.
- Python, Docker, REST, or AWS evidence may still be recognized where relevant.
- Supporting technology matches must not erase missing embedded-systems, device-driver, low-level hardware, or C/C++ evidence.
- Job-title similarity or generic "software engineer" experience must not establish specialization alignment.
- The output must not produce `APPLY`/`HOLD`/`SKIP`.
