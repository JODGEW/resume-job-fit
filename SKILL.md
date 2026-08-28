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
6. Before emitting the evaluation, audit the draft against the rules in this file and the referenced files, and correct the draft rather than describing the audit. Check at least the following:
   - Every row ID cited in Core Fit or Overall Qualitative Synthesis exists, and that row's evidence class supports the claim it is cited for. An ID or range cited for a directly supported or demonstrated claim resolves only to `Direct evidence` rows. Every Adjacent or Missing finding named in those sections carries its row ID.
   - Every `Missing evidence` row's resume-evidence cell reads exactly `No relevant evidence identified in the supplied resume`. If the row or its evaluation names related resume evidence, reclassify the row as `Adjacent evidence` and state the remaining gap.
   - For every compound JD criterion, identify each activity, technique, or technology the criterion names (for example, "retries" and "backoff" in "implement retries and backoff") and verify each against the supplied resume before finalizing the row's evidence class; alternatives the JD joins with "or" remain one component. Components are materially distinct whenever the resume evidence for them differs. If they resolve to different evidence classes, split them into separate rows as the Output Invariants require; do not let missing evidence for one component erase related or direct evidence for another, and do not let evidence for one component supply the class of a component the resume does not address. After splitting a compound criterion, do not retain a parent row that assigns a single evidence class to the combined components; evaluate those components only in their split rows.
   - Every Material Uncertainty is grounded in identifiable ambiguous or conflicting wording from the supplied resume or job description. Remove any that rests on resume silence, on an unmet clearly stated criterion, or on whether a stated criterion is really expected.

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
- When a compound JD responsibility or requirement contains materially distinct components supported at different evidence classes, explicitly evaluate each component separately. If Alignment Analysis evaluates responsibility alignment, every split responsibility component must appear there; discussion under a hard requirement, specialization, or primary-technology row does not substitute for that responsibility evaluation. For example, for "deploy and operate services in Kubernetes," include separate responsibility rows for deployment and ongoing operation; if deployment is `Adjacent evidence` and operation is `Missing evidence`, both rows must appear. Cross-references to `H`, `P`, `R`, or technology rows may reduce repetition but must not replace a component's evaluation.
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
