# Specialist Review: EHR Dementia Prediction Quality

## Specialist Scope

Non-dementia ICU multimodal preprint with reliability metrics.

## Bottom Line

Not dementia evidence, but useful for thinking about uncertainty/reliability metrics in multimodal EHR models.

## Prediction Task Clarity

Mortality and prolonged length-of-stay prediction.

## Index Date, Observation Window, and Prediction Horizon

ICU admission with first 24 hours as predictor window.

## Data Source and Cohort Definition

MIMIC-III ICU stays.

## Outcome and Reference Standard

Mortality and PLOS.

## Comparator or Control Group

Survivors/non-PLOS stays.

## EHR Text and Structured Data Use

Structured features plus free-text note encoders.

## Missing Data and Feature Availability

Structured variables are filtered by missingness; note types are restricted.

## Validation

Internal splits and multiple random seeds; no external validation.

## Calibration, Thresholds, and Clinical Utility

Brier score and NLL are reported; no clinical utility.

## Reporting and Reproducibility

Preprint with benchmark-style reporting and standard data source.

## Care-Pathway and Downstream-Action Bias

PLOS is care-process sensitive; ICU treatment affects outcomes.

## Implementation Readiness

Not relevant to dementia deployment.

## Strengths

Reliability metrics, multimodal baselines, multiple seeds.

## Concerns

Preprint, non-dementia target, no external validation.

## Missing Information

Prospective utility and external calibration.

## Implications for This Literature Review

Use for reporting Brier/NLL or uncertainty-aware fusion as method context.

## Recommended Follow-up

Do not cite for dementia evidence.
