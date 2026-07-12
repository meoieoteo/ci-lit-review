# Specialist Review: EHR Dementia Prediction Quality

## Specialist Scope

Non-dementia home-health structured-plus-notes risk prediction.

## Bottom Line

Not dementia evidence, but useful evidence that clinical notes can improve risk prediction over structured assessment data.

## Prediction Task Clarity

Hospitalization or ED visit during home health care.

## Index Date, Observation Window, and Prediction Horizon

Home-health episode; timing of note inclusion relative to outcome needs source checking.

## Data Source and Cohort Definition

OASIS/EHR data and home-health notes from a large New York nonprofit HHC organization.

## Outcome and Reference Standard

Hospitalization/ED visit from OASIS.

## Comparator or Control Group

Episodes without hospitalization/ED visit.

## EHR Text and Structured Data Use

Structured assessment/EHR variables plus concerning-note and Omaha risk-factor note features.

## Missing Data and Feature Availability

Notes and OASIS features are specific to HHC workflows.

## Validation

90/10 split and cross-validation; no external validation.

## Calibration, Thresholds, and Clinical Utility

F-score and PRC area reported; calibration and net benefit not established.

## Reporting and Reproducibility

Feature sets and models are described; local NLP tools would need implementation.

## Care-Pathway and Downstream-Action Bias

Outcome is utilization and reflects care decisions/access.

## Implementation Readiness

Not relevant to dementia deployment.

## Strengths

Large episode sample, PRC metric, structured-only comparator.

## Concerns

Non-dementia label, possible within-episode leakage, no external validation.

## Missing Information

Calibration, temporal note cutoff, external validation.

## Implications for This Literature Review

Use as evidence for additive note value, not cognitive target evidence.

## Recommended Follow-up

Mention endpoint and setting mismatch when citing.
