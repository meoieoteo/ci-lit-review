# Label Definition Review: shen2025_integrating_misclassified_ehr_outcomes

## Review Status

specialist_complete

## Label Definition Summary

The paper distinguishes a misclassified silver-standard outcome from a gold-standard validation outcome. In the ACT application, the silver-standard outcome is clinical Alzheimer disease diagnosis and the gold-standard outcome is autopsy-defined Alzheimer disease neuropathology.

## Construct Being Measured

The methods measure the consequences of outcome misclassification, not dementia risk prediction. The application contrasts clinical diagnosis with neuropathologic Alzheimer disease.

## Strengths

- Explicitly treats the EHR/clinical outcome as fallible.
- Estimates sensitivity and specificity for the silver-standard outcome in the validation sample.
- Incorporates validation-sample selection into the correction strategy.

## Weaknesses

- The gold standard may measure neuropathology rather than the clinical construct relevant to cardiology workflow.
- The method relies on modeling assumptions that may be hard to verify.
- It does not solve weak negative-label problems unless a credible validation sample exists.

## Implications for Our Labels

For a future dementia or cognitive-care label, local work should separate the operational label from the target construct and, where possible, create a validation subset with richer chart review or adjudication. Sampling into that subset must be documented and modeled.

## Label Risk Rating

`misclassification_correction_relevant`

## Recommended Use

Use as methods support for a validation-sample correction strategy, not as a direct dementia phenotype definition.
