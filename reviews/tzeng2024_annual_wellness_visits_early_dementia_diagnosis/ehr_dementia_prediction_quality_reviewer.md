# Specialist Review: EHR Dementia Prediction Quality

## Specialist Scope

Assessment under EHR dementia prediction quality concerns, although this is not a model-development paper.

## Bottom Line

methodologically_informative. The paper shows a future diagnosis label can be shifted by a care-process event.

## Prediction Task Clarity

No prediction task. Outcome is first MCI/ADRD diagnosis after AWV or matched index date.

## Index Date, Observation Window, and Prediction Horizon

Clear: index in 2018, follow-up through 2022, baseline exclusions from 2015-2017.

## Data Source and Cohort Definition

Texas fee-for-service Medicare claims; cohort flow is clearly reported.

## Outcome and Reference Standard

Claims-coded MCI/ADRD. No chart review or cognitive-test reference standard.

## Comparator or Control Group

Propensity-score-matched non-AWV beneficiaries, not cognitively screened controls.

## EHR Text and Structured Data Use

Structured claims only.

## Missing Data and Feature Availability

Complete-data cohort; missing social/clinical variables are acknowledged.

## Validation

No model validation. Robustness via sensitivity analyses.

## Calibration, Thresholds, and Clinical Utility

Not applicable to risk prediction.

## Reporting and Reproducibility

Good for claims-based reproduction, supplement needed for code details.

## Care-Pathway and Downstream-Action Bias

Central: AWV likely increases cognitive assessment and diagnosis opportunity.

## Implementation Readiness

Provides concrete variables to track: AWV, PCP, neurologist, psychiatric visits.

## Strengths

Large cohort, clear exposure and follow-up, competing-risk design.

## Concerns

Residual confounding and claims-label limitations.

## Missing Information

Whether cognitive assessment occurred during AWVs and how referrals were handled.

## Implications for This Literature Review

Supports Section 5 and outcome-label sensitivity analyses.

## Recommended Follow-up

Use this paper to define post-index diagnosis-opportunity variables in the study-design template.
