# Specialist Review: EHR Schema and Common Data Model

## Specialist Scope
Assessment of whether the MCI/AD ML review informs EHR data modeling.

## Bottom Line
Low EHR schema relevance because the reviewed studies mostly use ADNI-like imaging, biomarker, genetic, cognitive, and demographic data rather than operational EHR schemas.

## Data Model and Source System Summary
Published studies, mostly ADNI.

## Unit of Analysis and Identifiers
Research participant-level analyses rather than encounter-level EHR records.

## Encounter and Timeline Representation
Not aligned to cardiology encounter-start prediction.

## Cohort and Eligibility Implementation
Research cohort eligibility, not operational EHR cohort construction.

## Structured Feature Representation
Imaging and biomarker features predominate.

## Note and Text Metadata Representation
No note metadata contribution.

## Label and Outcome Data Representation
MCI/AD labels are study-specific and require source checking before comparison with EHR labels.

## Vocabulary, Code Sets, and Mappings
No clinical vocabulary or CDM mapping.

## Missingness, Data Quality, and Provenance
Research-data missingness differs from routine EHR missingness.

## Reproducibility and Portability
Limited for Epic-to-model-ready data transformation.

## Fit to Epic-to-Model-Ready Pipeline
Low.

## Strengths
- Useful contrast with routine-care EHR work.

## Concerns
- May encourage unrealistic data assumptions for cardiology practice.

## Missing Information
- No Epic, OMOP, encounter, note, or claims schema details.

## Implications for This Literature Review
Use to contrast traditional AD ML with routine EHR prediction.

## Recommended Follow-up
Do not source the EHR schema section from this paper.
