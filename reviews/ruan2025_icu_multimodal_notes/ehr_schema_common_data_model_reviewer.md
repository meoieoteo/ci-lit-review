# Specialist Review: EHR Schema and Common Data Model

## Specialist Scope

MIMIC ICU structured features and note types for multimodal evidence fusion.

## Bottom Line

Useful for documenting multimodal input domains and note-type restrictions, but not portable to outpatient cardiology without redesign.

## Data Model and Source System Summary

MIMIC-III ICU data.

## Unit of Analysis and Identifiers

ICU stay.

## Encounter and Timeline Representation

First 24 hours after ICU admission.

## Cohort and Eligibility Implementation

ICU stays with required structured and note inputs.

## Structured Feature Representation

Demographics, labs, selected vitals, treatments, and comorbidities.

## Note and Text Metadata Representation

Nursing, Nursing/Other, Physician, and Radiology notes; 512-token inputs.

## Label and Outcome Data Representation

Mortality and PLOS outcomes.

## Vocabulary, Code Sets, and Mappings

Not dementia-relevant.

## Missingness, Data Quality, and Provenance

Feature selection depends on missingness thresholds.

## Reproducibility and Portability

MIMIC improves reproducibility; ICU workflow limits portability.

## Fit to Epic-to-Model-Ready Pipeline

Low for cardiology, moderate for documenting modality-level provenance.

## Strengths

Explicit note types and structured domains.

## Concerns

No outpatient encounter model or CDM mapping.

## Missing Information

Detailed local code mappings and note timing edge cases.

## Implications for This Literature Review

Report modality provenance and missingness rules explicitly.

## Recommended Follow-up

Use as reliability/multimodal methods context.
