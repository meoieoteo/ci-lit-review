# Specialist Review: EHR Schema and Common Data Model

## Specialist Scope

Assessment of schema, feature, timestamp, and portability details in Wei et al.

## Bottom Line

Wei provides more implementation detail than many phenotyping papers, including ICD groups, medications, note types, and site experiments. It still does not provide a full Epic/OMOP mapping, note metadata model, or prospective encounter-timestamp design.

## Data Model and Source System Summary

MGH and BIDMC EHR data. No common data model is named.

## Unit of Analysis and Identifiers

The paper reports patients and visits. The model appears to classify MCI/ADRD status from patient/visit EHR features, but identifier-level joins are not described in database terms.

## Encounter and Timeline Representation

ICD assignment permits one day before and after the visit. If a patient had MED or ICD records, notes after first MED/ICD evidence were selected. This timing is appropriate for phenotyping but not for pre-index risk prediction.

## Cohort and Eligibility Implementation

Age 50+, at least one clinical note, stratified by MED/ICD status. Notes under 500 words excluded. Uncertain chart reviews excluded.

## Structured Feature Representation

Strong. The paper lists six ICD groups and dementia medication terms.

## Note and Text Metadata Representation

Notes include office visit, admission, progress, discharge, and correspondence notes from all specialties. The paper does not report note author, department, section, note signing time, addenda, or copied-forward handling.

## Label and Outcome Data Representation

Manual chart-review labels are assigned after reviewing notes in four MED/ICD strata. Label provenance is clear at a high level, but annotation schema details are limited.

## Vocabulary, Code Sets, and Mappings

ICD-9/ICD-10 codes are listed for Alzheimer's disease, vascular dementia, Lewy body dementia, frontotemporal dementia, unspecified dementias, and MCI. Medication list is also reported.

## Missingness, Data Quality, and Provenance

Sparse/administrative notes are excluded by word count. Missingness and utilization intensity are not deeply analyzed.

## Reproducibility and Portability

Code/data URLs are reported. Portability to other EHRs requires mapping local ICD, medication, and note-type metadata.

## Fit to Epic-to-Model-Ready Pipeline

Useful for local data dictionary fields: ICD groups, dementia medications, note text n-grams, note length filters, chart-review strata, and uncertain labels.

## Strengths

- Explicit ICD and medication groups.
- Multiple note types.
- Site-level experiments.
- Code/data availability statement.

## Concerns

- Date-range discrepancy in article.
- No common data model.
- No note timestamp/signing details.
- No annotation data model.

## Missing Information

Exact schema extraction logic, note metadata, review-tool details, and data availability verification.

## Implications for This Literature Review

Wei is a practical phenotyping implementation source, but local pipeline specs need more timestamp/provenance fields than the paper reports.

## Recommended Follow-up

Source-check the GitHub repository and use the listed code groups as a starting point for local concept-set review.
