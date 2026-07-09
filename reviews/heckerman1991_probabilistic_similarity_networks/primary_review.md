# Primary Review: heckerman1991_probabilistic_similarity_networks

## Review Status
primary_review_complete

## Review-Relevant Contribution
This paper provides sequential diagnosis, feature-acquisition, or decision-theoretic background. This review is drafted from the neutral summary and available repository source status (`full_text`); the source PDF was not deeply re-extracted in this pass.

## Fit to Problem Statement
Indirect fit to the current pre-cardiology cognitive-risk project. Its main value is as methodological or representation background rather than as a complete cardiology-specific solution.

## Evidence Category
- `sequential_diagnosis`

## Clinical Target
Diagnostic inference among competing hypotheses.

## Data and Cohort Relevance
The book discusses theory and examples, including Pathfinder.

Population: Not applicable.

## EHR Text Relevance
Limited direct EHR-text relevance based on the summary. If used in this review, it should mainly support non-text methods, study design, or background framing.

Inputs or predictors: Diagnostic findings and hypotheses in probabilistic knowledge maps.

## Label or Outcome Relevance
Diagnostic inference among competing hypotheses.

Index date or time origin: Not applicable.

Observation window: Not applicable.

Prediction horizon or follow-up: Not applicable.

## Modeling Relevance
The book presents similarity networks, partitions, knowledge maps, and probabilistic independence representations for diagnostic reasoning.

## Validation and Utility Signals
The book is primarily theoretical and methodological.

## Bias, Causality, and Downstream Action Issues
The summary does not establish that the paper solves downstream-action or diagnosis-opportunity bias for this project. It is most useful as later-stage sequential-decision or causal framing, not as a first risk-score implementation.

## Portability and Implementation Signals
Portability to a US Epic cardiology setting remains uncertain unless the paper specifically validates across sites, systems, or common data models. The paper should be treated as analogy or background unless later specialist review establishes direct fit.

## Key Extracted Claims
Similarity networks are presented as a way to simplify knowledge acquisition and represent asymmetric conditional independence in diagnostic models.

## What This Paper Supports
- Supports the outline section(s) associated with sequential diagnosis, feature-acquisition, or decision-theoretic background.
- Provides evidence or framing for the project's literature review, subject to the limitations above.

## What This Paper Does Not Support
- Does not by itself establish a deployable pre-cardiology cognitive-risk model.
- Does not by itself solve target definition, label validity, downstream-action bias, calibration, or workflow utility for this project.

## Default Specialist Reviews Called
- `ehr_dementia_prediction_quality_reviewer.md`
- `label_definition_reviewer.md`
- `validation_reviewer.md`

## Additional Specialist Reviews Needed
- Consider domain-specific specialist review if this paper becomes central to manuscript claims.

## Primary Reviewer Notes
Author-stated limitations: Not extracted in this draft.

Missing or ambiguous information: The extracted PDF metadata appears noisy, but the table of contents and title match the Heckerman monograph.
