# Specialist Review: EHR Dementia Prediction Quality

## Specialist Scope

Assessment under EHR dementia prediction concerns, although this is not a prediction model paper.

## Bottom Line

methodologically_informative. The paper is not a dementia prediction model, but it directly strengthens the critique that future coded ADRD diagnosis is a care-pathway-sensitive label.

## Prediction Task Clarity

Not a prediction task. The target is new claims-coded ADRD diagnosis in 2019.

## Index Date, Observation Window, and Prediction Horizon

Clear calendar design: 2018 lookback, 2019 new diagnosis.

## Data Source and Cohort Definition

Medicare fee-for-service claims, age 66+, HRR geography. Cohort construction is clear.

## Outcome and Reference Standard

Claims-coded ADRD using a validated algorithm, not clinical adjudication.

## Comparator or Control Group

No disease-free control group. Non-diagnosed beneficiaries should not be interpreted as dementia-free.

## EHR Text and Structured Data Use

Structured claims only.

## Missing Data and Feature Availability

Regional covariates are available at HRR/county level; unmeasured clinical factors remain.

## Validation

No model validation. The algorithm is cited as validated.

## Calibration, Thresholds, and Clinical Utility

Not applicable to risk-score performance.

## Reporting and Reproducibility

Good overall reporting; supplement source-check needed for exact implementation.

## Care-Pathway and Downstream-Action Bias

Central. The paper operationalizes diagnostic intensity and shows large geographic/subgroup variation.

## Implementation Readiness

Useful for analysis design, not as a deployable clinical model.

## Strengths

Large national claims sample, direct label-observability framing, subgroup analysis.

## Concerns

Observed-to-expected rates are not true under/overdiagnosis rates without a gold standard.

## Missing Information

Supplement details and local applicability to non-Medicare populations.

## Implications for This Literature Review

Anchor paper for Section 5.

## Recommended Follow-up

Use in state update after consolidation as direct evidence for diagnosis opportunity.
