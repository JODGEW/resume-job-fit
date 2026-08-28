# Host Compatibility

## Claude Code

Status: VERIFIED

### Installation Method

A personal Skill was installed by symlinking the repository root into Claude Code's personal skills directory:

```bash
ln -s /path/to/resume-job-fit ~/.claude/skills/resume-job-fit
```

The repository root contains `SKILL.md` and `references/`, so the Skill can keep using its existing relative references without duplicating files.

### Verification

The following were tested in a fresh Claude Code session:

1. Native discovery
   - `/resume-job-fit` appeared in Claude Code's Skill command completion.
   - The displayed command description matched the Skill metadata.
2. Native invocation without inputs
   - `/resume-job-fit` loaded the Skill and its referenced policy files.
   - With no resume or job description supplied, it correctly requested both inputs instead of fabricating an evaluation.
3. Native end-to-end execution
   - `/resume-job-fit` was invoked with the same Sam Kim resume and Platform Software Engineer job description used in the cross-model smoke test.
   - No explicit instruction to read `SKILL.md` or `references/` was included in the evaluation request.
   - Claude Code completed the Skill's normal evaluation successfully.

### Behaviors Verified

The native end-to-end run preserved the expected core behaviors:

- professional Python backend experience classified as Direct evidence
- `3+ years` classified as Direct evidence for `2022–Present` because every plausible start month satisfies the threshold as of 2026-08-27
- Docker/ECS classified as Adjacent rather than equivalent to Kubernetes
- the explicit production Kubernetes hard requirement remained not demonstrated by the supplied resume
- container-deployment evidence and ongoing service-operation evidence were kept separate when they had different evidence classes
- no Mixed, Partial, or other invented evidence class was used
- ordinary resume silence was not converted into improper Material Uncertainty
- no evidence class was assigned for role level when the JD supplied no material role-level criterion
- work-authorization eligibility was excluded from fit evidence
- no APPLY/HOLD/SKIP recommendation was produced

## Codex

Status: VERIFIED

### Tested Environment

- Codex CLI 0.150.1
- macOS Apple Silicon

### Installation Method

A personal Skill was installed by symlinking the repository root into Codex's user Skill directory:

```bash
ln -s /path/to/resume-job-fit ~/.agents/skills/resume-job-fit
```

The repository root contains `SKILL.md` and `references/`, so relative references remain intact.

### Verification

1. Native discovery
   - `$resume-job-fit` appeared as a native Skill in Codex.
   - The displayed Skill description matched the repository Skill metadata.
2. Native invocation without inputs
   - `$resume-job-fit` loaded the Skill and referenced policy files.
   - With no resume or JD supplied, Codex correctly requested both inputs instead of fabricating an evaluation.
3. Native end-to-end execution
   - `$resume-job-fit` was invoked with the Sam Kim resume and Platform Software Engineer JD.
   - No explicit instruction to read `SKILL.md` or `references/` was included.
   - Codex completed the normal evaluation successfully.

### Behaviors Verified

The final native run correctly:

- classified professional Python backend experience as Direct evidence
- classified the `3+ years` threshold as Direct evidence for `2022–Present`
- classified Docker/ECS as Adjacent rather than equivalent to Kubernetes
- preserved the production Kubernetes hard requirement as not demonstrated
- explicitly split the compound responsibility:
  - Kubernetes deployment → Adjacent evidence
  - ongoing service operation → Missing evidence
- did not let deployment evidence upgrade the operation component
- did not use Mixed, Partial, or another invented evidence class
- did not convert ordinary evidence gaps into Material Uncertainty
- assigned no role-level evidence class when the JD supplied no material role-level criterion
- excluded work authorization from fit evidence
- produced no APPLY/HOLD/SKIP recommendation

## Other Hosts

Other agent hosts remain unverified.

Manual explicit-file usage remains separately documented in the README.

## Limitations

Claude Code and Codex were each verified through one personal-Skill installation method and one environment.

This is not a universal compatibility guarantee across versions, operating systems, or other hosts.
