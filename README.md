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

Tell the agent to read `SKILL.md` and the files under `references/`, provide the resume and a sufficiently complete job description, and ask it to perform the evaluation using those instructions.

Native installation, registration, or auto-discovery has not yet been verified for Claude Code, Codex/OpenAI coding agents, or other hosts; the currently verified path is explicit file reading.

## Repository Structure

- `SKILL.md` — Skill instructions
- `references/` — supporting policies and rubrics
- `evals/cases/` — evaluation fixtures
- `evals/baseline.md` — latest committed qualitative baseline
- `evals/README.md` — evaluation procedure
- `examples/basic-example.md` — representative end-to-end example
- `evals/cross-model.md` — qualitative cross-model smoke test

## Evaluation Status

The current qualitative baseline passes 14/14 fixtures. This is a model-reviewed qualitative evaluation, not a deterministic automated test suite or a statistical reliability claim.

The same clean-room smoke-test scenario also passed on GPT-5.6 Sol / High, Claude Opus 5 / xhigh, and Claude Sonnet 5 / High; see [`evals/cross-model.md`](evals/cross-model.md) for details. This verifies policy-following after the models were explicitly instructed to read the repository files, not native Skill installation or auto-discovery.

## License

MIT License. See `LICENSE`.
