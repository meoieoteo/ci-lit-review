# Specialist Review: EHR Dementia Prediction Quality

## Specialist Scope

ClinicalBERT identification of cognitive impairment evidence in EHR note snippets.

## Bottom Line

Useful NLP feasibility evidence, but not a dementia prediction study in the patient-level risk-score sense.

## Prediction Task Clarity

Snippet-level cognitive impairment evidence classification.

## Index Date, Observation Window, and Prediction Horizon

No patient-level index or future horizon.

## Data Source and Cohort Definition

MGB older adults with APOE data and dementia-keyword-containing notes.

## Outcome and Reference Standard

Human annotation of text snippets for cognitive impairment evidence.

## Comparator or Control Group

No/Neither text snippets, not patient controls.

## EHR Text and Structured Data Use

Clinical note snippets only for modeling; APOE defines cohort context.

## Missing Data and Feature Availability

Keyword and BioBank enrichment limit representativeness.

## Validation

Internal holdout sequence-level validation.

## Calibration, Thresholds, and Clinical Utility

No calibration or clinical utility.

## Reporting and Reproducibility

Short source; limited details.

## Care-Pathway and Downstream-Action Bias

Text snippets are enriched for documented cognitive concern.

## Implementation Readiness

Not ready beyond a candidate NLP component.

## Strengths

Clear ClinicalBERT versus TF-IDF comparison and high holdout metrics.

## Concerns

Lower publication weight, no patient-level risk, no external validation.

## Missing Information

Patient-level aggregation and annotation reliability.

## Implications for This Literature Review

Use only for NLP extraction feasibility.

## Recommended Follow-up

Avoid citing as dementia risk prediction performance.
