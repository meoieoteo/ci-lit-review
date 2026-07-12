# Primary Review: ruan2025_icu_multimodal_notes

## Review Status

primary_review_complete

## Review-Relevant Contribution

Indirect methods evidence for multimodal fusion with explicit reliability metrics when combining structured ICU data and free-text notes.

## Publication Status and Evidence Weight

Preprint with indirect clinical relevance. Evidence weight for this review is low-to-moderate as method context and low for manuscript claims about dementia.

## Fit to Problem Statement

Relevant to multimodal fusion and reliability evaluation, not to dementia, cardiology, or outpatient pre-encounter scoring.

## Evidence Category

`unstructured_ehr_text`; `longitudinal_ehr_representation`; `validation_or_reporting_quality`; `background_or_context`

## Clinical Target

ICU mortality and prolonged length of stay.

## Data and Cohort Relevance

MIMIC-III ICU data are not aligned with cardiology cognitive-risk deployment.

## EHR Text Relevance

Moderate-to-high for using note types and BERT-family encoders in multimodal fusion.

## Label or Outcome Relevance

Outcomes are ICU utilization/mortality endpoints, not cognitive impairment labels.

## Modeling Relevance

Relevant for evidence fusion, uncertainty/reliability metrics, and multimodal comparison.

## Validation and Utility Signals

Reports discrimination plus Brier score and NLL across random seeds. External validation is absent.

## Bias, Causality, and Downstream Action Issues

ICU outcomes and notes are affected by treatment processes during the first 24 hours.

## Portability and Implementation Signals

Method ideas may transfer, but feature domains, note types, and timing differ sharply from outpatient cardiology.

## Key Extracted Claims

- Uses first 24 hours of MIMIC-III structured data and notes.
- Evaluates mortality and prolonged length of stay.
- Reports gains in AUROC/AUPRC and reliability metrics over baselines.

## What This Paper Supports

Reliability metrics and uncertainty-aware multimodal fusion are useful design considerations.

## What This Paper Does Not Support

It does not provide dementia-specific evidence or a validated cardiology workflow model.

## Default Specialist Reviews Called

All current specialist reviewers are called.

## Additional Specialist Reviews Needed

None.

## Primary Reviewer Notes

Use as method background with preprint caution.
