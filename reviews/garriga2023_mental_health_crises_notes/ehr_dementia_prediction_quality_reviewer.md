# Specialist Review: EHR Dementia Prediction Quality

## Specialist Scope

Non-dementia multimodal EHR text prediction analogy.

## Bottom Line

Not dementia evidence, but useful for short-horizon structured-plus-note prediction design and low-prevalence metrics.

## Prediction Task Clarity

Weekly prediction of mental health crisis relapse within 28 days.

## Index Date, Observation Window, and Prediction Horizon

Weekly index with 28-day horizon.

## Data Source and Cohort Definition

Mental-health EHR data across eight years.

## Outcome and Reference Standard

Mental health crisis event, a care-event outcome.

## Comparator or Control Group

Weeks without crisis in the prediction horizon.

## EHR Text and Structured Data Use

Structured features plus BERT-derived note embeddings.

## Missing Data and Feature Availability

Note availability affects prediction; ensemble accounts for note presence.

## Validation

Retrospective internal validation.

## Calibration, Thresholds, and Clinical Utility

AUPRC/AUROC reported; dementia-relevant thresholds not established.

## Reporting and Reproducibility

Useful metric reporting; local features and notes limit reproducibility.

## Care-Pathway and Downstream-Action Bias

Crisis labels depend on service contact and documentation.

## Implementation Readiness

Not relevant to dementia implementation readiness.

## Strengths

Rolling horizon, multimodal comparison, AUPRC reporting.

## Concerns

Different disease area and care-event label.

## Missing Information

Calibration and external validation.

## Implications for This Literature Review

Use as a method analogy for multimodal EHR prediction.

## Recommended Follow-up

Do not cite for dementia claims.
