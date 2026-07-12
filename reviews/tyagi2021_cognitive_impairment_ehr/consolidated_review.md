# Consolidated Review: tyagi2021_cognitive_impairment_ehr

## Consolidation Status

consolidated_complete

## One-Sentence Takeaway

Tyagi 2021 shows high ClinicalBERT performance for cognitive-impairment snippet classification, but it is a lower-weight NLP component paper rather than patient-level dementia prediction evidence.

## Bottom Line for This Literature Review

Use for feasibility of transformer-based cognitive evidence extraction and for annotation distinctions, not for risk-model performance claims.

## What This Paper Should Be Cited For

`note_concept_extraction`; `ehr_text_signal`; `background_only`

## What This Paper Should Not Be Cited For

Do not cite for patient-level future dementia prediction, cardiology deployment, or external validity.

## Publication Status and Evidence Weight

Direct topical fit but lower evidentiary weight because it is a short ML4H/arXiv-style source and lacks full validation.

## Evidence Strength

`weak_direct_evidence`; `lower_publication_weight`

## Key Contributions

Annotated snippets, ClinicalBERT baseline comparison, and explicit rule that concern alone is not cognitive impairment.

## Key Limitations

Snippet-level task, keyword-enriched cohort, no external validation, no patient-level risk score.

## Agreements Across Reviewers

All reviewers agree it is useful NLP feasibility evidence but not outcome prediction evidence.

## Tensions or Disagreements Across Reviewers

No major disagreement.

## Label, Target, and Timing Takeaways

Snippet labels are not patient labels. The distinction between concern and impairment is useful.

## Validation and Transportability Takeaways

High internal metrics require local validation and patient-level aggregation.

## Bias and Downstream-Action Takeaways

Keyword sampling biases the task toward already documented concern.

## Implications for Study Design

If using snippet classifiers, define aggregation to patient/encounter features and validate on unselected notes.

## Claims to Carry Forward

ClinicalBERT can classify explicit cognitive impairment evidence in EHR text.

## Claims to Treat Cautiously

Sequence-level AUC does not imply patient-level risk prediction performance.

## Open Questions

How does the classifier perform on outpatient cardiology notes without keyword enrichment?

## Recommended Next Action

Use as NLP feasibility/background with publication-status caution.
