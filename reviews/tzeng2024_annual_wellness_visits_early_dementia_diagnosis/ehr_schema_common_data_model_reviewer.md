# Specialist Review: EHR Schema and Common Data Model

## Specialist Scope

Assessment of claims feature and outcome representation.

## Bottom Line

Useful claims-data operational example for care-contact variables, not a local EHR schema paper.

## Data Model and Source System Summary

Medicare beneficiary, inpatient, outpatient, and carrier claims files.

## Unit of Analysis and Identifiers

Beneficiary-level time-to-event analysis.

## Encounter and Timeline Representation

Index date is first AWV date or matched pseudo-index. Follow-up and censoring are clearly defined.

## Cohort and Eligibility Implementation

Claims-based age, enrollment, prior diagnosis, prior AWV, nursing home, and residency exclusions.

## Structured Feature Representation

AWV, diagnosis codes, comorbidities, utilization, PCP, neurology, psychiatry, and area-level social variables.

## Note and Text Metadata Representation

Not applicable.

## Label and Outcome Data Representation

Diagnosis-code outcome dates from claims.

## Vocabulary, Code Sets, and Mappings

ICD-9/ICD-10, CCW, Elixhauser, E/M and AWV claim codes. Supplement needed for exact lists.

## Missingness, Data Quality, and Provenance

Claims provenance is clear; actual cognitive-assessment content is absent.

## Reproducibility and Portability

Good for Medicare claims. Epic translation would need mappings to visit types, orders, referrals, cognitive assessments, and specialty encounters.

## Fit to Epic-to-Model-Ready Pipeline

Strong for defining diagnosis-opportunity variables, not for text or feature modeling.

## Strengths

Clear index-date logic and care-process exposure.

## Concerns

Claims cannot show what happened clinically inside the AWV.

## Missing Information

Visit content, test orders/results, and referral completion.

## Implications for This Literature Review

Use AWV and specialty visits as examples of care-process variables that shape labels.

## Recommended Follow-up

Add Epic definitions for AWV, cognitive screening, referral/order, specialist visit, and completed test.
