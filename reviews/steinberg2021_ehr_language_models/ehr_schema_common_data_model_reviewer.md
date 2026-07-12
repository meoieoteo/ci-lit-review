# Specialist Review: EHR Schema and Common Data Model

## Specialist Scope

Assessment of data representation and portability for Steinberg et al.

## Bottom Line

The paper is useful for structured-EHR sequence representation and includes an OHDSI implementation signal, but it does not provide an Epic-to-model-ready pipeline for notes or dementia labels.

## Data Model and Source System Summary

De-identified Stanford EHR data from Stanford Hospital and Lucile Packard Children's Hospital. The paper reports a CLMBR implementation backported for the OHDSI schema in `ehr_ml.clmbr`.

## Unit of Analysis and Identifiers

Examples are patient plus time-of-prediction. A patient can appear in multiple splits, but prediction times do not overlap.

## Encounter and Timeline Representation

Records are represented as ordered sequences of days; each day includes sets of diagnosis, procedure, medication-order, and lab-order codes. CLMBR also uses age and time-delta features.

## Cohort and Eligibility Implementation

Cohort construction is outcome-specific. The paper gives outcome counts but not reusable SQL.

## Structured Feature Representation

Strong. Uses ICD-10, CPT/HCPCS, RxCUI, and LOINC codes, ontology expansion through UMLS, count features, embeddings, and language-model representations.

## Note and Text Metadata Representation

Not applicable. Clinical notes are not used.

## Label and Outcome Data Representation

Task labels are operational structured outcomes; not dementia labels.

## Vocabulary, Code Sets, and Mappings

The paper reports vocabulary families and ontology expansion. It does not publish full concept sets in the article.

## Missingness, Data Quality, and Provenance

Limited discussion. Quantitative labs and vitals are omitted because unavailable in the de-identified EHR data.

## Reproducibility and Portability

The OHDSI-compatible implementation is a strong portability signal. Cross-site performance is not tested.

## Fit to Epic-to-Model-Ready Pipeline

Useful for a structured-code sequence pipeline after Epic-to-standard-code mapping. Not sufficient for note extraction or cognitive labels.

## Strengths

- Explicit code systems.
- Daily temporal sequence design.
- UMLS ontology expansion.
- OHDSI implementation note.

## Concerns

- No note pipeline.
- No dementia label representation.
- No cross-institution transport test.

## Missing Information

Detailed source table mappings and full feature construction code beyond the package reference.

## Implications for This Literature Review

Steinberg should inform the structured baseline and representation-learning options, not the NLP or label sections.

## Recommended Follow-up

Check `ehr_ml.clmbr` only if the project decides to test CLMBR-like structured representations.
