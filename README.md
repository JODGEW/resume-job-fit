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

### Claude Code

Claude Code personal-Skill installation has been verified by symlinking the repository root:

```bash
ln -s /path/to/resume-job-fit ~/.claude/skills/resume-job-fit
```

After installation, Claude Code discovered `/resume-job-fit` natively and completed an end-to-end evaluation without an explicit instruction to read `SKILL.md` or `references/`. Native installation or registration remains unverified for Codex/OpenAI coding agents and other hosts.

## Repository Structure

- `SKILL.md` — Skill instructions
- `references/` — supporting policies and rubrics
- `evals/cases/` — evaluation fixtures
- `evals/baseline.md` — latest committed qualitative baseline
- `evals/README.md` — evaluation procedure
- `examples/basic-example.md` — representative end-to-end example
- `evals/cross-model.md` — qualitative cross-model smoke test
- `evals/host-compatibility.md` — verified host installation and execution checks

## Evaluation Status

The current qualitative baseline passes 15/15 fixtures. This is a model-reviewed qualitative evaluation, not a deterministic automated test suite or a statistical reliability claim.

The same clean-room smoke-test scenario also passed on GPT-5.6 Sol / High, Claude Opus 5 / xhigh, and Claude Sonnet 5 / High; see [`evals/cross-model.md`](evals/cross-model.md) for details. This verifies policy-following after the models were explicitly instructed to read the repository files, not native Skill installation or auto-discovery.

Claude Code native discovery, invocation, and end-to-end execution were separately verified through the symlink installation method; see [`evals/host-compatibility.md`](evals/host-compatibility.md) for details.

## License

MIT License. See `LICENSE`.
