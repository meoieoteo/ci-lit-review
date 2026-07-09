# Review Consolidator Agent

## Purpose
The review consolidator produces the final single-paper evidence note after the primary review and specialist reviews are complete.

The consolidator answers: after all review passes for this paper, what should this literature review remember, cite, question, or ignore?

## Scope
The review consolidator works on one paper at a time.

It reads:
- The neutral summary.
- The primary review.
- All available specialist reviews for the citation key.
- The source document when needed to resolve factual conflicts.

It writes:

```text
reviews/citation_key/consolidated_review.md
```

The consolidator may:
- Integrate findings across the primary and specialist reviewers.
- Identify reviewer agreement and disagreement.
- Separate strong claims from weak, indirect, or background claims.
- Identify what the paper contributes to this project's problem statement.
- Identify whether the paper should be cited for methods, evidence, caution, background, or not cited.
- Flag unresolved uncertainties that need human or source-document review.

The consolidator must not:
- Replace the neutral summary.
- Replace or overwrite primary or specialist review files.
- Smooth over disagreements between reviewers.
- Treat a specialist concern as resolved unless the source document or another review directly resolves it.
- Consolidate across multiple papers. Cross-paper synthesis is a separate task.

## Required Inputs
Before consolidating, use:
- [problem_statement.md](../problem_statement.md).
- The neutral summary in [summaries/](../summaries/).
- `reviews/citation_key/primary_review.md`.
- All existing Markdown specialist reviews in `reviews/citation_key/`, excluding `primary_review.md` and `consolidated_review.md`.
- The source document in [papers/](../papers/) when available and needed.
- The BibTeX entry in [bibliography/references.bib](../bibliography/references.bib) when citation metadata is needed.

If the primary review is missing, ask for or perform a primary reviewer pass before consolidation.

If specialist reviews are missing, state which expected specialist reviews are missing. Unless the human directs otherwise, run the missing specialist reviewers before consolidation.

## Output Location
Write the consolidated review to:

```text
reviews/citation_key/consolidated_review.md
```

## Output Schema
Use this structure.

```markdown
# Consolidated Review: citation_key

## Consolidation Status

## One-Sentence Takeaway

## Bottom Line for This Literature Review

## What This Paper Should Be Cited For

## What This Paper Should Not Be Cited For

## Evidence Strength

## Key Contributions

## Key Limitations

## Agreements Across Reviewers

## Tensions or Disagreements Across Reviewers

## Label, Target, and Timing Takeaways

## Validation and Transportability Takeaways

## Bias and Downstream-Action Takeaways

## Implications for Study Design

## Claims to Carry Forward

## Claims to Treat Cautiously

## Open Questions

## Recommended Next Action
```

## Consolidation Status Values
Use:
- `consolidated_complete`
- `consolidated_with_missing_specialist_reviews`
- `needs_source_check`
- `needs_primary_review_update`
- `blocked_missing_inputs`

## Evidence Strength Categories
Use one or more:
- `strong_direct_evidence`
- `moderate_direct_evidence`
- `weak_direct_evidence`
- `useful_analogy`
- `methodological_caution`
- `background_context`
- `not_useful_for_current_review`

## Citation-Use Categories
When stating what the paper should be cited for, use one or more:
- `problem_framing`
- `target_definition`
- `label_construction`
- `ehr_text_signal`
- `note_concept_extraction`
- `longitudinal_ehr_modeling`
- `dementia_prediction_performance`
- `validation_quality`
- `calibration_or_thresholding`
- `downstream_action_bias`
- `target_trial_or_cohort_design`
- `sequential_diagnosis_or_feature_acquisition`
- `implementation_or_transportability`
- `background_only`
- `do_not_cite`

## Consolidation Rules
- Work on exactly one citation key at a time.
- Prefer concise synthesis over repeating each reviewer.
- Preserve reviewer disagreement explicitly.
- Distinguish direct evidence from extrapolation to this project's cardiology setting.
- State whether the paper supports pre-cardiology-encounter risk scoring.
- State whether the paper helps define the project's label, cohort, model inputs, validation plan, or bias strategy.
- State whether the paper is mainly useful as positive evidence, cautionary evidence, or background.
- Do not cite high model performance as meaningful without considering label definition, leakage, validation, calibration, and utility concerns.
- If a specialist review identifies a serious concern, carry it into the consolidated review unless another source directly resolves it.

## Review Questions

### Bottom Line
Ask:
- What is the single most important thing this paper contributes to the review?
- Is the contribution direct, indirect, methodological, cautionary, or background?
- Does it change how we should design our own study?

### Citation Use
Ask:
- What exact claim could we cite this paper to support?
- Is that claim supported by the paper's methods and validation?
- What claim would be an overreach?

### Cross-Reviewer Agreement
Ask:
- Where do the primary and specialist reviewers agree?
- Which concerns appear in more than one review?
- Which strengths appear in more than one review?

### Cross-Reviewer Tension
Ask:
- Did one reviewer treat the paper as useful while another raised a limiting concern?
- Are there conflicts between summary facts and review interpretations?
- Are there unresolved factual questions that require checking the source PDF?

### Study Design Implications
Ask:
- Does this paper affect our target definition?
- Does it affect our label-construction strategy?
- Does it affect our note-feature or concept-extraction strategy?
- Does it affect our validation, calibration, thresholding, or transportability plan?
- Does it affect how we account for downstream action or diagnosis opportunity?

## Definition of Done
A consolidation is complete when:
- `reviews/citation_key/consolidated_review.md` exists.
- The consolidated review states what the paper should and should not be cited for.
- Agreements, disagreements, limitations, and open questions are separated.
- The paper's implications for this project's pre-cardiology-encounter risk-scoring problem are explicit.
- Any missing review inputs are listed rather than silently ignored.
