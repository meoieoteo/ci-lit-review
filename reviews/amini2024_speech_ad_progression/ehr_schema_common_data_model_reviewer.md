# Specialist Review: EHR Schema and Common Data Model

## Specialist Scope
Assessment of whether the speech-based Alzheimer progression study informs EHR schema or CDM implementation.

## Bottom Line
Minimal direct schema relevance: the data source is a cohort study with speech recordings and neuropsychological data, not operational EHR extraction.

## Data Model and Source System Summary
Framingham Heart Study recordings and participant data are used.

## Unit of Analysis and Identifiers
Participant-level prediction rather than cardiology encounter-level prediction.

## Encounter and Timeline Representation
Assessment timing exists but does not map to EHR encounter-start anchoring.

## Cohort and Eligibility Implementation
Cohort construction is study-specific rather than EHR-schema driven.

## Structured Feature Representation
Structured predictors include demographics, genetics, health factors, cognitive tests, and MMSE in some feature sets.

## Note and Text Metadata Representation
No clinical note metadata.

## Label and Outcome Data Representation
Labels are tied to study follow-up and cognitive outcomes, not EHR diagnosis opportunity.

## Vocabulary, Code Sets, and Mappings
No code-set or CDM mapping contribution.

## Missingness, Data Quality, and Provenance
Speech-processing quality matters, but operational EHR missingness is not addressed.

## Reproducibility and Portability
Portability to Epic-to-model-ready pipelines is low.

## Fit to Epic-to-Model-Ready Pipeline
Low fit.

## Strengths
- Clear multimodal feature framing in a cognitive domain.

## Concerns
- Does not address encounters, EHR timestamps, notes, or code vocabularies.

## Missing Information
- No EHR extraction details.

## Implications for This Literature Review
Do not cite for EHR schema or CDM transformation.

## Recommended Follow-up
Use only for language/cognitive-signal background if source-checked.
