# Primary Review: li2025_multimodal_dementia

## Review Status

primary_review_complete

## Review-Relevant Contribution

Direct dissertation evidence on multimodal dementia detection from structured EHR data and medical notes, including decision-focused content selection and fusion.

## Publication Status and Evidence Weight

Direct topical fit, but lower publication weight because the source is a dissertation rather than a peer-reviewed journal article. Use for method context and hypothesis generation unless peer-reviewed components are identified.

## Fit to Problem Statement

Very strong conceptual fit: structured EHR plus notes, explicit observation windows and horizons, and early detection framing. It is not cardiology-specific.

## Evidence Category

`dementia_prediction`; `unstructured_ehr_text`; `longitudinal_ehr_representation`; `validation_or_reporting_quality`

## Clinical Target

Dementia case/control status at specified prediction horizons.

## Data and Cohort Relevance

INPC data and case-control cohorts are relevant but need source-checking for deployment comparability and control contamination.

## EHR Text Relevance

High. The dissertation focuses on lengthy medical notes and note-content selection.

## Label or Outcome Relevance

Relevant but needs careful review of case/control construction and label dates before manuscript claims.

## Modeling Relevance

High for multimodal fusion design and handling long notes.

## Validation and Utility Signals

Nested cross-validation is reported. External validation and prospective utility are not established.

## Bias, Causality, and Downstream Action Issues

Future diagnosis labels remain sensitive to downstream workup and diagnosis opportunity.

## Portability and Implementation Signals

Structured-data and note-fusion ideas are portable in principle but require local schema, note, and label mapping.

## Key Extracted Claims

- Uses observation periods of one to three years and horizons around 0.5 to 1 year.
- Combines Random Forest structured predictions with Longformer note embeddings.
- Reports multimodal fusion improvement over unimodal baselines.

## What This Paper Supports

Multimodal EHR plus notes is a plausible architecture family for dementia detection.

## What This Paper Does Not Support

It should not be cited as high-weight clinical evidence without peer-reviewed confirmation and external validation.

## Default Specialist Reviews Called

All current specialist reviewers are called.

## Additional Specialist Reviews Needed

Consider checking whether chapters overlap with peer-reviewed articles already in the bibliography.

## Primary Reviewer Notes

Direct but lower publication weight; preserve that distinction in synthesis.
