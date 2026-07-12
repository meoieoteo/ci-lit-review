# Primary Review: garriga2023_mental_health_crises_notes

## Review Status

primary_review_complete

## Review-Relevant Contribution

Indirect but useful evidence that clinical notes can improve short-horizon EHR risk prediction when fused with structured data.

## Publication Status and Evidence Weight

Peer-reviewed journal article. Evidence weight is high for its own mental-health task but indirect for dementia and cardiology.

## Fit to Problem Statement

Useful analogy for multimodal structured-plus-text risk prediction and weekly rolling prediction. It does not address dementia labels.

## Evidence Category

`unstructured_ehr_text`; `longitudinal_ehr_representation`; `validation_or_reporting_quality`; `background_or_context`

## Clinical Target

Mental health crisis relapse within 28 days.

## Data and Cohort Relevance

Mental-health EHR data are not clinically aligned with cardiology cognitive screening, but the longitudinal prediction setup is relevant.

## EHR Text Relevance

High for note embeddings as additive signal.

## Label or Outcome Relevance

Outcome is a crisis event, not cognitive impairment.

## Modeling Relevance

Relevant for structured/text fusion, low-prevalence AUPRC reporting, and SHAP interpretation.

## Validation and Utility Signals

The ensemble model improved AUPRC and AUROC over baselines, but direct utility for dementia is analogical.

## Bias, Causality, and Downstream Action Issues

Crisis events are care-pathway outcomes and can reflect access and service contact.

## Portability and Implementation Signals

Demonstrates that note availability and note frequency matter for model performance.

## Key Extracted Claims

- 59,750 patients and eight years of EHR data.
- Hybrid note/structured approach achieved mean AUPRC 0.133 and AUROC 0.865.
- Notes improved performance when available.

## What This Paper Supports

Structured-plus-note fusion can improve short-horizon clinical risk prediction.

## What This Paper Does Not Support

It does not provide dementia-specific labels, cognitive concepts, or cardiology evidence.

## Default Specialist Reviews Called

All current specialist reviewers are called.

## Additional Specialist Reviews Needed

None.

## Primary Reviewer Notes

Use as a multimodal prediction analogy.
