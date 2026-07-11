# Specialist Review: EHR Schema and Common Data Model

## Specialist Scope
Assessment of source-schema implications for using ClinicalBERT-style models trained on MIMIC notes.

## Bottom Line
Limited schema contribution: the paper is about text representation, not an Epic, OMOP, or encounter-level data-transformation pipeline.

## Data Model and Source System Summary
The source corpus is MIMIC-III clinical notes.

## Unit of Analysis and Identifiers
The model operates on text examples for NLP tasks, not on this project's encounter-level unit.

## Encounter and Timeline Representation
No reusable encounter-start anchoring or lookback-window design is apparent.

## Cohort and Eligibility Implementation
Not applicable for this project's cardiology cohort construction.

## Structured Feature Representation
Structured EHR features are not central.

## Note and Text Metadata Representation
Clinical note provenance matters, but the summary does not provide note-type mapping details relevant to Epic outpatient notes.

## Label and Outcome Data Representation
Downstream benchmark labels are not clinical outcome labels for dementia-risk modeling.

## Vocabulary, Code Sets, and Mappings
No CDM vocabulary mapping contribution.

## Missingness, Data Quality, and Provenance
Data quality issues are mainly corpus-domain issues rather than schema issues.

## Reproducibility and Portability
Portable at the model level, but local note extraction and de-identification must be handled separately.

## Fit to Epic-to-Model-Ready Pipeline
Low direct fit; it can inform the text encoder layer after Epic note extraction is solved.

## Strengths
- Highlights value of domain-specific clinical text pretraining.

## Concerns
- Does not address patient, encounter, timestamp, or feature provenance.

## Missing Information
- No Epic, OMOP, FHIR, or reproducible clinical data warehouse mapping.

## Implications for This Literature Review
Treat as representation background, not data-transformation evidence.

## Recommended Follow-up
Pair with implementation papers that describe note extraction, sectioning, and timestamp handling.
