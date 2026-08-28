# resume-job-fit

`resume-job-fit` is a Skill for evidence-grounded analysis of how a resume fits a job description. It uses only the supplied resume and job description (JD).

## Scope

The Skill identifies relevant qualifications, gaps, and role-level alignment. It does not:

- make an APPLY, HOLD, or SKIP recommendation;
- apply salary, location, or application-history logic; or
- infer employment or legal eligibility.

## Evidence Model

- **Direct evidence:** the resume demonstrates the qualification as written without relying on an unstated fact or equivalence.
- **Adjacent evidence:** the resume shows related or transferable experience, but not the qualification itself.
- **Missing evidence:** the qualification is not demonstrated by the supplied resume.

The analysis must not invent candidate facts or silently treat adjacent experience as direct evidence. It preserves whether evidence comes from professional, project, or academic work. Missing evidence means only "not demonstrated by the supplied resume," not proof that the candidate lacks the qualification. Role level is evaluated from demonstrated scope and responsibility, not title alone.

## Usage

Provide a resume and a sufficiently complete JD, then invoke or read the Skill according to the host agent's Skill mechanism.

## Repository Structure

- `SKILL.md` — Skill instructions
- `references/` — supporting policies and rubrics
- `evals/cases/` — evaluation fixtures
- `evals/baseline.md` — latest committed qualitative baseline
- `evals/README.md` — evaluation procedure

## Evaluation Status

The current qualitative baseline passes 13/13 fixtures. This is a model-reviewed qualitative evaluation, not a deterministic automated test suite or a statistical reliability claim.

## License

MIT License. See `LICENSE`.
