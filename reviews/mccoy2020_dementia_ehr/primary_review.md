# Primary Review: mccoy2020_dementia_ehr

## Review Status

primary_review_complete

## Review-Relevant Contribution

Direct evidence that cognitive symptoms documented in discharge notes are associated with future coded dementia diagnosis over long follow-up.

## Publication Status and Evidence Weight

Peer-reviewed journal article with direct dementia and EHR-text relevance. Evidence weight is moderate for the association claim, but lower for this project's intended outpatient cardiology prediction setting because the exposure comes from inpatient discharge notes.

## Fit to Problem Statement

Supports the premise that routine notes contain cognitive signals years before diagnosis. It does not directly match pre-cardiology-encounter outpatient risk scoring.

## Evidence Category

`dementia_prediction`; `unstructured_ehr_text`; `longitudinal_ehr_representation`; `label_definition`; `validation_or_reporting_quality`

## Clinical Target

Future coded dementia diagnosis.

## Data and Cohort Relevance

Large hospitalized adult cohort from two academic medical centers; less representative of outpatient cardiology encounters.

## EHR Text Relevance

High for discharge-note cognitive symptom burden; moderate for outpatient note-feature design.

## Label or Outcome Relevance

Incident dementia diagnosis code is relevant but depends on future documentation and diagnostic opportunity.

## Modeling Relevance

The paper uses an interpretable symptom score and competing-risk survival modeling rather than a complex ML risk score.

## Validation and Utility Signals

The association was similar in a second hospital system and age subgroup, but calibration and clinical utility for risk scoring are not central outputs.

## Bias, Causality, and Downstream Action Issues

Patients with cognitive symptoms in discharge notes may receive more follow-up and diagnostic attention, increasing diagnosis opportunity.

## Portability and Implementation Signals

The term-score approach is implementable, but discharge-note vocabulary may not map cleanly to outpatient cardiology notes.

## Key Extracted Claims

- 267,855 hospitalized patients and 1,251,858 patient-years of follow-up.
- 6,516 new dementia diagnoses.
- Cognitive symptom score HR 1.63 for earlier dementia diagnosis.

## What This Paper Supports

Documented cognitive symptoms in routine EHR text can precede coded dementia diagnosis by years.

## What This Paper Does Not Support

It does not prove that the score detects true undiagnosed dementia independent of future care pathways.

## Default Specialist Reviews Called

All current specialist reviewers are called.

## Additional Specialist Reviews Needed

None.

## Primary Reviewer Notes

Use as direct longitudinal EHR-text evidence with inpatient-setting caveats.
