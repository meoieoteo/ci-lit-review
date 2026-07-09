# Primary Review: liu2018_deep_rl_dtr

## Review Status
primary_review_complete

## Review-Relevant Contribution
This paper provides dynamic treatment regime or reinforcement-learning background. This review is drafted from the neutral summary and available repository source status (`full_text`); the source PDF was not deeply re-extracted in this pass.

## Fit to Problem Statement
Indirect fit to the current pre-cardiology cognitive-risk project. Its main value is as methodological or representation background rather than as a complete cardiology-specific solution.

## Evidence Category
- `causal_inference`
- `longitudinal_ehr_representation`

## Clinical Target
Dynamic treatment policies with high expected reward, including survival and relapse-related reward structure.

## Data and Cohort Relevance
Center for International Blood and Marrow Transplant Research registry.

Population: 6,021 leukemia patients who underwent allogeneic hematopoietic cell transplantation.

## EHR Text Relevance
Limited direct EHR-text relevance based on the summary. If used in this review, it should mainly support non-text methods, study design, or background framing.

Inputs or predictors: Patient clinical states, treatment histories, and high-dimensional treatment options.

## Label or Outcome Relevance
Dynamic treatment policies with high expected reward, including survival and relapse-related reward structure.

Index date or time origin: Transplant and subsequent treatment decision stages.

Observation window: Treatment decisions from initial conditioning and prophylaxis through acute and chronic GVHD treatment stages up to four years.

Prediction horizon or follow-up: Four-year treatment-regime horizon after transplantation.

## Modeling Relevance
The framework uses supervised learning to predict likely expert actions and deep reinforcement learning to estimate long-term value functions over candidate actions.

## Validation and Utility Signals
Top-N expert-action prediction accuracy and expected reward under learned dynamic treatment regimes.

## Bias, Causality, and Downstream Action Issues
The summary does not establish that the paper solves downstream-action or diagnosis-opportunity bias for this project. It is most useful as later-stage sequential-decision or causal framing, not as a first risk-score implementation.

## Portability and Implementation Signals
Portability to a US Epic cardiology setting remains uncertain unless the paper specifically validates across sites, systems, or common data models. The paper should be treated as analogy or background unless later specialist review establishes direct fit.

## Key Extracted Claims
Top-N expert treatment prediction accuracy was generally between 75% and 90% for initial treatments, and DRL-based regimes showed high expected reward in experiments.

## What This Paper Supports
- Supports the outline section(s) associated with dynamic treatment regime or reinforcement-learning background.
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
Author-stated limitations: The paper notes limitations from available data size and uses separate models for different treatment stages.

Missing or ambiguous information: This is treatment-policy work rather than risk-score development.
