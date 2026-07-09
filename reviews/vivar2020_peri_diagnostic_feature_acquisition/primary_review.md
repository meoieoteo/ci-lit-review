# Primary Review: vivar2020_peri_diagnostic_feature_acquisition

## Review Status
primary_review_complete

## Review-Relevant Contribution
This paper provides sequential diagnosis, feature-acquisition, or decision-theoretic background. This review is drafted from the neutral summary and available repository source status (`full_text`); the source PDF was not deeply re-extracted in this pass.

## Fit to Problem Statement
Indirect fit to the current pre-cardiology cognitive-risk project. Its main value is as methodological or representation background rather than as a complete cardiology-specific solution.

## Evidence Category
- `sequential_diagnosis`

## Clinical Target
Accurate diagnosis with fewer or lower-cost acquired features.

## Data and Cohort Relevance
Two public medical datasets and two synthetic datasets.

Population: Not a single clinical cohort; public medical datasets are used for evaluation.

## EHR Text Relevance
Limited direct EHR-text relevance based on the summary. If used in this review, it should mainly support non-text methods, study design, or background framing.

Inputs or predictors: Partially observed feature vectors and feature costs.

## Label or Outcome Relevance
Accurate diagnosis with fewer or lower-cost acquired features.

Index date or time origin: The decision point is the current diagnostic state with partial features observed.

Observation window: Sequential acquisition during a diagnostic workflow.

Prediction horizon or follow-up: Not a future prediction task; the target is diagnosis after feature acquisition.

## Modeling Relevance
The authors train neural networks with input dropout and use integrated gradients at test time to estimate which missing feature is most valuable. They introduce accumulated integrated gradients for dynamic acquisition.

## Validation and Utility Signals
Accuracy and feature/cost efficiency on medical and synthetic datasets.

## Bias, Causality, and Downstream Action Issues
The summary does not establish that the paper solves downstream-action or diagnosis-opportunity bias for this project. It is most useful as later-stage sequential-decision or causal framing, not as a first risk-score implementation.

## Portability and Implementation Signals
Portability to a US Epic cardiology setting remains uncertain unless the paper specifically validates across sites, systems, or common data models. The paper should be treated as analogy or background unless later specialist review establishes direct fit.

## Key Extracted Claims
The proposed approach is reported to be more cost- and feature-efficient than prior approaches while achieving higher overall accuracy.

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
Author-stated limitations: The paper discusses limitations of prior RL and attribution approaches; detailed limitations of the proposed method are not extracted in this draft.

Missing or ambiguous information: This paper is about within-diagnostic feature acquisition, not pre-encounter risk scoring.
