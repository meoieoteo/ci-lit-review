# Specialist Review: EHR Dementia Prediction Quality

## Specialist Scope

Non-dementia ICU multimodal transformer benchmark.

## Bottom Line

Not dementia evidence; useful only for multimodal architecture and interpretability context.

## Prediction Task Clarity

In-hospital mortality prediction.

## Index Date, Observation Window, and Prediction Horizon

ICU admission, first 48 hours, in-hospital outcome.

## Data Source and Cohort Definition

MIMIC-III ICU stays with notes.

## Outcome and Reference Standard

Mortality, a comparatively objective label.

## Comparator or Control Group

Survivors.

## EHR Text and Structured Data Use

Structured time series plus clinical-note embeddings.

## Missing Data and Feature Availability

Patients without notes excluded.

## Validation

Internal train/validation/test split.

## Calibration, Thresholds, and Clinical Utility

No dementia-relevant calibration or utility.

## Reporting and Reproducibility

MIMIC improves reproducibility but preprocessing remains important.

## Care-Pathway and Downstream-Action Bias

ICU treatment processes affect notes and outcomes.

## Implementation Readiness

Not relevant to dementia deployment.

## Strengths

Multimodal transformer, held-out test set, interpretation methods.

## Concerns

Target and setting mismatch, no external validation.

## Missing Information

Calibration and prospective use.

## Implications for This Literature Review

Use only as method background.

## Recommended Follow-up

Do not cite for dementia prediction.
