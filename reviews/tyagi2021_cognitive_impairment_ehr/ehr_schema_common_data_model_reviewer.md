# Specialist Review: EHR Schema and Common Data Model

## Specialist Scope

Schema implications of extracting keyword-centered note snippets.

## Bottom Line

The paper gives little reusable EHR schema guidance beyond the need to link notes to patients and extract local text windows.

## Data Model and Source System Summary

Mass General Brigham EHR notes linked to BioBank APOE data.

## Unit of Analysis and Identifiers

Sequence/snippet-level modeling nested within patients.

## Encounter and Timeline Representation

No deployment timeline or encounter index.

## Cohort and Eligibility Implementation

Age, APOE genotype availability, and dementia-keyword note presence.

## Structured Feature Representation

Structured data are not primary model predictors.

## Note and Text Metadata Representation

800-character windows around dementia-related keywords.

## Label and Outcome Data Representation

Human sequence labels.

## Vocabulary, Code Sets, and Mappings

Dementia keyword list drives sampling.

## Missingness, Data Quality, and Provenance

Keyword sampling and BioBank inclusion create selection.

## Reproducibility and Portability

Portable in method, but keyword lists and snippets need local validation.

## Fit to Epic-to-Model-Ready Pipeline

Low-to-moderate as an NLP extraction component.

## Strengths

Simple snippet extraction design.

## Concerns

No encounter-level feature availability model.

## Missing Information

Note classes, timestamps, departments, and patient-level split details.

## Implications for This Literature Review

Snippet classifiers need careful aggregation before use in encounter-level risk scoring.

## Recommended Follow-up

Use only after defining note-to-encounter joins and pre-index cutoffs.
