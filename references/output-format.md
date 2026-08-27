# Output Format

Produce the evaluation in the Markdown structure below. Keep it concise, use tables for repeated comparisons, and include only material criteria and findings.

## Traceability Rules

- Give each qualification or alignment row a stable identifier such as `R1`, `H1`, `P1`, or `A1`. Identifiers are references only; they are not scores, ranks, or weights.
- In `JD evidence`, include a short quotation or precise paraphrase and identify its location or category in the job description when possible.
- In `Resume evidence`, include a short quotation or precise paraphrase and identify the relevant role, project, academic entry, or section.
- Keep JD requirements and resume evidence in separate columns. Do not blend them into one claim.
- Use only `Direct evidence`, `Adjacent evidence`, or `Missing evidence` in an `Evidence class` column.
- For direct or adjacent evidence, cite both the JD criterion and the supporting resume content. For missing evidence, cite the JD criterion and write `No relevant evidence identified in the supplied resume` rather than inventing a resume citation.
- State the remaining difference whenever evidence is adjacent. State the unsupported requirement or context whenever evidence is missing.
- Make every material conclusion traceable either to source evidence in its row or to the identifiers of rows that contain that evidence.
- Treat uncertainty separately from evidence class. Uncertainty is not a fourth evidence class.

## Required Structure

```markdown
# Resume–Job Fit Evaluation

## Context

- Target role: {title or identifying description from the JD}
- Source limitations: {missing, incomplete, ambiguous, or unreadable input details; otherwise state that no material source limitation was identified}

## Core Fit

{A brief evidence-grounded summary of the role's central needs, the strongest direct alignment, the most material adjacent or missing evidence, and any consequential uncertainty. Cite relevant row IDs. Do not assign an overall fit label or make an application recommendation.}

## Required Qualifications

| ID | JD requirement and evidence | Evidence class | Resume evidence | Evaluation |
|---|---|---|---|---|
| R1 | {requirement plus JD source} | {Direct evidence, Adjacent evidence, or Missing evidence} | {resume evidence and source, or the missing-evidence statement} | {supported scope, remaining gap, or uncertainty} |

{Include each material required qualification that is not already reported as an explicit hard requirement.}

## Explicit Hard Requirements

| ID | JD hard requirement and evidence | Evidence class | Resume evidence | Evaluation |
|---|---|---|---|---|
| H1 | {in-scope hard requirement plus JD source} | {Direct evidence, Adjacent evidence, or Missing evidence} | {resume evidence and source, or the missing-evidence statement} | {supported scope, remaining gap, or uncertainty} |

{Include only resume-assessable job-fit requirements that the JD clearly makes non-negotiable. Exclude legal and employment eligibility conditions. If none are identified, state that no in-scope explicit hard requirements were identified in the supplied JD.}

## Important Preferred Qualifications

| ID | JD preference and evidence | Evidence class | Resume evidence | Evaluation |
|---|---|---|---|---|
| P1 | {important preference plus JD source} | {Direct evidence, Adjacent evidence, or Missing evidence} | {resume evidence and source, or the missing-evidence statement} | {supported scope, remaining gap, or uncertainty} |

{Include preferred qualifications that are material to understanding fit. Do not mix them with required qualifications or present their absence as a required-qualification gap.}

## Alignment Analysis

| ID | Dimension | JD evidence | Evidence class | Resume evidence | Evaluation |
|---|---|---|---|---|---|
| A1 | Specialization | {JD evidence} | {evidence class} | {resume evidence or missing-evidence statement} | {alignment, difference, or uncertainty} |
| A2 | Responsibilities | {JD evidence} | {evidence class} | {resume evidence or missing-evidence statement} | {alignment, difference, or uncertainty} |
| A3 | Experience duration | {JD evidence} | {evidence class} | {resume evidence or missing-evidence statement} | {supported duration, gap, or unresolved duration} |
| A4 | Primary technology or language | {JD evidence} | {evidence class} | {resume evidence or missing-evidence statement} | {exact alignment, non-equivalent adjacency, or gap} |
| A5 | Role level | {JD evidence} | {evidence class} | {resume evidence or missing-evidence statement} | {scope, autonomy, complexity, or leadership alignment} |

{Use additional rows when a dimension contains materially different criteria with different evidence classes. Do not assign one evidence class to a mixed collection of evidence. If the JD contains no material criterion for a dimension, state that no material criterion was identified and do not assign an evidence class. Cross-reference qualification row IDs instead of repeating evidence when practical.}

## Material Uncertainties

| ID | Source evidence | What is uncertain | Affected rows | Effect on evaluation |
|---|---|---|---|---|
| U1 | {ambiguous or incomplete JD or resume wording and source} | {unresolved fact or interpretation} | {row IDs} | {how the uncertainty limits the conclusion} |

{List ambiguity or incomplete evidence that could materially change the evaluation. Keep evidence gaps classified as Missing evidence in the relevant table; do not restate ordinary resume silence as uncertainty. If none are material, state that no material uncertainty was identified from the supplied inputs.}

## Overall Qualitative Synthesis

{A concise synthesis explaining how direct evidence, adjacent evidence, missing evidence, and material uncertainties interact across the role's central requirements and alignment dimensions. Cite the relevant row IDs. Do not add a standardized fit label, numeric result, or APPLY/HOLD/SKIP recommendation.}
```

## Concision and Scope

- Prefer one precise evidence reference over repeated prose. Use row-ID cross-references when the same evidence affects multiple findings.
- Include peripheral JD details only when they materially change the fit evaluation.
- Do not include salary, location, relocation, eligibility, application history, application limits, PERM, agency or aggregator status, or any other out-of-scope factor.
- Leave the decision to the human reader. Report fit evidence, gaps, and uncertainty without recommending whether the candidate should apply.
