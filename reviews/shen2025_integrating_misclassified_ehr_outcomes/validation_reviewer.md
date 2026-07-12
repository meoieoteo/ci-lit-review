# Validation Review: shen2025_integrating_misclassified_ehr_outcomes

## Review Status

specialist_complete

## Validation Design

The paper is centered on validation design. It assumes a large cohort with a misclassified binary outcome and a smaller validation sample with the true outcome. It then evaluates estimators that account for both outcome misclassification and non-probability validation-sample selection.

## External or Gold-Standard Validation

The ACT application uses autopsy neuropathology as the gold-standard outcome relative to clinical Alzheimer disease diagnosis. The validation sample is non-random, which is the methodological problem the paper addresses.

## Strengths

- Directly addresses imperfect EHR outcomes.
- Makes validation-sample selection explicit.
- Uses simulation to compare naive, misclassification-corrected, and selection-corrected estimators.
- Provides an applied Alzheimer disease example.

## Limitations

- Preprint status.
- The framework is causal-effect estimation rather than prediction validation.
- Assumptions about selection and outcome models may fail in real EHR validation samples.
- Validation information may be unavailable for many cardiology patients.

## Implications for Our Validation Plan

If local chart review or adjudication is used to validate EHR dementia labels, sampling should be planned rather than incidental. The validation sample should include code-positive, code-negative, high-risk, and low-risk patients so sensitivity, specificity, and selection bias can be estimated.

## Evidence Weight

`lower_weight_methods_preprint`; `useful_for_validation_design`

## Recommended Use

Use to justify explicit validation-sample sampling and misclassification sensitivity analysis.
