# Specialist Review: EHR Schema and Common Data Model

## Specialist Scope
Assessment of target-trial emulation concepts for EHR data representation.

## Bottom Line
Strong indirect schema relevance: it reinforces that eligibility, time zero, covariates, outcomes, follow-up, and censoring must be operationally encoded before modeling.

## Data Model and Source System Summary
Narrative discussion of observational clinical research, not a specific EHR system.

## Unit of Analysis and Identifiers
Trial-eligible person-time or treatment episodes, not specifically cardiology encounters.

## Encounter and Timeline Representation
Central contribution is time-zero and follow-up discipline.

## Cohort and Eligibility Implementation
Highly relevant conceptually: eligibility criteria must be computable and aligned to the intended decision point.

## Structured Feature Representation
Covariates, exposure/treatment, and outcomes must be defined before follow-up.

## Note and Text Metadata Representation
No note metadata, but the same timing rules apply to notes.

## Label and Outcome Data Representation
Important for separating baseline covariates from post-index outcomes and downstream care processes.

## Vocabulary, Code Sets, and Mappings
No specific code sets.

## Missingness, Data Quality, and Provenance
Raises the need to define censoring and follow-up but not detailed EHR data quality.

## Reproducibility and Portability
Portable as study-design discipline.

## Fit to Epic-to-Model-Ready Pipeline
Moderate: informs the design specification that the pipeline must implement.

## Strengths
- Clear timing and cohort-design relevance.

## Concerns
- Not an implementation paper.

## Missing Information
- No Epic, OMOP, or SQL representation.

## Implications for This Literature Review
Use to frame the data dictionary around index time, eligibility, pre-index covariates, outcomes, censoring, and follow-up.

## Recommended Follow-up
Translate the chosen target into target-trial-like schema fields before extraction.
