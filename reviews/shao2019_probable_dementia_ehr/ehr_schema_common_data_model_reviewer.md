# Specialist Review: EHR Schema and Common Data Model

## Specialist Scope

Assessment of EHR source schema, feature construction, and portability.

## Bottom Line

Useful but not implementation-complete. The paper identifies key EHR domains and time windows, but it does not provide enough schema detail to directly reproduce the pipeline in Epic or OMOP.

## Data Model and Source System Summary

VHA clinical and administrative data from CDW/VINCI, including diagnoses, procedures, medications, clinical document types, and clinical note text.

## Unit of Analysis and Identifiers

Patient-level analysis. It does not use encounter-level prediction units.

## Encounter and Timeline Representation

The primary time structure is a three-year lookback before first dementia diagnosis or a random control visit date. Detailed event timestamp handling is not described.

## Cohort and Eligibility Implementation

Eligibility is operationalized through age, ICD-9 dementia codes, visit/note availability, medications, and matching variables. These criteria are implementable but VHA-specific.

## Structured Feature Representation

Structured features include ICD codes, CPT codes, medications, and document types aggregated over the observation window.

## Note and Text Metadata Representation

Clinical notes are modeled as a large text corpus. Note types enter as structured features, but detailed note metadata, sectioning, authorship, signing time, and copied-forward handling are not reported.

## Label and Outcome Data Representation

Labels come from dementia ICD-9 codes, anti-dementia medications for control exclusion, and specialist chart review for validation.

## Vocabulary, Code Sets, and Mappings

Dementia ICD-9 codes are listed. Other feature code sets are not fully enumerated.

## Missingness, Data Quality, and Provenance

The study requires minimum note/visit availability for cases. Broader missingness and data-quality handling are limited.

## Reproducibility and Portability

Partial. The broad pipeline is portable conceptually, but local implementation would require re-creating topic models, feature extraction, and code sets.

## Fit to Epic-to-Model-Ready Pipeline

Indirect. It supports a patient-history feature table built from structured events and notes, but it does not define an Epic-to-common-data-model path.

## Strengths

- Clear high-level EHR domains.
- Explicit lookback window.
- Combines structured and unstructured data.

## Concerns

- Patient-level rather than encounter-level design.
- Limited timestamp/provenance details.
- Local VHA data model not mapped to standard concepts.

## Missing Information

- Source table/domain details.
- Full feature lists.
- Note metadata and timestamp rules.

## Implications for This Literature Review

Use as an example of feature-table construction from longitudinal EHR history, not as a reproducible Epic pipeline.

## Recommended Follow-up

For local design, create a data dictionary that separates code domains, note metadata, and feature availability timestamps.
