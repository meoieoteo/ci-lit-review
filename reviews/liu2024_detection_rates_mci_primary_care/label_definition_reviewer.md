# Specialist Review: Label Definition

## Specialist Scope

MCI diagnosis label and clinician/practice detection rate assessment.

## Bottom Line

usable_with_caveats. The paper makes the diagnosis-code label weakness explicit.

## Label Summary

Observed MCI is ICD-10-CM G31.84 on two claims on separate days in 2017-2019.

## Target Construct

`future_coded_dementia_diagnosis`; `current_undocumented_cognitive_impairment`; `future_care_pathway`

## Label Source and Operational Definition

Medicare claims/encounter diagnosis codes; expected MCI from HRS CIND model.

## Index Date and Label Timing

Three-year 2017-2019 window.

## Positive Case Definition

Two MCI claims on separate days.

## Negative or Control Definition

No MCI diagnosis among attributed patients; not confirmed absence of MCI.

## Indeterminate or Excluded Cases

Patients with both MCI and dementia claims were assigned using midpoint/latest-claim rules.

## Label Validity Evidence

Expected rate model references HRS cognitive/proxy assessments. Administrative MCI algorithm needs validation.

## Misclassification Risks

Large false-negative risk for MCI claims. Some diagnoses may be communicated but not documented.

## Downstream-Action and Diagnosis-Opportunity Bias

Central. Detection depends on clinician/practice behavior, specialty, documentation, and referral.

## Leakage Risks

Not applicable as a prediction model.

## Fit to Pre-Cardiology Risk Scoring

High as label-bias evidence. Future MCI diagnosis labels should consider PCP attribution and detection opportunity.

## Strengths

Clinician/practice-level analysis and expected-rate inference.

## Concerns

Expected rates are model-derived; MCI code algorithm needs validation.

## Missing Information

Supplemental model details and code validation.

## Implications for This Literature Review

Supports not treating no MCI code as no cognitive impairment.

## Recommended Follow-up

Define PCP contact and primary-care continuity as diagnosis-opportunity variables.
