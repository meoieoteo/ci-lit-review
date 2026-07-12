# Primary Review: tzeng2024_annual_wellness_visits_early_dementia_diagnosis

## Review Status

primary_review_complete

## Review-Relevant Contribution

This paper provides direct evidence that a care-process exposure, Medicare annual wellness visit receipt, is associated with subsequent first MCI diagnosis.

## Publication Status and Evidence Weight

Peer-reviewed journal article. High relevance to Section 5. Evidence weight is moderate-to-high for AWV as a diagnosis-opportunity signal, but not causal proof because AWV receipt is observational and self-selected.

## Fit to Problem Statement

Strong fit for the problem statement's concern that diagnostic workup and care contact can create labels. Not cardiology-specific and not a prediction-model study.

## Evidence Category

`downstream_action_bias`; `label_definition`; `clinical_decision_support`; `background_or_context`

## Clinical Target

First coded MCI or ADRD diagnosis after index.

## Data and Cohort Relevance

Texas fee-for-service Medicare cohort of older adults without prior MCI/ADRD or prior AWV. Useful for U.S. claims-based diagnosis-opportunity evidence.

## EHR Text Relevance

None.

## Label or Outcome Relevance

High. First MCI/ADRD diagnosis is explicitly tied to a care-process exposure.

## Modeling Relevance

Indirect. AWV, PCP contact, neurologist visit, psychiatrist visit, and hospitalizations are examples of variables that can act as diagnosis-opportunity measures.

## Validation and Utility Signals

Uses propensity score matching, competing-risk models, death as competing risk, and sensitivity analyses. No chart validation of MCI/ADRD labels.

## Bias, Causality, and Downstream Action Issues

Central. AWV receipt may both increase cognitive assessment opportunity and reflect patient/caregiver selection or healthcare engagement.

## Portability and Implementation Signals

Claims-based AWV and diagnosis codes are implementable. Local Epic analogues include wellness visits, PCP visits, cognitive assessment, and specialty visits.

## Key Extracted Claims

- Incident AWV in 2018 was associated with first MCI diagnosis (HR 1.21, 95% CI 1.16-1.27).
- Association with ADRD diagnosis was smaller (HR 1.04, 95% CI 1.02-1.06) and not robust in one sensitivity analysis.
- PCP, neurologist, and psychiatrist contact were associated with diagnosis patterns.

## What This Paper Supports

- Care contact can affect whether cognitive impairment becomes coded.
- AWV is a concrete diagnosis-opportunity event.
- Future MCI diagnosis can be partly a function of surveillance intensity.

## What This Paper Does Not Support

- It does not prove AWVs cause cognitive impairment.
- It does not validate claims-coded MCI/ADRD against cognitive testing.
- It does not establish cardiology-specific workflows.

## Default Specialist Reviews Called

All five default specialist reviewers.

## Additional Specialist Reviews Needed

None.

## Primary Reviewer Notes

This is likely a core Section 5 paper alongside Bynum.
