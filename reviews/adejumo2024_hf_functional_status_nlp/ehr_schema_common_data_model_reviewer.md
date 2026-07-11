# Specialist Review: EHR Schema and Common Data Model

## Specialist Scope
Assessment of the paper's EHR source, note metadata, structured cohort extraction, and portability to an Epic-to-model-ready pipeline.

## Bottom Line
Useful Epic implementation analogue: the study used Epic Clarity, structured EHR cohort identification, outpatient cardiology note metadata, and sectioned text, but it does not provide a common-data-model strategy.

## Data Model and Source System Summary
Yale New Haven Health System EHR data were extracted from Epic Clarity.

## Unit of Analysis and Identifiers
The NLP unit is the outpatient note/encounter; the cohort is patient-level heart failure with outpatient cardiovascular encounters.

## Encounter and Timeline Representation
The paper reports a broad 2013-2022 source window. A local risk-score implementation would need stricter encounter-start anchoring.

## Cohort and Eligibility Implementation
Heart-failure cohort identification used structured EHR elements such as diagnosis codes and encounter information.

## Structured Feature Representation
Structured fields support cohort construction, but the main extracted features are note-derived functional-status labels.

## Note and Text Metadata Representation
Note type, sectioning, and outpatient cardiovascular context are central strengths. Sectioning focused on HPI and assessment/plan.

## Label and Outcome Data Representation
Labels are expert annotations of note evidence, not patient outcomes. This is appropriate for concept extraction but not sufficient for dementia-risk labels.

## Vocabulary, Code Sets, and Mappings
The summary does not expose full code lists or a reusable vocabulary mapping.

## Missingness, Data Quality, and Provenance
The paper directly addresses undercapture of NYHA status in explicit documentation, which is a useful data-quality lesson.

## Reproducibility and Portability
Reproducibility depends on access to annotation details, note-sectioning rules, and local Epic document metadata.

## Fit to Epic-to-Model-Ready Pipeline
High fit for Epic note extraction and sectioning; low fit for OMOP/CDM translation.

## Strengths
- Epic Clarity source.
- Outpatient cardiology notes.
- Note sectioning.
- Structured cohort plus unstructured note pipeline.

## Concerns
- Local note templates and documentation habits may drive performance.
- Common data model mapping is not addressed.

## Missing Information
- Complete code sets, note-type mappings, and extraction SQL are not captured in the summary.

## Implications for This Literature Review
Use as a concrete implementation analogue for Epic cardiology-note extraction, not as a portable CDM model.

## Recommended Follow-up
Source-check supplemental details for note metadata, sections removed, cohort codes, and Epic extraction assumptions.
