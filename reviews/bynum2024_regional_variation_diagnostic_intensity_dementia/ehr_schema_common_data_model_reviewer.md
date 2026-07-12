# Specialist Review: EHR Schema and Common Data Model

## Specialist Scope

Assessment of claims-data representation and portability to an Epic-to-model-ready pipeline.

## Bottom Line

Useful for claims-based outcome representation and regional covariates, but not a detailed EHR schema implementation source.

## Data Model and Source System Summary

Medicare claims files and beneficiary summary data, plus external regional datasets.

## Unit of Analysis and Identifiers

Beneficiary and hospital referral region. Not encounter-level.

## Encounter and Timeline Representation

Calendar-year claims windows are clear; no encounter-start decision point.

## Cohort and Eligibility Implementation

Age, enrollment, fee-for-service, and HRR residency criteria are implementable from claims.

## Structured Feature Representation

Claims diagnosis algorithms and regional engineered covariates.

## Note and Text Metadata Representation

Not applicable.

## Label and Outcome Data Representation

ADRD diagnosis is represented as claims-coded diagnosis; label date is claim-based.

## Vocabulary, Code Sets, and Mappings

ICD-10-CM ADRD algorithm is cited; local details require supplement/cited algorithm review.

## Missingness, Data Quality, and Provenance

Claims data provenance is clear at a high level; clinical truth and documentation completeness remain uncertain.

## Reproducibility and Portability

Reproducible with Medicare data access and supplement details. Portability to Epic requires translating "diagnosis intensity" to local care-opportunity measures.

## Fit to Epic-to-Model-Ready Pipeline

Useful for outcome-bias concepts, not for direct Epic feature engineering.

## Strengths

Clear source population, time window, and geographic unit.

## Concerns

No note metadata, no local EHR mappings, and no encounter-level design.

## Missing Information

Exact algorithm supplement not locally reviewed.

## Implications for This Literature Review

Supports adding diagnosis-opportunity covariates such as geography, specialty access, and utilization context to the data model.

## Recommended Follow-up

Define local analogues of HRR diagnostic intensity: pre/post-index PCP contact, neurology contact, cognitive testing, and follow-up completeness.
