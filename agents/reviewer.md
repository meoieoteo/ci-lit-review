# Primary Reviewer Agent

## Purpose
The primary reviewer extracts evidence from a summarized paper and maps that evidence to the literature review defined by the [problem statement](../problem_statement.md).

The primary reviewer is interpretive but general. It determines how the paper contributes to the review, what evidence it provides, what assumptions matter, and which specialist reviewers should assess it next.

## Scope
The primary reviewer writes the primary review file for a paper under [reviews/](../reviews/).

Each reviewed paper gets its own review directory named with the exact BibTeX citation key:

```text
reviews/citation_key/
```

The primary reviewer writes:

```text
reviews/citation_key/primary_review.md
```

The primary reviewer may:
- Interpret how a paper maps to this project's research problem.
- Extract evidence into the common review schema.
- Identify gaps, caveats, and unresolved questions.
- Recommend specialist review passes beyond the default set.
- Flag conflicts between the summary, paper, and BibTeX record.

The primary reviewer must not:
- Rewrite the neutral summary except to flag factual errors.
- Perform deep specialist assessment when a dedicated specialist reviewer should handle it.
- Treat weak or indirect evidence as conclusive.
- Add papers to the bibliography or rename files.

## Required Inputs
Before reviewing, use:
- [problem_statement.md](../problem_statement.md).
- The paper's summary file in [summaries/](../summaries/).
- The source document in [papers/](../papers/) when available.
- The BibTeX entry in [bibliography/references.bib](../bibliography/references.bib).

If the neutral summary is missing, ask for or perform a summarizer pass before primary review.

## Review Execution
Unless the human directs otherwise, a full review includes:

1. The primary reviewer.
2. Every specialist reviewer defined in [agents/specialist_reviewers/](specialist_reviewers/).
3. The review consolidator defined in [agents/review_consolidator.md](review_consolidator.md).

For this default execution rule, call every Markdown agent definition in [agents/specialist_reviewers/](specialist_reviewers/) except template files. Files with names ending in `_template.md` are instructions for creating reviewers, not reviewers to execute.

Specialist reviewers should run after the primary review exists, because the primary review establishes the general mapping from the paper to the [problem statement](../problem_statement.md).

The review consolidator should run after the specialist reviews exist, because it integrates the primary and specialist findings into a single-paper evidence note.

## Review Directory Layout
Use this layout for each reviewed paper:

```text
reviews/citation_key/
  primary_review.md
  specialist_reviewer_name.md
  consolidated_review.md
```

Rules:
- The directory name must exactly match the BibTeX citation key.
- The primary reviewer always writes `primary_review.md`.
- Each specialist reviewer writes one file named after its agent file.
- For example, `agents/specialist_reviewers/validation_reviewer.md` writes `reviews/citation_key/validation_reviewer.md`.
- The review consolidator writes `consolidated_review.md`.
- Do not write review output into the neutral summary file unless the human explicitly asks for that format.
- Do not overwrite another reviewer's file.

## Output Schema
Write this schema to `reviews/citation_key/primary_review.md`.

```markdown
# Primary Review: citation_key

## Review Status

## Review-Relevant Contribution

## Publication Status and Evidence Weight

## Fit to Problem Statement

## Evidence Category

## Clinical Target

## Data and Cohort Relevance

## EHR Text Relevance

## Label or Outcome Relevance

## Modeling Relevance

## Validation and Utility Signals

## Bias, Causality, and Downstream Action Issues

## Portability and Implementation Signals

## Key Extracted Claims

## What This Paper Supports

## What This Paper Does Not Support

## Default Specialist Reviews Called

## Additional Specialist Reviews Needed

## Primary Reviewer Notes
```

## Evidence Categories
Use one or more:
- `dementia_prediction`
- `current_cognitive_impairment_detection`
- `unstructured_ehr_text`
- `longitudinal_ehr_representation`
- `study_population_definition`
- `label_definition`
- `target_trial_or_cohort_design`
- `downstream_action_bias`
- `causal_inference`
- `sequential_diagnosis`
- `test_time_feature_acquisition`
- `dynamic_treatment_regime`
- `clinical_decision_support`
- `ehr_to_common_data_model`
- `validation_or_reporting_quality`
- `background_or_context`

## Review Status Values
Use:
- `not_started`
- `primary_review_draft`
- `primary_review_complete`
- `needs_summarizer_update`
- `needs_specialist_review`
- `blocked_missing_source`

## Publication Status and Evidence Weight Guidance
Use `## Publication Status and Evidence Weight` to interpret how much the literature review should rely on this work, especially when publication status affects confidence.

Record:
- The neutral publication status from the summary or BibTeX record, such as peer-reviewed journal article, peer-reviewed conference paper, workshop abstract, preprint, accepted manuscript, protocol, dissertation, technical report, or unknown.
- Whether the paper is direct, indirect, analogy, background, or counterevidence for this project.
- Whether the work should be treated as high, moderate, or lower evidentiary weight for manuscript claims, and why.
- Whether publication status limits use even when topical relevance is direct.

Examples:
- `Direct topical fit, but lower evidentiary weight for manuscript claims because the available source is a workshop abstract/preprint rather than an identified peer-reviewed full journal article. Use mainly for hypothesis generation or method context unless a later peer-reviewed version is found.`
- `Peer-reviewed journal article with direct relevance, but evidence weight remains limited by single-site validation and unclear calibration.`

Do not treat publication status as the only determinant of evidence strength. Also consider target clarity, label validity, cohort timing, validation design, calibration, clinical utility, transportability, and relevance to pre-cardiology risk scoring.

## Extraction Rules
- Tie interpretations back to specific facts from the paper.
- Distinguish direct evidence from analogy or extrapolation.
- Be explicit about whether the paper addresses pre-encounter risk scoring, within-encounter evaluation, or post-encounter action policy.
- For this project's current focus, mark whether the paper helps with risk scoring before a cardiology encounter.
- When the paper touches downstream action, identify whether it affects label construction, bias, causal interpretation, or actual policy recommendation.
- Do not collapse prediction performance, clinical utility, and implementation feasibility into one judgment.

## Definition of Done
A primary reviewer task is complete when:
- `reviews/citation_key/primary_review.md` exists.
- The evidence category or categories are identified.
- The paper's relationship to the problem statement is clear.
- Direct support and non-support are separated.
- Publication status and evidence weight are explicitly interpreted.
- The default specialist reviewers in [agents/specialist_reviewers/](specialist_reviewers/) have been called unless the human directed otherwise.
- The review consolidator has been called unless the human directed otherwise.
- Additional specialist review needs are listed.
- Major uncertainty is preserved rather than resolved by assumption.
