# Primary Review: lyu2022_multimodal_mortality_notes

## Review Status

primary_review_complete

## Review-Relevant Contribution

Indirect methods evidence for multimodal transformer fusion of structured EHR time series and clinical-note embeddings.

## Publication Status and Evidence Weight

Conference/preprint source with useful methods relevance but indirect clinical relevance. Evidence weight for dementia manuscript claims is low except as method background.

## Fit to Problem Statement

Relevant to multimodal fusion architecture and interpretability; not relevant to dementia target construction or cardiology encounters.

## Evidence Category

`unstructured_ehr_text`; `longitudinal_ehr_representation`; `validation_or_reporting_quality`; `background_or_context`

## Clinical Target

ICU in-hospital mortality.

## Data and Cohort Relevance

MIMIC-III ICU data are not aligned with outpatient cardiology.

## EHR Text Relevance

Moderate-to-high for note embedding and fusion mechanics.

## Label or Outcome Relevance

Mortality label is not relevant to cognitive impairment, though timing discipline is informative.

## Modeling Relevance

High for multimodal transformer design.

## Validation and Utility Signals

Held-out test performance is reported; external validation, calibration, and clinical utility are limited.

## Bias, Causality, and Downstream Action Issues

ICU documentation and early-treatment decisions shape both notes and outcomes.

## Portability and Implementation Signals

The architecture is portable in principle, but MIMIC-specific note timing and variable definitions limit direct reuse.

## Key Extracted Claims

- Uses first 48 hours of ICU data.
- Reports AUCPR 0.538, AUROC 0.877, and F1 0.490.
- Includes integrated gradients and Shapley-style interpretation.

## What This Paper Supports

Multimodal transformer fusion is a plausible EHR architecture.

## What This Paper Does Not Support

It does not support dementia-specific performance or outpatient implementation claims.

## Default Specialist Reviews Called

All current specialist reviewers are called.

## Additional Specialist Reviews Needed

None.

## Primary Reviewer Notes

Background methods citation only.
