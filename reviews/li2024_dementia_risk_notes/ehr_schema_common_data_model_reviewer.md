# Specialist Review: EHR Schema and Common Data Model

## Specialist Scope

Assessment of EHR data-source reporting, timeline representation, note provenance, label representation, and portability for Li et al.

## Bottom Line

The paper is useful for thinking about text-to-model transformations, especially chronological note aggregation and sentence selection, but it does not provide enough EHR schema detail to directly implement the cohort, labels, or note extraction in Epic or a common data model.

## Data Model and Source System Summary

The source is INPC through the Regenstrief Data Core, described as a centralized community-wide electronic medical record spanning hospitals, health systems, public health, laboratories, radiology centers, and physician practices. No formal common data model such as OMOP, PCORnet, i2b2, or FHIR is specified.

## Unit of Analysis and Identifiers

The unit of analysis is patient-level risk prediction. Each patient has a document composed of notes from the observation period. The paper does not describe encounter IDs, note IDs, provider IDs, department IDs, site IDs, or repeated encounters in detail.

## Encounter and Timeline Representation

The paper defines one- and two-year observation periods and six-month and one-year prediction horizons. Notes are ordered chronologically from oldest to newest. It does not specify encounter start/end timestamps, note creation/signing times, diagnosis entry dates, or whether notes are linked to outpatient, inpatient, emergency, or specialty encounters.

## Cohort and Eligibility Implementation

Eligibility is reported at a conceptual level: incident dementia cases, exclusion of MCI or previous dementia, and controls with no dementia or MCI diagnosis matched by sex, race, and age. The main text does not provide code sets, SQL, source-table logic, or follow-up requirements.

## Structured Feature Representation

Although INPC contains structured data, the model uses notes only. Structured EHR features are discussed as background and future work, not as inputs for the evaluated model.

## Note and Text Metadata Representation

The paper says "medical notes" and "health providers' notes" but does not provide a note-type inventory, author specialty list, section metadata, document class, encounter link, signing time, or copied-forward text handling. Text preprocessing includes replacing numerals with spaces, removing formatting tags and report titles, NLTK sentence tokenization, and duplicate sentence removal.

## Label and Outcome Data Representation

Labels are represented as patient-level incident dementia case status and no dementia/MCI control status. Label provenance is not detailed enough to distinguish diagnosis-code source, problem-list source, encounter setting, provider specialty, or clinical event date.

## Vocabulary, Code Sets, and Mappings

No dementia or MCI code sets are reported in the main text. The paper references prior work with UMLS mapping but does not use UMLS concept features in the evaluated model.

## Missingness, Data Quality, and Provenance

The paper notes that older EHR records may not be available for all patients and motivates one- or two-year observation windows. It does not quantify missing notes, sparse utilization, copied-forward text, duplicate notes beyond duplicate sentence removal, or source-system heterogeneity.

## Reproducibility and Portability

Algorithmic reproducibility is stronger than data reproducibility. The content-selection method is described in detail and code is reported as available, but another site would still need to reconstruct labels, note extraction, and temporal joins without enough operational detail from the article alone.

## Fit to Epic-to-Model-Ready Pipeline

The paper supports the need for an Epic pipeline that creates patient-level chronological note documents before an index time and then applies sentence-level preprocessing. It does not directly specify an Epic-to-OMOP or Epic-to-model-ready implementation.

## Strengths

- Clear patient-level document construction from notes over defined observation windows.
- Chronological ordering of notes is explicitly preserved.
- Preprocessing steps are described at a useful high level.
- The long-text constraint is quantified.

## Concerns

- No common data model or source-table mapping.
- No note metadata sufficient for pre-cardiology encounter anchoring.
- No code sets for labels.
- No provenance fields for diagnosis source or note source.
- No site-level or source-system heterogeneity reporting.

## Missing Information

- Note type, author specialty, encounter type, note date, and signing date.
- Diagnosis-code/provenance logic for dementia and MCI.
- Eligibility and matching implementation details.
- Handling of patients with sparse prior notes.
- Whether same-day or near-index notes could include diagnostic workup.

## Implications for This Literature Review

Use this paper as a modeling and long-note transformation source, not as a schema implementation template. It reinforces that our local pipeline must preserve note provenance and timestamps more explicitly than many modeling papers report.

## Recommended Follow-up

For local adaptation, create a data dictionary that separates patient ID, encounter ID, note ID, note timestamp, note type, author discipline, diagnosis-code source, label evidence date, observation window, and prediction horizon.
