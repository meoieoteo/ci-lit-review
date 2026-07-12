# Specialist Review: EHR Schema and Common Data Model

## Specialist Scope

Schema implications of transforming notes into cross-institution dementia-prediction features.

## Bottom Line

The paper is useful for showing cross-site portability problems, but it does not provide a reusable Epic/CDM extraction specification.

## Data Model and Source System Summary

Multiple institutional EHR note sources; source schemas are not the paper's main contribution.

## Unit of Analysis and Identifiers

Patient-level case/control modeling.

## Encounter and Timeline Representation

Lookback and prediction horizon are defined relative to index date.

## Cohort and Eligibility Implementation

Incident dementia cases and matched controls; code-level implementation requires source checking.

## Structured Feature Representation

Structured data are mainly used for cohort construction and matching, not as primary predictors.

## Note and Text Metadata Representation

Medical notes are used, but note types, authors, departments, and timestamps are not deeply specified in the summary.

## Label and Outcome Data Representation

Dementia labels are EHR-derived and require code/date provenance.

## Vocabulary, Code Sets, and Mappings

TF-ICF keywords and UMLS concepts are central mapping layers.

## Missingness, Data Quality, and Provenance

Institution-specific vocabulary and documentation are core data-quality concerns.

## Reproducibility and Portability

Portability is empirically limited across institutions.

## Fit to Epic-to-Model-Ready Pipeline

Useful warning that note feature engineering must be validated after schema/source transfer.

## Strengths

Explicit multi-institution evaluation and UMLS concept layer.

## Concerns

Insufficient operational note metadata for implementation.

## Missing Information

Local note classes, code sets, and feature availability timing.

## Implications for This Literature Review

Common concepts do not guarantee transportability.

## Recommended Follow-up

Use this when arguing for local validation after Epic-to-CDM transformation.
