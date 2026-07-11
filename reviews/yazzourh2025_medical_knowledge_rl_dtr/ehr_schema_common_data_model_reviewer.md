# Specialist Review: EHR Schema and Common Data Model

## Specialist Scope
Assessment of RL/DTR review for EHR schema implications.

## Bottom Line
Indirect schema relevance for future policy work: RL/DTR requires patient state, history, actions, rewards, and expert knowledge representations, but the review does not supply an EHR pipeline.

## Data Model and Source System Summary
Methodological literature review, not a specific EHR source.

## Unit of Analysis and Identifiers
Patient states, histories, treatments/actions, and rewards.

## Encounter and Timeline Representation
Sequential histories matter, but no cardiology encounter implementation is provided.

## Cohort and Eligibility Implementation
Method-dependent, not specified for this project.

## Structured Feature Representation
Structured states and actions are needed for RL/DTR.

## Note and Text Metadata Representation
No notes.

## Label and Outcome Data Representation
Rewards and long-term outcomes for policy learning.

## Vocabulary, Code Sets, and Mappings
No EHR vocabulary mappings.

## Missingness, Data Quality, and Provenance
No detailed EHR data-quality guidance.

## Reproducibility and Portability
Conceptual policy-learning portability only.

## Fit to Epic-to-Model-Ready Pipeline
Low for the first risk model.

## Strengths
- Highlights expert-knowledge representation.

## Concerns
- No operational EHR extraction detail.

## Missing Information
- No source-system schema or timestamp rules.

## Implications for This Literature Review
Use later if converting cardiology follow-up actions into a policy model.

## Recommended Follow-up
Define EHR action, outcome, and reward fields before using this literature.
