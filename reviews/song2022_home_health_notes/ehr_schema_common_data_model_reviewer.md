# Specialist Review: EHR Schema and Common Data Model

## Specialist Scope

Home-health structured assessment and clinical-note feature construction.

## Bottom Line

The paper is useful for structured-plus-text feature-set comparison but relies on HHC-specific OASIS/Omaha data structures.

## Data Model and Source System Summary

OASIS, EHR assessment data, and home-health clinical notes.

## Unit of Analysis and Identifiers

Home-health episode.

## Encounter and Timeline Representation

Episode-level prediction; exact pre-outcome note timing should be checked.

## Cohort and Eligibility Implementation

HHC episodes from 2015-2017.

## Structured Feature Representation

OASIS and other structured EHR variables.

## Note and Text Metadata Representation

Approximately 2.3 million clinical notes from nurses, therapists, and social workers.

## Label and Outcome Data Representation

Hospitalization/ED visit from OASIS.

## Vocabulary, Code Sets, and Mappings

Omaha System problems and concerning-note classifier outputs.

## Missingness, Data Quality, and Provenance

Note volume and discipline mix are setting-specific.

## Reproducibility and Portability

Limited outside HHC unless analogous structured assessments and note types exist.

## Fit to Epic-to-Model-Ready Pipeline

Moderate as an example of adding note-derived variables to structured features.

## Strengths

Clear feature-set comparison.

## Concerns

OASIS/Omaha features do not map directly to cardiology.

## Missing Information

Timestamps and exact NLP implementation details.

## Implications for This Literature Review

Structured-plus-note features should be represented as separate domains in model-ready data.

## Recommended Follow-up

Use as a non-dementia schema analogy only.
