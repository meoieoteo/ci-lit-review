# Specialist Review: EHR Dementia Prediction Quality

## Specialist Scope

Assessment against EHR dementia-prediction quality concerns.

## Bottom Line

methodologically_informative. The paper directly addresses underdiagnosis and weak labels but remains limited by single-system validation, care-pathway labels, and incomplete clinical utility evidence.

## Prediction Task Clarity

Adequate. The task is detection of probable dementia in patients without dementia codes, not generic dementia prediction.

## Index Date, Observation Window, and Prediction Horizon

Partial. The three-year pre-index window is clear, but the task is case finding rather than future prediction. Controls use a random visit index date.

## Data Source and Cohort Definition

Adequate for the study. Data are VHA/VINCI EHR data from VA Puget Sound. Applicability beyond older mostly male Veterans is limited.

## Outcome and Reference Standard

Partial. Specialty ICD-coded dementia is used as a silver standard for development; chart review is used for validation among controls. Neither is a perfect disease-state reference.

## Comparator or Control Group

Controls are explicitly imperfect uncoded patients. This is acceptable for the study goal but would be weak if interpreted as confirmed non-dementia.

## EHR Text and Structured Data Use

Adequate. The paper uses both note-topic features and structured EHR features.

## Missing Data and Feature Availability

Partial. Sufficient visit/note requirements are reported, but detailed missingness and feature availability are not deeply assessed.

## Validation

Partial. Manual review is a strength; external and temporal validation are absent.

## Calibration, Thresholds, and Clinical Utility

Thresholds are reported, but calibration and clinical utility are underdeveloped.

## Reporting and Reproducibility

Partial. Major design elements are reported, but exact code sets, topics, coefficients, and implementation details are incomplete.

## Care-Pathway and Downstream-Action Bias

Important concern. The model may learn signals of evaluation and documentation opportunity as well as cognitive impairment.

## Implementation Readiness

Not clinically ready without local validation, threshold planning, and workflow design.

## Strengths

- Directly targets undiagnosed dementia.
- Uses structured plus unstructured EHR data.
- Includes chart-review validation.

## Concerns

- Single VHA setting.
- Specialty-coded development positives.
- No external validation or net-benefit analysis.

## Missing Information

- Full feature/code/topic definitions.
- Calibration.
- Subgroup performance.

## Implications for This Literature Review

This paper is a key candidate for Section 8's structured-plus-note-derived-feature rung and Section 4/5 label caveats.

## Recommended Follow-up

Use in the modeling ladder as a fixed-feature structured-plus-text comparator.
