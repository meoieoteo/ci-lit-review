# Specialist Review: EHR Schema and Common Data Model

## Specialist Scope
Assessment of ADNI structured multimodal data for relevance to routine EHR schema.

## Bottom Line
Limited EHR schema relevance: the paper uses ADNIMERGE data, which is not a routine Epic or CDM extraction environment.

## Data Model and Source System Summary
ADNIMERGE from ADNI phases ADNI1, ADNI2, ADNI3, and ADNI-GO.

## Unit of Analysis and Identifiers
Participant-level ADNI observations, not cardiology encounters.

## Encounter and Timeline Representation
Longitudinal ADNI assessments exist but do not map directly to operational EHR encounter timing.

## Cohort and Eligibility Implementation
ADNI cohort rules are research-study specific.

## Structured Feature Representation
Clinical, cognitive, imaging, genetic, biomarker, and demographic variables are standardized research variables.

## Note and Text Metadata Representation
No note metadata.

## Label and Outcome Data Representation
MCI/AD labels are research-data labels rather than EHR-derived care-process labels.

## Vocabulary, Code Sets, and Mappings
No Epic, ICD, LOINC, OMOP, or local code mapping.

## Missingness, Data Quality, and Provenance
ADNI missingness differs from routine-care missingness.

## Reproducibility and Portability
Reproducible within ADNI but not directly portable to operational EHR.

## Fit to Epic-to-Model-Ready Pipeline
Low.

## Strengths
- Well-structured research data.

## Concerns
- Routine EHR translation is not addressed.

## Missing Information
- No clinical warehouse, timestamp, or code-set implementation.

## Implications for This Literature Review
Use as cognitive-prediction context, not as EHR transformation guidance.

## Recommended Follow-up
Avoid using ADNI schema assumptions for Epic model design.
