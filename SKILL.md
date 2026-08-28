---
name: resume-job-fit
description: Evaluate how well a supplied resume matches a supplied job description using only evidence in those documents. Use for evidence-based fit analysis, not application decisions or candidate preference and eligibility checks.
---

# Resume–Job Fit

## Scope

Evaluate resume-to-job fit. Identify the job's core responsibilities and explicit hard requirements, distinguish required qualifications from preferred ones, and assess:

Here, explicit hard requirements means only job-fit requirements that can legitimately be assessed from the supplied resume and that the job description itself clearly marks as non-negotiable with language such as "must have," "required without exception," "hard requirement," or equivalent explicit emphasis. Placement under a heading such as "Required Qualifications" alone does not make a criterion an explicit hard requirement. Citizenship, work authorization, security clearance, background checks, licenses, and other legal or employment eligibility conditions are out of scope and must not be inferred from resume silence.

- specialization alignment
- responsibility alignment
- experience gaps
- primary technology or programming-language gaps
- role-level alignment

## Inputs

Require both:

1. The candidate's resume.
2. The job description.

If either input is missing, incomplete, or unreadable, state the limitation and do not fill it with assumptions.

## Workflow

1. Extract the job's core responsibilities, required qualifications, preferred qualifications, and explicit hard requirements. Preserve uncertainty when the job description is ambiguous.
2. Find resume evidence relevant to each material criterion. Classify it as direct evidence, adjacent evidence, or missing evidence.
3. Distinguish professional, project, and academic evidence when the source materially affects the strength or relevance of the match.
4. Evaluate the alignment areas in Scope, emphasizing unmet required qualifications and hard requirements without ignoring preferred qualifications.
5. Produce the evaluation using [references/output-format.md](references/output-format.md), applying [references/evidence-policy.md](references/evidence-policy.md) and [references/evaluation-rubric.md](references/evaluation-rubric.md).

## Evidence Guardrails

- Use only evidence present in the supplied resume and job description.
- Tie conclusions to identifiable evidence from the relevant input.
- Never invent, infer as fact, or embellish candidate experience.
- Never silently treat adjacent evidence as direct evidence.
- Treat missing evidence as "not demonstrated by the supplied resume," not proof that the candidate lacks the qualification.
- Surface ambiguity, conflicting evidence, and uncertainty instead of guessing.
- Do not introduce numeric thresholds or a `FULL`/`PARTIAL`/`ZERO` scoring system unless the referenced policies explicitly define them.

## Output Invariants

- The only valid evidence classes are `Direct evidence`, `Adjacent evidence`, and `Missing evidence`. Never emit `Mixed`, `Partial`, or any other evidence class.
- When one JD responsibility or requirement contains materially distinct components, evaluate those components in separate rows if the supplied resume supports them at different evidence classes. Do not collapse the components under the strongest available class or use evidence for one component to upgrade another; for example, "deploy and operate services in Kubernetes" may require `Adjacent evidence` for deployment and `Missing evidence` for ongoing operation.
- Use Material Uncertainty only for genuine ambiguity in the supplied job description or resume evidence. Ordinary resume silence or an unmet clearly stated criterion is an evidence gap, not uncertainty.
- If an Alignment Analysis dimension has no material job-description criterion, state that no material criterion was identified and do not assign an evidence class.
- Do not infer role level from title or experience duration alone.

## Out of Scope

Do not evaluate, infer, or recommend based on:

- salary preferences
- location or relocation policy
- whether the candidate should apply, including `APPLY`/`HOLD`/`SKIP` decisions
- application history or duplicate detection
- employer application limits
- PERM detection
- agency or aggregator filtering
- facts about a specific candidate that are not contained in the supplied resume

Do not perform application strategy, eligibility screening, or candidate-specific policy enforcement. Return only the resume-to-job fit evaluation.
