# Primary Review: liu2024_detection_rates_mci_primary_care

## Review Status

primary_review_complete

## Review-Relevant Contribution

This paper localizes MCI underdetection to primary care clinicians and practices, providing direct evidence that diagnosis opportunity depends on clinician/practice behavior.

## Publication Status and Evidence Weight

Peer-reviewed journal article. High Section 5 relevance; moderate-to-high evidence for low MCI detection, with expected-rate model caveats.

## Fit to Problem Statement

Strong. It supports the idea that future MCI labels depend on primary care recognition and documentation.

## Evidence Category

`downstream_action_bias`; `label_definition`; `clinical_decision_support`; `background_or_context`

## Clinical Target

Claims-documented MCI among attributed primary-care patient panels.

## Data and Cohort Relevance

National Medicare FFS/MA primary care attribution. Not cardiology-specific.

## EHR Text Relevance

None.

## Label or Outcome Relevance

Very high for MCI diagnosis-code undercapture.

## Modeling Relevance

Indirect. Primary care contact and clinician/practice detection propensity are candidate diagnosis-opportunity covariates.

## Validation and Utility Signals

HRS-derived expected rates; clinician/practice confidence interval inference. No chart validation.

## Bias, Causality, and Downstream Action Issues

Central: clinicians/practices differ in observed diagnosis relative to expected rates.

## Portability and Implementation Signals

Useful for defining provider/practice-level detection opportunity, but local implementation requires attribution logic.

## Key Extracted Claims

- Average MCI detection rate was 0.08 for clinicians and practices.
- 99.9% of clinicians and 99.8% of practices had observed rates below expected.
- Geriatric clinicians had higher detection than other primary care specialties, but still below expected.

## What This Paper Supports

MCI is underdetected in primary care, and clinician/practice context affects diagnosis labels.

## What This Paper Does Not Support

It does not validate MCI codes against charts or cognitive testing in Medicare.

## Default Specialist Reviews Called

All five default specialist reviewers.

## Additional Specialist Reviews Needed

None.

## Primary Reviewer Notes

Use as direct Section 5 evidence for primary-care diagnosis opportunity.
