# Specialist Review: EHR Dementia Prediction Quality

## Specialist Scope

One-year-ahead dementia prediction from medical notes.

## Bottom Line

This is directly relevant dementia-note prediction evidence, with the key lesson that note-derived models can lose performance when transported across institutions.

## Prediction Task Clarity

The task is one-year-ahead incident dementia prediction.

## Index Date, Observation Window, and Prediction Horizon

Three-year note lookback with the year immediately before index excluded.

## Data Source and Cohort Definition

Multi-institution note data with one development institution and two external institutions.

## Outcome and Reference Standard

Incident dementia case/control label; exact EHR phenotype needs source checking.

## Comparator or Control Group

Matched controls excluding prior dementia/MCI.

## EHR Text and Structured Data Use

Clinical notes are transformed into keywords, embeddings, and UMLS concept exposure features.

## Missing Data and Feature Availability

Note availability and institution-specific documentation likely affect features.

## Validation

Internal held-out and external institution evaluation are reported.

## Calibration, Thresholds, and Clinical Utility

Discrimination is reported; calibration and utility thresholds are not established.

## Reporting and Reproducibility

Feature-engineering steps are described at a high level; exact implementation should be checked.

## Care-Pathway and Downstream-Action Bias

Dementia diagnosis is affected by differential workup and documentation.

## Implementation Readiness

Not ready without local validation and recalibration.

## Strengths

Explicit horizon, note-only feature engineering, external institution tests.

## Concerns

External performance degradation and code-derived diagnosis concerns.

## Missing Information

Calibration, threshold performance, and full phenotype details.

## Implications for This Literature Review

Use as direct evidence for note signal and direct caution about transportability.

## Recommended Follow-up

Carry external-performance drop into synthesis.
