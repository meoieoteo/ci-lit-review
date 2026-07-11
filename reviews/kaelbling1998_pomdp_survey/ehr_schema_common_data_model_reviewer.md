# Specialist Review: EHR Schema and Common Data Model

## Specialist Scope
Assessment of POMDP framing for EHR schema implications.

## Bottom Line
Indirect schema relevance only: POMDPs require states, observations, actions, and rewards, but the paper does not specify how to represent those in EHR data.

## Data Model and Source System Summary
No clinical data source.

## Unit of Analysis and Identifiers
States, actions, observations, and beliefs rather than EHR identifiers.

## Encounter and Timeline Representation
Sequential decision time is central, but not operationalized as EHR timestamps.

## Cohort and Eligibility Implementation
Not applicable.

## Structured Feature Representation
Abstract state and observation variables.

## Note and Text Metadata Representation
No notes.

## Label and Outcome Data Representation
Rewards and outcomes are abstract.

## Vocabulary, Code Sets, and Mappings
None.

## Missingness, Data Quality, and Provenance
Partial observability is conceptually relevant to missing clinical state.

## Reproducibility and Portability
No EHR transformation details.

## Fit to Epic-to-Model-Ready Pipeline
Low for the first pipeline.

## Strengths
- Useful conceptual language for hidden cognitive state.

## Concerns
- No operational schema guidance.

## Missing Information
- No EHR representation.

## Implications for This Literature Review
Use for later sequential diagnosis, not CDM translation.

## Recommended Follow-up
Define EHR action and observation schemas before any POMDP work.
