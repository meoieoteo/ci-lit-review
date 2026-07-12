# Specialist Review: EHR Dementia Prediction Quality

## Specialist Scope

Discharge-note cognitive symptom score associated with future coded dementia.

## Bottom Line

Strong large-cohort evidence that note-documented cognitive symptoms precede coded dementia diagnosis, but not a complete risk-score validation.

## Prediction Task Clarity

The paper evaluates time to future coded dementia diagnosis after hospitalization.

## Index Date, Observation Window, and Prediction Horizon

Index is inpatient discharge; follow-up extends up to eight years.

## Data Source and Cohort Definition

Two academic medical-center EHRs; hospitalized adults without prior/current dementia code.

## Outcome and Reference Standard

Incident dementia diagnosis code, not adjudicated dementia.

## Comparator or Control Group

Patients without dementia code during follow-up/censoring.

## EHR Text and Structured Data Use

Cognitive symptom score from discharge notes plus structured covariates.

## Missing Data and Feature Availability

Only hospitalized patients with discharge notes are represented.

## Validation

Large cohort and second-system/subgroup support; not a prediction model validation with calibration.

## Calibration, Thresholds, and Clinical Utility

Not reported for clinical decision support.

## Reporting and Reproducibility

Term-score approach is simpler than black-box text models but term lists and preprocessing matter.

## Care-Pathway and Downstream-Action Bias

Diagnosis after discharge can be driven by follow-up intensity and clinician concern.

## Implementation Readiness

Not ready as an outpatient cardiology score.

## Strengths

Large sample, long follow-up, competing-risk modeling.

## Concerns

Inpatient setting, coded outcome, no calibration/thresholds.

## Missing Information

Prediction performance and utility as a deployed score.

## Implications for This Literature Review

Use as direct longitudinal EHR-text signal evidence, not a model-readiness citation.

## Recommended Follow-up

Keep association language distinct from prediction-performance language.
