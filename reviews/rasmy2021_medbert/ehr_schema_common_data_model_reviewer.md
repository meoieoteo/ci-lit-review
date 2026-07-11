# Specialist Review: EHR Schema and Common Data Model

## Specialist Scope
Assessment of Med-BERT's structured EHR representation for model-ready data.

## Bottom Line
Useful structured EHR representation source: Med-BERT demonstrates BERT-style pretraining over variable-length diagnosis-code visit sequences, but it does not solve Epic extraction, note integration, irregular-time representation, or encounter-level indexing.

## Data Model and Source System Summary
Large structured EHR datasets from two EHR databases.

## Unit of Analysis and Identifiers
Patient-level visit sequences.

## Encounter and Timeline Representation
Visit sequence structure is central; local adaptation requires mapping encounters and pre-index cutoffs.

## Cohort and Eligibility Implementation
Downstream disease-prediction cohorts, not cardiology-specific.

## Structured Feature Representation
Diagnosis-code sequences are the primary input. The representation is sequence-shaped, not a fixed-length engineered-feature vector.

## Note and Text Metadata Representation
No notes.

## Label and Outcome Data Representation
Task-specific disease labels.

## Vocabulary, Code Sets, and Mappings
Requires diagnosis-code vocabulary construction; source-checking needed for exact mapping and tokenization.

## Missingness, Data Quality, and Provenance
Diagnosis-code absence is not necessarily disease absence, which matters for cognitive targets.

## Reproducibility and Portability
Model approach is portable if vocabularies, visit grouping, and time windows are specified.

## Fit to Epic-to-Model-Ready Pipeline
Moderate for model-ready structured sequences; low for raw extraction and CDM conversion.

## Strengths
- Structured EHR sequence pretraining.
- Relevant baselines for longitudinal representation.

## Concerns
- May encode coding and utilization patterns.
- No note-derived cognitive concepts.

## Missing Information
- Exact code grouping and sequence construction details need source checks.

## Implications for This Literature Review
Use as a structured representation anchor and as a reason to compare against simpler baselines.

## Recommended Follow-up
Define whether local model inputs are visit-level codes, time-binned events, or encounter-anchored histories.
