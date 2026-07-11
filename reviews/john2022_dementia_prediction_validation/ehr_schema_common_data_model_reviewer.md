# Specialist Review: EHR Schema and Common Data Model

## Specialist Scope
Assessment of OMOP/OHDSI external validation for EHR schema and reproducibility.

## Bottom Line
Strong schema and reproducibility anchor: the paper shows why dementia prediction models need implementable feature definitions and demonstrates external validation in OMOP-mapped observational health data.

## Data Model and Source System Summary
Observational health databases mapped to the OMOP common data model.

## Unit of Analysis and Identifiers
Patient-level prediction models, not cardiology encounter-level scoring.

## Encounter and Timeline Representation
Observation windows and time-to-event horizons are central to external validation; details should be source-checked.

## Cohort and Eligibility Implementation
The paper reviewed whether published models reported enough information to recreate cohorts and predictors.

## Structured Feature Representation
Demographics, diagnosis codes, medication data, and other structured predictors depending on model. The validated models primarily use fixed-length engineered predictor sets from structured OMOP data, not variable-length EHR sequence inputs.

## Note and Text Metadata Representation
No major note-text contribution.

## Label and Outcome Data Representation
Dementia outcomes are operationalized in observational data and should be examined for code definitions and timing.

## Vocabulary, Code Sets, and Mappings
OMOP/OHDSI infrastructure is directly relevant to portable concept sets and patient-level prediction.

## Missingness, Data Quality, and Provenance
The paper highlights reporting gaps that block validation and reuse.

## Reproducibility and Portability
Core contribution: many published models lacked enough detail for external validation.

## Fit to Epic-to-Model-Ready Pipeline
High for the OMOP/reproducibility argument; moderate for this project's encounter-level design.

## Strengths
- Direct CDM relevance.
- External validation focus.
- Dementia prediction domain.

## Concerns
- Patient-level rather than cardiology encounter-level.
- Structured-data emphasis.

## Missing Information
- Source-check exact OMOP cohort definitions and validated model specifications before citing in detail.

## Implications for This Literature Review
Use as a central source for reproducible EHR data transformation and external validation requirements.

## Recommended Follow-up
Source-check the OMOP implementation details and reporting criteria before drafting the data-transformation section.
