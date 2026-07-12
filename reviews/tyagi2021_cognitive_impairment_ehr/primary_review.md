# Primary Review: tyagi2021_cognitive_impairment_ehr

## Review Status

primary_review_complete

## Review-Relevant Contribution

Direct evidence that ClinicalBERT can classify note snippets for cognitive impairment evidence with high sequence-level performance.

## Publication Status and Evidence Weight

Direct topical fit but lower publication weight because the available source is a short workshop/preprint paper. Use mainly for NLP feasibility and method context.

## Fit to Problem Statement

Relevant to extracting cognitive evidence from notes, but it is not a patient-level pre-cardiology risk model.

## Evidence Category

`current_cognitive_impairment_detection`; `unstructured_ehr_text`; `note_concept_extraction`; `validation_or_reporting_quality`

## Clinical Target

Sequence-level evidence of cognitive impairment.

## Data and Cohort Relevance

MGB older-patient notes are relevant, but the cohort is enriched by dementia-related keyword matches and APOE availability.

## EHR Text Relevance

High for NLP classification of cognitive impairment mentions.

## Label or Outcome Relevance

Annotation rules distinguish cognitive impairment evidence from concern alone, which is useful for concept inventory design.

## Modeling Relevance

ClinicalBERT versus TF-IDF is a useful baseline comparison for text classification.

## Validation and Utility Signals

Holdout sequence-level performance is high, but patient-level deployment, calibration, and external validation are absent.

## Bias, Causality, and Downstream Action Issues

Keyword-centered sampling can overrepresent obvious documentation and underrepresent subtle impairment.

## Portability and Implementation Signals

The model would require local annotation and testing before use in cardiology notes.

## Key Extracted Claims

- 8,656 annotated sequences from 2,487 patients.
- ClinicalBERT reported AUC 0.98 and accuracy 0.93.
- Concern alone was not labeled as cognitive impairment.

## What This Paper Supports

Transformer models can classify explicit cognitive impairment evidence in EHR text.

## What This Paper Does Not Support

It does not establish patient-level future dementia prediction or external transportability.

## Default Specialist Reviews Called

All current specialist reviewers are called.

## Additional Specialist Reviews Needed

None.

## Primary Reviewer Notes

Useful for NLP annotation and method feasibility, not central outcome evidence.
