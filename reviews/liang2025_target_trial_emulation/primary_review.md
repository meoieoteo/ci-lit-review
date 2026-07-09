# Primary Review: liang2025_target_trial_emulation

## Review Status
primary_review_complete

## Review-Relevant Contribution
This paper provides target-trial and causal study-design background. This review is drafted from the neutral summary and available repository source status (`full_text`); the source PDF was not deeply re-extracted in this pass.

## Fit to Problem Statement
Indirect fit to the current pre-cardiology cognitive-risk project. Its main value is as methodological or representation background rather than as a complete cardiology-specific solution.

## Evidence Category
- `causal_inference`
- `longitudinal_ehr_representation`

## Clinical Target
Design of stronger causal and clinical evidence from observational data.

## Data and Cohort Relevance
Narrative discussion of cohort studies, randomized trials, and target trial emulation.

Population: Not a single study population.

## EHR Text Relevance
Limited direct EHR-text relevance based on the summary. If used in this review, it should mainly support non-text methods, study design, or background framing.

Inputs or predictors: Exposure, treatment, covariate, outcome, follow-up, and eligibility definitions in observational clinical research.

## Label or Outcome Relevance
Design of stronger causal and clinical evidence from observational data.

Index date or time origin: Depends on the emulated target trial or cohort design.

Observation window: Longitudinal follow-up is central to cohort studies and target trial emulation.

Prediction horizon or follow-up: Not a prediction paper.

## Modeling Relevance
The commentary compares cohort studies, randomized controlled trials, and target trial emulation, describing strengths, limitations, and future directions.

## Validation and Utility Signals
Not applicable.

## Bias, Causality, and Downstream Action Issues
The summary does not establish that the paper solves downstream-action or diagnosis-opportunity bias for this project. It is most useful as later-stage sequential-decision or causal framing, not as a first risk-score implementation.

## Portability and Implementation Signals
Portability to a US Epic cardiology setting remains uncertain unless the paper specifically validates across sites, systems, or common data models. The paper should be treated as analogy or background unless later specialist review establishes direct fit.

## Key Extracted Claims
The authors argue that cohort studies and target trial emulation can provide important real-world evidence, but require standardized data processing, careful control of bias, and better data-sharing infrastructure.

## What This Paper Supports
- Supports the outline section(s) associated with target-trial and causal study-design background.
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
Author-stated limitations: The commentary notes limitations including cost and follow-up loss for cohorts and lack of randomization/assumptions for target trial emulation.

Missing or ambiguous information: This is a design/commentary paper, not an empirical model study.
