# Specialist Review: EHR Schema and Common Data Model

## Specialist Scope

Representation of structured EHR data and notes for multimodal dementia modeling.

## Bottom Line

The work is relevant to model-ready multimodal transformation but does not by itself define an Epic-to-CDM implementation.

## Data Model and Source System Summary

Indiana Network for Patient Care data.

## Unit of Analysis and Identifiers

Patient-level case/control modeling.

## Encounter and Timeline Representation

Observation windows and prediction horizons are explicit; not anchored to cardiology encounters.

## Cohort and Eligibility Implementation

Matched case-control design; exact criteria require source checking.

## Structured Feature Representation

Demographics and diagnoses feed structured models.

## Note and Text Metadata Representation

Medical notes are used, with emphasis on long-note content selection.

## Label and Outcome Data Representation

Dementia case/control labels from EHR phenotype.

## Vocabulary, Code Sets, and Mappings

Structured diagnosis groupings and note tokenization/selection are key mappings.

## Missingness, Data Quality, and Provenance

Health-information exchange data may differ from a single Epic instance.

## Reproducibility and Portability

Architecture is portable; data transformations need local reimplementation.

## Fit to Epic-to-Model-Ready Pipeline

Useful for thinking about structured/text fusion and long notes, not a schema recipe.

## Strengths

Explicit time windows and multimodal feature separation.

## Concerns

No OMOP/FHIR/Epic mapping guidance.

## Missing Information

Exact source domains, note classes, and coding vocabularies.

## Implications for This Literature Review

Our pipeline should expose both structured summary features and note representations with strict pre-index timestamps.

## Recommended Follow-up

Source-check dissertation methods before borrowing window definitions.
