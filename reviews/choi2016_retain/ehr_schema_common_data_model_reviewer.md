# Specialist Review: EHR Schema and Common Data Model

## Specialist Scope
Assessment of RETAIN's structured visit-sequence representation for this project's data model.

## Bottom Line
Useful representation analogue: RETAIN requires variable-length patient-level visit sequences and coded variables, which supports the need to convert Epic events into temporally ordered encounter features rather than only fixed-length tabular snapshots.

## Data Model and Source System Summary
Large Sutter Health EHR dataset.

## Unit of Analysis and Identifiers
Patient-level sequences of visits and visit-level code sets.

## Encounter and Timeline Representation
Visit order is central. The reverse-time model emphasizes recent visits, aligning with pre-encounter longitudinal history.

## Cohort and Eligibility Implementation
Not directly tied to cardiology encounters.

## Structured Feature Representation
Diagnosis, medication, and procedure codes are represented as visit-level variables inside ordered visit sequences. The model-ready structure is sequence-shaped, not one fixed vector per patient at extraction time.

## Note and Text Metadata Representation
No note metadata.

## Label and Outcome Data Representation
Supervised prediction labels depend on task-specific outcomes; not dementia-specific here.

## Vocabulary, Code Sets, and Mappings
Uses coded EHR concepts, but source-checking is needed before detailed vocabulary claims.

## Missingness, Data Quality, and Provenance
Not the main focus.

## Reproducibility and Portability
A RETAIN-like design requires reproducible visit grouping, code mapping, and pre-index feature windows.

## Fit to Epic-to-Model-Ready Pipeline
Moderate: helps specify a model-ready longitudinal structure, not the Epic extraction itself.

## Strengths
- Clear patient visit-sequence abstraction.
- Interpretable visit and variable attention.

## Concerns
- No common-data-model pipeline.
- Visit definitions may differ across EHRs.

## Missing Information
- Source-level feature coding details are needed before implementation claims.

## Implications for This Literature Review
Use as support for temporally ordered structured baselines and interpretable sequence models.

## Recommended Follow-up
Define how Epic encounters, diagnoses, medications, procedures, and note-derived concepts become visit-level variables.
