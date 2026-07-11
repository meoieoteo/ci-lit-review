# Specialist Review: EHR Schema and Common Data Model

## Specialist Scope
Assessment of preoperative frailty LLM paper for EHR schema and label representation.

## Bottom Line
Useful caution for schema and labels: VES-13 and eFI labels come from different data structures and yield different learned constructs, so label provenance must be explicit.

## Data Model and Source System Summary
Single-institution preoperative anesthesia clinic notes with two spine-surgery datasets.

## Unit of Analysis and Identifiers
Patient/preoperative-note classification, not cardiology encounter risk scoring.

## Encounter and Timeline Representation
Preoperative encounter timing is central; local adaptation would need cardiology encounter-start anchoring.

## Cohort and Eligibility Implementation
Spine-surgery preoperative cohorts, not cardiology cohorts.

## Structured Feature Representation
The eFI label incorporates comorbidities, functional status, labs, and physical exam findings from the EHR.

## Note and Text Metadata Representation
Preoperative anesthesia H&P notes are the text source; note-type transfer to cardiology is uncertain.

## Label and Outcome Data Representation
VES-13 questionnaire and eFI are distinct label sources and constructs.

## Vocabulary, Code Sets, and Mappings
No reusable Epic/OMOP mapping in the summary.

## Missingness, Data Quality, and Provenance
Label provenance is the central data-quality issue.

## Reproducibility and Portability
Single-institution implementation limits portability.

## Fit to Epic-to-Model-Ready Pipeline
Moderate as a warning about label-source provenance; low as a CDM template.

## Strengths
- Directly compares labels from different data-generating processes.

## Concerns
- Note source and label source may be locally specific.
- Direct classifier outputs are hard to audit.

## Missing Information
- Exact eFI construction and note metadata need source checking.

## Implications for This Literature Review
Use to support separating disease-state, questionnaire, and EHR-derived labels in the local data model.

## Recommended Follow-up
Track label source, evidence date, and construct class for every candidate outcome.
