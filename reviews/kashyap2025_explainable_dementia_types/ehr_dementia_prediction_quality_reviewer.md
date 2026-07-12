# Specialist Review: EHR Dementia Prediction Quality

## Specialist Scope

LLM-aided dementia subtype classification from clinical notes.

## Bottom Line

Useful for interpretable concept engineering, but not a dementia risk-prediction study.

## Prediction Task Clarity

The task is dementia type classification.

## Index Date, Observation Window, and Prediction Horizon

No pre-index risk horizon is central.

## Data Source and Cohort Definition

Single-hospital clinical-note data.

## Outcome and Reference Standard

Dementia subtype labels; provenance should be source-checked.

## Comparator or Control Group

Comparators are model baselines, not dementia-free controls.

## EHR Text and Structured Data Use

Clinical notes only, transformed into LLM-aided concept features.

## Missing Data and Feature Availability

Demographic/lifestyle features and temporal information are omitted.

## Validation

Internal evaluation; no external validation.

## Calibration, Thresholds, and Clinical Utility

Not established.

## Reporting and Reproducibility

Code availability helps; LLM versioning and concept-generation details matter.

## Care-Pathway and Downstream-Action Bias

Subtype labels and notes may reflect specialist workup and documentation.

## Implementation Readiness

Not ready for risk scoring; more mature as a feature-engineering concept.

## Strengths

Interpretable concepts and baseline comparison.

## Concerns

Target mismatch, single site, no temporal prediction design.

## Missing Information

External validation and label provenance.

## Implications for This Literature Review

Use for LLM-aided feature engineering, not target evidence.

## Recommended Follow-up

Review concept list before adapting to pre-cardiology needs.
