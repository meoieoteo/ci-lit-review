# EHR Schema / Common Data Model Review: hong2020_cognitive_concerns_nlp

## Review Status

Complete.

## Data Model

The paper uses local MGB EHR data. It does not describe use of OMOP, FHIR, PCORnet, or another common data model.

## Structured Data Elements

Structured inputs include ICD diagnoses and cognitive-related medications: galantamine, donepezil, rivastigmine, and memantine.

## Unstructured Data Elements

Progress notes are the key data source. The paper includes preprocessing to trim notes and remove noise, but does not provide a portable note-section schema.

## Temporal Structure

Inputs are drawn from the 2018 calendar year. The task is not specified using an index encounter, prediction horizon, or clean lookback/outcome separation.

## Portability Concerns

Porting would require local mappings for cognitive ICD codes, medication lists, note types, note preprocessing, and possibly institution-specific language.

## Use in Review

Useful for motivating a multimodal EHR schema that includes notes alongside diagnosis and medication features. Not useful as a template for common-data-model implementation.
