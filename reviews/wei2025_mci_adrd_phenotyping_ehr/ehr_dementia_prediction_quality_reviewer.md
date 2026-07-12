# Specialist Review: EHR Dementia Prediction Quality

## Specialist Scope

Assessment of Wei et al. as an EHR-based dementia/MCI model.

## Bottom Line

`methodologically_informative`. The paper is high-value for MCI/ADRD phenotyping and note-vs-code evidence, but it is not a dementia risk prediction study and should not be interpreted as prospective pre-encounter risk scoring.

## Prediction Task Clarity

The task is phenotyping/case finding for MCI/ADRD diagnosis, not future prediction.

## Index Date, Observation Window, and Prediction Horizon

No future horizon is defined. Notes are selected around documented medication/ICD evidence for some patients, reinforcing that this is phenotype classification rather than prediction before recognition.

## Data Source and Cohort Definition

MGH and BIDMC outpatients aged 50+ with at least one clinical note. Stratified sampling across MED/ICD groups enriched positives.

## Outcome and Reference Standard

Manual neurologist chart review is the reference standard, stronger than diagnosis codes alone. Lack of inter-rater reliability remains a limitation.

## Comparator or Control Group

Chart-review negatives across MED/ICD strata. This is stronger than no-code controls.

## EHR Text and Structured Data Use

Uses clinical notes, ICD groups, and medications. Notes include office visit, admission, progress, discharge, and correspondence notes from all specialties.

## Missing Data and Feature Availability

All included patients had at least one note; notes under 500 words were removed. The paper does not deeply analyze missingness or care-utilization differences.

## Validation

Nested cross-validation and site experiments are reported. No external non-Boston validation or temporal validation.

## Calibration, Thresholds, and Clinical Utility

Calibration and clinical utility are not reported. The model is framed primarily for research phenotyping.

## Reporting and Reproducibility

Good reporting of ICD and medication groups and public code/data availability. Needs repository source check.

## Care-Pathway and Downstream-Action Bias

The model identifies documented MCI/ADRD. It may miss undocumented impairment and may learn explicit diagnostic documentation. This is acceptable for phenotype extraction but not for estimating true underdiagnosed impairment.

## Implementation Readiness

Promising for research phenotyping after local validation and mapping. Not ready as a cardiology decision support tool.

## Strengths

- Direct MCI/ADRD EHR model.
- Chart-review reference labels.
- Notes outperform ICD-only and medication-only features.
- Simple interpretable model performs best.

## Concerns

- No future-risk design.
- No calibration.
- No subtype/severity labeling.
- Ambiguous cases excluded.

## Missing Information

Inter-rater reliability, temporal validation, demographic subgroup evaluation, and final repository details.

## Implications for This Literature Review

Wei should become a direct anchor for Section 4 label validity and Section 6 EHR text as signal.

## Recommended Follow-up

Use its four MED/ICD strata and chart-review labels as a template for designing local validation.
