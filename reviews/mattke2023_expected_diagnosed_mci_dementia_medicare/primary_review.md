# Primary Review: mattke2023_expected_diagnosed_mci_dementia_medicare

## Review Status

primary_review_complete

## Review-Relevant Contribution

This paper directly quantifies the gap between expected MCI/dementia prevalence and claims-documented diagnosis in Medicare.

## Publication Status and Evidence Weight

Peer-reviewed journal article. High relevance to Section 5 and label validity. Evidence weight is moderate-to-high for under-detection of MCI in Medicare, with caveats because expected rates are model-derived.

## Fit to Problem Statement

Strong fit for the concern that absence of a future cognitive diagnosis code is not absence of cognitive impairment.

## Evidence Category

`label_definition`; `downstream_action_bias`; `validation_or_reporting_quality`; `background_or_context`

## Clinical Target

Claims-documented MCI and dementia compared with expected cognitive impairment/dementia rates.

## Data and Cohort Relevance

National Medicare FFS and Medicare Advantage data; highly relevant for claims/EHR outcome ascertainment.

## EHR Text Relevance

None.

## Label or Outcome Relevance

Very high. MCI diagnoses capture a small fraction of expected cases; dementia coding differs by subgroup.

## Modeling Relevance

Indirect. Shows why future coded MCI/dementia is a noisy, opportunity-dependent outcome.

## Validation and Utility Signals

HRS-based expected-rate model was checked against 2016 HRS data, with modest MCI discrimination and better dementia discrimination.

## Bias, Causality, and Downstream Action Issues

Strong. Detection rates differ by race/ethnicity, dual eligibility, and coverage type.

## Portability and Implementation Signals

Claims algorithms are implementable, but expected-rate modeling is not a direct local EHR label.

## Key Extracted Claims

- MCI detection rate was 0.079 in 2017-2019.
- About 7.4 million expected MCI cases among Medicare beneficiaries were undiagnosed.
- MCI detection was lower for Black and Hispanic beneficiaries than for non-Hispanic White beneficiaries.
- Dementia was diagnosed more often than expected overall but still underdetected in Black and Hispanic groups.

## What This Paper Supports

- MCI diagnosis codes are highly insensitive.
- Diagnosis-code labels are differentially observed across populations.
- Future coded diagnosis outcomes need sensitivity analyses.

## What This Paper Does Not Support

- It does not provide a chart-reviewed gold standard.
- It does not validate a cardiology encounter-level target.
- It does not use EHR text.

## Default Specialist Reviews Called

All five default specialist reviewers.

## Additional Specialist Reviews Needed

None.

## Primary Reviewer Notes

Use with Liu 2024 as a pair: population-level underdiagnosis plus clinician/practice-level detection.
