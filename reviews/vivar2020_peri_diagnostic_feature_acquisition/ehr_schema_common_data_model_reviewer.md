# Specialist Review: EHR Schema and Common Data Model

## Specialist Scope
Assessment of peri-diagnostic feature acquisition for EHR schema implications.

## Bottom Line
Indirect schema relevance: it would require explicit representation of observed and missing features plus acquisition costs, but it does not provide an EHR schema.

## Data Model and Source System Summary
Two public medical datasets and two synthetic datasets.

## Unit of Analysis and Identifiers
Feature vectors, not encounter-level EHR records.

## Encounter and Timeline Representation
No cardiology encounter timeline.

## Cohort and Eligibility Implementation
Dataset-specific.

## Structured Feature Representation
Partially observed structured features and feature costs.

## Note and Text Metadata Representation
No notes.

## Label and Outcome Data Representation
Benchmark classification labels.

## Vocabulary, Code Sets, and Mappings
None.

## Missingness, Data Quality, and Provenance
Missingness is operationally important but simplified relative to EHR.

## Reproducibility and Portability
No Epic/CDM guidance.

## Fit to Epic-to-Model-Ready Pipeline
Low for first model; possible later use in action-policy feature metadata.

## Strengths
- Treats missing feature acquisition explicitly.

## Concerns
- Not an EHR data-transformation paper.

## Missing Information
- No clinical code sets or timestamps.

## Implications for This Literature Review
Use only for future feature-acquisition policy.

## Recommended Follow-up
Define available, missing, and acquirable data elements before applying this class of method.
