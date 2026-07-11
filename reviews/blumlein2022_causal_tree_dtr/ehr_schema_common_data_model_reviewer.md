# Specialist Review: EHR Schema and Common Data Model

## Specialist Scope
Assessment of whether the DTR causal tree/forest paper informs EHR schema and longitudinal data representation.

## Bottom Line
Moderate indirect schema relevance for longitudinal treatment-history representation, but not for Epic-to-OMOP transformation or cardiology encounter data extraction.

## Data Model and Source System Summary
The paper uses synthetic data and a real-world ICU application.

## Unit of Analysis and Identifiers
Sequential patient states and treatment histories are central; exact operational identifiers are not a main contribution.

## Encounter and Timeline Representation
Longitudinal treatment timing matters, but not in the specific pre-cardiology encounter format.

## Cohort and Eligibility Implementation
Not directly applicable to the cardiology cohort.

## Structured Feature Representation
Structured covariates, treatment histories, and outcomes are required.

## Note and Text Metadata Representation
No note representation.

## Label and Outcome Data Representation
Outcomes support policy evaluation rather than dementia-risk labels.

## Vocabulary, Code Sets, and Mappings
No reusable clinical vocabularies or code sets.

## Missingness, Data Quality, and Provenance
Not a schema-quality paper.

## Reproducibility and Portability
Method portability depends on having well-structured longitudinal treatment and outcome data.

## Fit to Epic-to-Model-Ready Pipeline
Low for the first model; may matter later if extracting action histories after cardiology encounters.

## Strengths
- Emphasizes longitudinal state, treatment, and outcome representation.

## Concerns
- Does not address EHR implementation details.

## Missing Information
- No Epic, CDM, timestamp, or vocabulary mapping details.

## Implications for This Literature Review
Use only as later policy-learning background.

## Recommended Follow-up
If action-policy modeling becomes active, define EHR representations for actions, timing, and outcomes before applying DTR methods.
