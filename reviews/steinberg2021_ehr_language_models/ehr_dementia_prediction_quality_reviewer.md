# Specialist Review: EHR Dementia Prediction Quality

## Specialist Scope

Assessment of whether Steinberg et al. is useful for EHR dementia prediction quality.

## Bottom Line

`background_only`. The paper is not a dementia prediction study, but it informs structured longitudinal EHR representation choices.

## Prediction Task Clarity

Clear for five non-dementia tasks. Not relevant to dementia target clarity.

## Index Date, Observation Window, and Prediction Horizon

Prediction times are defined per task. Histories are represented as code sequences before prediction time.

## Data Source and Cohort Definition

Large Stanford de-identified structured EHR dataset. Not a dementia cohort.

## Outcome and Reference Standard

Operational outcomes, not dementia or cognitive impairment.

## Comparator or Control Group

Task-specific non-events.

## EHR Text and Structured Data Use

Uses structured codes only. Does not use notes, images, vitals, or quantitative lab values.

## Missing Data and Feature Availability

The paper does not provide a dementia-relevant missingness analysis.

## Validation

Temporal internal validation only.

## Calibration, Thresholds, and Clinical Utility

Not reported.

## Reporting and Reproducibility

Strong method reporting and open-source implementation signal.

## Care-Pathway and Downstream-Action Bias

Not addressed.

## Implementation Readiness

Useful as a research representation method, not as a clinical dementia model.

## Strengths

- Strong comparison to simple baselines.
- Evaluates label-scarcity settings.
- Uses temporal splits.

## Concerns

- Indirect for dementia.
- Excludes clinical notes.
- No calibration or clinical utility.

## Missing Information

Dementia-specific label behavior and performance are not studied.

## Implications for This Literature Review

Use as indirect support for a structured-EHR representation ladder.

## Recommended Follow-up

Pair with dementia-specific papers before making any cognitive-risk modeling claim.
