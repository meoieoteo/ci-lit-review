# Specialist Review: EHR Schema and Common Data Model

## Specialist Scope

Data representation for note-based dementia subtype classification.

## Bottom Line

The paper is method-focused and provides limited reusable EHR schema guidance.

## Data Model and Source System Summary

Single-hospital clinical-note dataset.

## Unit of Analysis and Identifiers

Patient/note classification for dementia subtype.

## Encounter and Timeline Representation

Temporal structure is not central.

## Cohort and Eligibility Implementation

Dementia-type cohort details require source checking.

## Structured Feature Representation

Structured EHR features are not central.

## Note and Text Metadata Representation

Clinical notes are used, but note classes and timestamps are not the primary contribution.

## Label and Outcome Data Representation

Dementia subtype labels.

## Vocabulary, Code Sets, and Mappings

254 LLM-derived concepts are the key vocabulary artifact.

## Missingness, Data Quality, and Provenance

Single-site note and label provenance limit transport.

## Reproducibility and Portability

Concepts and code may help; local note mappings remain required.

## Fit to Epic-to-Model-Ready Pipeline

Useful for concept-vector layer, not extraction pipeline.

## Strengths

Interpretable concept representation.

## Concerns

No CDM mapping or timing model.

## Missing Information

Source EHR schema, note metadata, subtype-label provenance.

## Implications for This Literature Review

LLM-derived concept lists still need schema-aware feature availability.

## Recommended Follow-up

If adopting concept features, map them to local notes and timestamps.
