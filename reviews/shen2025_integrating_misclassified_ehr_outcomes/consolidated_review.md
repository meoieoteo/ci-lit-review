# Consolidated Review: shen2025_integrating_misclassified_ehr_outcomes

## Consolidation Status

consolidated_complete

## One-Sentence Takeaway

Shen et al. provides a methods framework for correcting misclassified EHR outcomes when a smaller, non-random validation sample has a gold-standard outcome.

## Bottom Line for This Literature Review

Useful indirect Section 4/5/10 methods support for outcome-misclassification and validation-sample design, but lower publication weight because it is a preprint and not a dementia prediction study.

## What This Paper Should Be Cited For

`label_construction`; `validation_design`; `outcome_misclassification`; `methodological_caution`

## What This Paper Should Not Be Cited For

Cardiology workflow, EHR text modeling, dementia prediction performance, or diagnosis-opportunity mechanisms.

## Publication Status and Evidence Weight

arXiv preprint. Methodologically relevant but indirect for this review.

## Evidence Strength

`indirect_methods_evidence`; `lower_publication_weight`; `validation_relevant`

## Key Contributions

The paper formalizes silver-standard EHR outcomes, gold-standard validation outcomes, misclassification correction, and validation-sample selection correction.

## Key Limitations

Not a prediction paper; not cardiology-specific; no EHR text; depends on model assumptions; uses neuropathologic Alzheimer disease rather than a cardiology-facing cognitive-care target.

## Agreements Across Reviewers

All reviewers agree the paper belongs in methodological caution and validation design rather than as direct dementia prediction evidence.

## Tensions or Disagreements Across Reviewers

No major disagreement. The main boundary is that the paper corrects outcome misclassification but does not itself define diagnosis-opportunity variables.

## Label, Target, and Timing Takeaways

Separate silver-standard operational labels from target constructs and validation outcomes. Preserve validation-sample selection information.

## Validation and Transportability Takeaways

A validation sample is not automatically representative; its sampling process can bias estimates if ignored.

## Bias and Downstream-Action Takeaways

Outcome misclassification is related to but distinct from diagnosis-opportunity bias. The paper helps with measurement error correction, not care-pathway modeling.

## Implications for Study Design

Plan a validation sample intentionally, record sampling strata and selection variables, and assess sensitivity/specificity of future diagnosis labels against chart-reviewed or adjudicated evidence.

## Claims to Carry Forward

EHR outcomes should be treated as silver-standard labels unless validated.

## Claims to Treat Cautiously

Direct use of the proposed treatment-effect estimators for prediction-model calibration or thresholding without adaptation.

## Open Questions

What local gold-standard or enriched validation outcome is feasible for cardiology patients?

## Recommended Next Action

Use as a methodological citation when designing label-validation and misclassification sensitivity analyses.
