# EHR Schema and Common Data Model Review: shen2025_integrating_misclassified_ehr_outcomes

## Review Status

specialist_complete

## Data Model Relevance

The paper is not a schema or common-data-model paper. Its relevance is that EHR pipelines should distinguish silver-standard labels from validation labels and preserve enough provenance to estimate misclassification.

## Useful Data Elements

- Silver-standard outcome source and date.
- Gold-standard or adjudicated validation outcome source and date.
- Sampling mechanism for validation cases.
- Covariates used in selection and outcome models.
- Treatment or exposure definition, if causal estimands are studied.
- Completeness indicators and reasons for missing validation outcome.

## Schema Implications for This Project

The model-ready dataset should not contain only a single collapsed dementia outcome. It should carry separate columns for diagnosis codes, cognitive testing, referrals, medications, specialist notes, chart-reviewed outcomes, and adjudication status, along with the provenance of each label source.

## Limitations

No implementation details are given for Epic, OMOP, note metadata, or vocabulary mapping.

## Recommended Use

Use as a rationale for explicit label-provenance tables and validation-sample metadata in the local data specification.
