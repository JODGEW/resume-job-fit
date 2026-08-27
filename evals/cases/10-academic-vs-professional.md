# Academic Evidence vs. Professional Requirements

## Test Purpose

Verify that the Skill preserves academic source context when evaluating academic machine-learning work against separate professional machine-learning and generic PyTorch experience requirements.

## Resume Input

```text
Priya Shah

Education
M.S. in Computer Science

Capstone Project
Image Classification System

- Built and trained image-classification models using PyTorch.
- Evaluated model performance on an academic dataset.

Academic Research
Graduate Researcher

- Conducted machine-learning research on feature selection and model evaluation.
- Implemented experiments in Python and documented research findings.

Skills
Python, PyTorch, machine learning
```

## Job Description Input

```text
Machine Learning Engineer

Responsibilities

- Develop and evaluate machine-learning models.
- Implement model-training workflows with PyTorch.

Required Qualifications

- Professional machine-learning experience.
- PyTorch experience.
```

## Expected Behaviors

- Academic machine-learning work must not satisfy a professional-experience requirement as `Direct evidence`.
- Academic ML work may provide `Adjacent evidence` for professional ML experience when it is meaningfully related.
- Explicit PyTorch usage in an academic project may be `Direct evidence` for a generic PyTorch experience requirement if the JD does not require professional or production PyTorch use.
- The Skill must preserve the academic source context.
- Education must not be converted into professional experience unless the JD explicitly allows that equivalence.
- The output must not produce `APPLY`/`HOLD`/`SKIP`.
