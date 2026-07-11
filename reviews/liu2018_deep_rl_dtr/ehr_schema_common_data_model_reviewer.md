# Specialist Review: EHR Schema and Common Data Model

## Specialist Scope
Assessment of deep RL DTR framework for longitudinal data representation.

## Bottom Line
Indirect schema relevance for future policy work: it requires structured patient states, treatment histories, actions, and outcomes, but does not guide Epic extraction.

## Data Model and Source System Summary
Center for International Blood and Marrow Transplant Research registry.

## Unit of Analysis and Identifiers
Longitudinal patient states and treatment histories.

## Encounter and Timeline Representation
Visit/action sequences are central, but not cardiology encounter-specific.

## Cohort and Eligibility Implementation
Registry-specific.

## Structured Feature Representation
Patient clinical states, treatment histories, and high-dimensional treatment options.

## Note and Text Metadata Representation
No notes.

## Label and Outcome Data Representation
Rewards/value functions for treatment policy, not cognitive-risk labels.

## Vocabulary, Code Sets, and Mappings
No reusable EHR vocabularies in the summary.

## Missingness, Data Quality, and Provenance
Not a schema-quality focus.

## Reproducibility and Portability
Method requires a high-quality longitudinal registry-like state/action schema.

## Fit to Epic-to-Model-Ready Pipeline
Low for first model; possible later relevance for action histories.

## Strengths
- Makes action and state representation explicit.

## Concerns
- Registry setting differs from routine EHR cardiology encounters.

## Missing Information
- No Epic/CDM mapping or timestamp rules.

## Implications for This Literature Review
Use only for later dynamic-treatment-regime design.

## Recommended Follow-up
If future policy learning is pursued, define cardiology actions and follow-up outcomes as EHR data elements.
