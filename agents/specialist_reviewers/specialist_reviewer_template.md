# Specialist Reviewer Template

## Purpose
A specialist reviewer assesses one bounded dimension of a paper after the neutral summary and primary evidence extraction exist.

Specialist reviewers should be opinionated within their domain, but they should not rewrite the neutral summary or take over the primary review.

## Scope
Create a separate agent file for each specialist reviewer in [agents/specialist_reviewers/](./), using this template as the starting point.

Examples:
- `clinical_reviewer.md`
- `ehr_schema_reviewer.md`
- `nlp_modeling_reviewer.md`
- `causal_bias_reviewer.md`
- `validation_reviewer.md`
- `target_trial_reviewer.md`
- `skeptical_reviewer.md`

Each specialist reviewer writes one Markdown file in the reviewed paper's directory:

```text
reviews/citation_key/specialist_reviewer_name.md
```

The output filename should match the specialist agent filename. For example, `agents/specialist_reviewers/validation_reviewer.md` writes `reviews/citation_key/validation_reviewer.md`.

## Required Inputs
Before specialist review, use:
- [problem_statement.md](../../problem_statement.md).
- The neutral summary in [summaries/](../../summaries/).
- The primary review in `reviews/citation_key/primary_review.md`.
- The source document in [papers/](../../papers/) when available.
- Any domain-specific standards or checklists named by the specialist agent.

If the primary review is missing, ask for a primary reviewer pass first unless the human explicitly requests a standalone specialist assessment.

## Standard Output Schema
Use this section structure unless the specialist agent defines a stricter schema.

```markdown
# Specialist Review: Reviewer Name

## Specialist Scope

## Bottom Line

## Domain-Specific Findings

## Strengths

## Concerns

## Missing Information

## Implications for This Literature Review

## Recommended Follow-up
```

## Rules
- Stay inside the specialist domain.
- Use the paper, neutral summary, and primary review as inputs, but verify important points against the source document when available.
- Clearly distinguish fatal flaws, ordinary limitations, and open questions.
- Do not change the citation key, paper filename, or bibliography.
- Do not duplicate the entire primary evidence extraction.

## Definition of Done
A specialist review is complete when:
- `reviews/citation_key/specialist_reviewer_name.md` exists.
- The review states its domain-specific bottom line.
- Findings, concerns, and missing information are separated.
- The implications for this literature review are explicit.
- Follow-up needs are listed when applicable.
