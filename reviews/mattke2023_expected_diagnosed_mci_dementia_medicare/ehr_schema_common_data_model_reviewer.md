# Specialist Review: EHR Schema and Common Data Model

## Specialist Scope

Claims schema and portability assessment.

## Bottom Line

Useful claims operationalization for MCI/dementia detection rates; limited Epic schema detail.

## Data Model and Source System Summary

Medicare claims/encounter and enrollment data plus HRS survey/cognitive data.

## Unit of Analysis and Identifiers

Beneficiary-level rolling-window analysis.

## Encounter and Timeline Representation

Three-year rolling windows and separate-day claim requirements.

## Cohort and Eligibility Implementation

Age, enrollment, death, FFS/MA coverage criteria are implementable.

## Structured Feature Representation

Diagnosis codes and demographic variables.

## Note and Text Metadata Representation

Not applicable.

## Label and Outcome Data Representation

MCI/dementia represented by diagnosis-code claims, with overlap assignment rules.

## Vocabulary, Code Sets, and Mappings

ICD-9/ICD-10 and modified CCW; supplement needed.

## Missingness, Data Quality, and Provenance

Diagnosis absence may mean undocumented, not absent.

## Reproducibility and Portability

Good for claims; Epic implementation would need diagnosis/procedure/order mappings and local validation.

## Fit to Epic-to-Model-Ready Pipeline

Useful for defining outcome-code caveats and follow-up requirements.

## Strengths

Clear observation windows and claims definitions.

## Concerns

No encounter-level decision point; no clinical text.

## Missing Information

Full supplement not locally reviewed.

## Implications for This Literature Review

Do not treat local absence of cognitive codes as negative without follow-up/opportunity criteria.

## Recommended Follow-up

Develop local code lists and a hierarchy for MCI, dementia, medications, testing, and referrals.
