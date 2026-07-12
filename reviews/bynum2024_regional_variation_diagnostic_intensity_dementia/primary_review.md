# Primary Review: bynum2024_regional_variation_diagnostic_intensity_dementia

## Review Status

primary_review_complete

## Review-Relevant Contribution

This is direct evidence that future ADRD diagnosis is partly an observation process: after adjustment for measured regional risk and general diagnostic intensity, the likelihood of receiving a new ADRD diagnosis still varies by hospital referral region.

## Publication Status and Evidence Weight

Peer-reviewed journal article with high relevance to Section 5. Evidence weight is moderate-to-high for claims about geographic variation in ADRD diagnosis intensity, but not for causal claims about why that variation occurs.

## Fit to Problem Statement

Strong fit for the problem statement's concern that equivalent patients may receive different cognitive labels because one is more likely to be diagnosed. It is not cardiology-specific and does not build a prediction model.

## Evidence Category

`downstream_action_bias`; `label_definition`; `validation_or_reporting_quality`; `background_or_context`

## Clinical Target

New ADRD diagnosis in claims, not true incident dementia.

## Data and Cohort Relevance

Uses national Medicare fee-for-service claims and HRR-level analysis. The cohort is older adults age 66+; not encounter-level and not cardiology-specific.

## EHR Text Relevance

None. The paper uses claims diagnosis codes and regional covariates.

## Label or Outcome Relevance

Very high. The paper explicitly separates diagnosed cases from expected cases and names "diagnosis intensity" as a construct.

## Modeling Relevance

Indirect. The observed-to-expected diagnosis-intensity measure could inspire sensitivity analyses or adjustment/stratification variables for label observability.

## Validation and Utility Signals

The study uses a validated claims algorithm and STROBE reporting. It does not validate true dementia status by chart review or cognitive testing.

## Bias, Causality, and Downstream Action Issues

Central. The paper shows that place of residence is associated with diagnosis likelihood, particularly among younger-old, Black, and Hispanic beneficiaries.

## Portability and Implementation Signals

The approach is implementable with claims and regional covariates. Translating it to a local Epic pre-cardiology cohort would require local measures of diagnosis opportunity rather than HRR-level intensity alone.

## Key Extracted Claims

- New ADRD diagnosis rates varied across HRRs from 1.7 to 5.4 per 100.
- ADRD-specific diagnosis intensity ranged from 0.69 to 1.47.
- Variation was largest among adults aged 66-74 and Black and Hispanic groups.
- Diagnosis intensity was associated with about a two-fold difference in individual probability of receiving an ADRD diagnosis.

## What This Paper Supports

- Future coded dementia diagnosis is not only disease state; it is also shaped by diagnosis opportunity.
- Geographic and subgroup variation should be considered when using diagnosis codes as outcomes.
- Section 5 can cite "diagnostic intensity" directly.

## What This Paper Does Not Support

- It does not prove which health system mechanisms cause the variation.
- It does not validate a pre-cardiology cognitive-risk label.
- It does not show how to correct local EHR labels.

## Default Specialist Reviews Called

All five default specialist reviewers.

## Additional Specialist Reviews Needed

None beyond source-checking the supplement if exact code algorithm details are needed.

## Primary Reviewer Notes

This should become a core Section 5 paper after consolidation.
