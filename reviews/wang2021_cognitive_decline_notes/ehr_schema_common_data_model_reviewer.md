# EHR Schema / Common Data Model Review: wang2021_cognitive_decline_notes

## Review Status

Complete.

## Data Model

Local Mass General Brigham Enterprise Data Warehouse. No common data model such as OMOP or FHIR is described.

## Structured Data Elements

Structured EHR fields are mainly used for cohort identification through ICD-10 MCI code G31.84.

## Unstructured Data Elements

Clinical note sections are the primary modeling input. Sections are generated and normalized by the Medical Text Extraction, Reasoning and Mapping System.

## Temporal Structure

The lookback window is four years before initial MCI diagnosis. The paper does not define a cardiology-style index encounter.

## Portability Concerns

Section headers, note-writing conventions, and embeddings may be site specific. The authors anticipate retraining for other institutions.

## Use in Review

Use to motivate explicit note-section processing and temporal lookback windows in the proposed EHR schema.
