# Specialist Review: EHR Schema and Common Data Model

## Specialist Scope
Assessment of BEHRT's structured EHR sequence representation for this project's data model.

## Bottom Line
Important representation analogue: BEHRT shows how diagnoses, medications, measurements, age, and time information can be transformed into variable-length patient sequences for transformer modeling.

## Data Model and Source System Summary
Clinical Practice Research Datalink linked with hospital and administrative datasets in the UK.

## Unit of Analysis and Identifiers
Patient-level longitudinal event sequences.

## Encounter and Timeline Representation
Irregular time intervals and visit/event ordering are central. This supports explicit time encoding before cardiology encounter start.

## Cohort and Eligibility Implementation
Disease-trajectory cohorts, not cardiology encounter cohorts.

## Structured Feature Representation
Structured concepts include diagnoses, medications, measurements, demographics, and time/position embeddings. This is a sequence-token representation with explicit temporal encodings, not a fixed-length engineered-feature table.

## Note and Text Metadata Representation
No note metadata.

## Label and Outcome Data Representation
Task-specific disease prediction labels, not cognitive-care labels.

## Vocabulary, Code Sets, and Mappings
Requires mapping structured EHR concepts into model tokens; source-checking needed for vocabulary details.

## Missingness, Data Quality, and Provenance
Not a primary focus, but irregular observation and missingness are relevant to routine EHR.

## Reproducibility and Portability
Conceptually portable if concept mapping and time windows are well defined.

## Fit to Epic-to-Model-Ready Pipeline
Moderate to high for model-ready longitudinal representation; low for raw Epic extraction.

## Strengths
- Explicit temporal sequence representation.
- Uses routinely collected structured EHR concepts.

## Concerns
- Not encounter-level by default.
- No text-derived concept integration in the summary.

## Missing Information
- Exact concept mappings, time-bin definitions, and implementation details need source checking.

## Implications for This Literature Review
Use as a key longitudinal representation source, with caution that model architecture is secondary to target and label validity.

## Recommended Follow-up
Define local event-token vocabulary and time encodings before considering transformer sequence models.
