# Primary Review: song2022_home_health_notes

## Review Status

primary_review_complete

## Review-Relevant Contribution

Indirect clinical-risk evidence that note-derived features improve prediction beyond structured EHR/assessment data in home health care.

## Publication Status and Evidence Weight

Peer-reviewed journal article. Evidence weight is moderate as an EHR-note prediction analogy and low for dementia-specific claims.

## Fit to Problem Statement

Relevant to the general premise that clinical notes add signal to structured data. Not dementia-specific and not cardiology-specific.

## Evidence Category

`unstructured_ehr_text`; `note_concept_extraction`; `validation_or_reporting_quality`; `background_or_context`

## Clinical Target

Hospitalization or ED visit during home health care.

## Data and Cohort Relevance

Home-health episodes differ from cardiology encounters, but the use of routine nursing and allied-health notes is relevant to broad EHR text value.

## EHR Text Relevance

High for note-derived risk factors and concerning-note features.

## Label or Outcome Relevance

Hospitalization/ED visit is a care-utilization outcome, not disease state.

## Modeling Relevance

Useful comparison of structured-only versus structured-plus-notes models.

## Validation and Utility Signals

90/10 split, cross-validation, and PRC/F-score reporting are useful. External validation is not established.

## Bias, Causality, and Downstream Action Issues

Utilization outcomes reflect care access, clinical decisions, and documentation intensity.

## Portability and Implementation Signals

OASIS and Omaha System features may not transport directly to cardiology, but the structured-plus-text design is informative.

## Key Extracted Claims

- 86,823 episodes, with 9.6% hospitalization/ED outcome.
- SVM highest F-score at 0.82; Random Forest highest PRC area at 0.864.
- Clinical notes improved F-score by up to 16.6% and PRC area by up to 17.8%.

## What This Paper Supports

Note features can improve risk prediction over structured assessment/EHR variables.

## What This Paper Does Not Support

It does not support dementia-specific target definitions or cardiology deployment.

## Default Specialist Reviews Called

All current specialist reviewers are called.

## Additional Specialist Reviews Needed

None.

## Primary Reviewer Notes

Use as a non-dementia EHR-text risk-prediction analogy.
