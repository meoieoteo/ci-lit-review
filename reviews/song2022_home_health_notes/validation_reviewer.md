# Specialist Review: Validation

## Specialist Scope

Validation of home-health hospitalization/ED prediction with note features.

## Bottom Line

Good internal comparison of structured versus note-augmented models; external validation is missing.

## Validation Design Summary

90% training and 10% testing with tenfold cross-validation.

## Development and Validation Separation

LASSO feature selection and model tuning require source checking for separation from test data.

## Internal Validation

Internal holdout and cross-validation.

## Temporal Validation

No temporal validation.

## External Validation

None.

## Transportability

OASIS/Omaha features are setting-specific.

## Calibration

Not emphasized.

## Thresholds and Operating Points

F-score and PRC area reported; threshold clinical use not established.

## Clinical Utility

Potential early warning use discussed, but outcome benefit not tested.

## Subgroup and Fairness Evaluation

Not central.

## Robustness and Sensitivity Analyses

Multiple model families and feature sets compared.

## Reporting Completeness

Strong on metrics; external transport details limited.

## Reproducibility

Requires note NLP tools and OASIS mapping.

## Fit to Pre-Cardiology Risk Scoring

Useful analogy for structured-plus-notes internal validation.

## Strengths

Large episode count, PRC reporting, feature-set comparison.

## Concerns

No external validation and possible within-episode leakage.

## Missing Information

Calibration and prospective utility.

## Implications for This Literature Review

Evidence for additive note value should be paired with validation caveats.

## Recommended Follow-up

Use as non-dementia analogy.
