# Specialist Review: EHR Schema and Common Data Model

## Specialist Scope

Operational representation of notes, cognitive assessments, and patient-level concept features.

## Bottom Line

The paper provides useful high-level timing and note-source information, but not enough schema detail for direct Epic-to-model-ready implementation.

## Data Model and Source System Summary

Epic Clarity notes from Kaiser Permanente Washington.

## Unit of Analysis and Identifiers

Patient-level modeling tied to cognitive assessment dates.

## Encounter and Timeline Representation

Clinical note timing relative to assessments is central but not sufficient for a cardiology encounter index.

## Cohort and Eligibility Implementation

Exclusions are translatable in principle, but require local diagnosis/medication code lists.

## Structured Feature Representation

Demographics and cognitive assessment scores are used; structured EHR predictors are limited.

## Note and Text Metadata Representation

Clinic notes are used, but note types, author roles, sections, and signing timestamps are not enough for local replication.

## Label and Outcome Data Representation

Assessment scores and thresholds define labels.

## Vocabulary, Code Sets, and Mappings

The 42 concepts are the key reusable vocabulary.

## Missingness, Data Quality, and Provenance

Selective testing and note availability are important data-quality issues.

## Reproducibility and Portability

Moderate for concepts; limited for schema implementation.

## Fit to Epic-to-Model-Ready Pipeline

Useful for concept-feature design, not a full pipeline precedent.

## Strengths

Named Epic source and interpretable concepts.

## Concerns

Insufficient note metadata and CDM mapping detail.

## Missing Information

Source tables, note classes, timestamps, section handling.

## Implications for This Literature Review

Schema work should explicitly define note provenance and assessment-label timing.

## Recommended Follow-up

Use the concept inventory, not the extraction pipeline, as the reusable element.
