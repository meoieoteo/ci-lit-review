# Specialist Review: EHR Schema and Common Data Model

## Specialist Scope

Claims schema, attribution, and feature representation.

## Bottom Line

Useful for provider/practice attribution and MCI claims outcome representation.

## Data Model and Source System Summary

Medicare enrollment, claims, and encounter data.

## Unit of Analysis and Identifiers

Primary care clinician and practice panels, with beneficiaries attributed by plurality of office visits.

## Encounter and Timeline Representation

Three-year window; office visits used for attribution.

## Cohort and Eligibility Implementation

Age, enrollment, office visits, clinician NPI, practice TIN, and panel-size criteria.

## Structured Feature Representation

Diagnosis codes, E/M visits, clinician specialty, NPI/TIN.

## Note and Text Metadata Representation

Not applicable.

## Label and Outcome Data Representation

MCI claims diagnosis; overlap assignment with dementia.

## Vocabulary, Code Sets, and Mappings

ICD-10 G31.84, office visit E/M codes, CCW-style structure.

## Missingness, Data Quality, and Provenance

Clinician attribution is inferred and may not equal true primary clinician.

## Reproducibility and Portability

Good for claims; Epic requires provider/department attribution rules.

## Fit to Epic-to-Model-Ready Pipeline

Useful for defining PCP continuity and provider specialty features.

## Strengths

Clear attribution strategy.

## Concerns

TIN/NPI attribution does not translate directly to Epic departments or care teams.

## Missing Information

Exact E/M code list and supplement details.

## Implications for This Literature Review

Provider/practice context should be considered in outcome observability.

## Recommended Follow-up

Design local attribution variables: PCP on file, recent PCP visit, primary care department, and specialist contact.
