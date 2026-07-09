# Primary Review: grammenos2024_explainable_mci_ad

## Review Status
primary_review_complete

## Review-Relevant Contribution
This paper provides dementia, MCI, or Alzheimer disease prediction evidence. This review is drafted from the neutral summary and available repository source status (`full_text`); the source PDF was not deeply re-extracted in this pass.

## Fit to Problem Statement
Direct or moderate fit to the current pre-cardiology cognitive-risk project. Its main value is as dementia/cognitive prediction context rather than as a complete cardiology-specific solution.

## Evidence Category
- `dementia_prediction`
- `longitudinal_ehr_representation`
- `validation_or_reporting_quality`

## Clinical Target
Stable MCI versus MCI transition to Alzheimer disease.

## Data and Cohort Relevance
ADNIMERGE data from ADNI phases ADNI1, ADNI2, ADNI3, and ADNI-GO.

Population: The paper describes an initial ADNI dataset of 2378 participants and a modeled MCI cohort with stable and transition groups after preprocessing.

## EHR Text Relevance
Limited direct EHR-text relevance based on the summary. If used in this review, it should mainly support non-text methods, study design, or background framing.

Inputs or predictors: ADNI clinical, cognitive, imaging, genetic, biomarker, and demographic variables available in ADNIMERGE.

## Label or Outcome Relevance
Stable MCI versus MCI transition to Alzheimer disease.

Index date or time origin: Baseline ADNI visit.

Observation window: Longitudinal data from baseline through follow-up visits, including a 48-month observation framing in the methods.

Prediction horizon or follow-up: The abstract describes a 36-month prediction period; the introduction and methods also discuss 48-month transition framing.

## Modeling Relevance
The authors compare multiple classifiers, select XGBoost, tune hyperparameters, use Recursive Feature Elimination, and apply SHAP values for explanation.

## Validation and Utility Signals
Five-fold cross-validation is reported with precision, recall, F1, accuracy, and ROC AUC.

## Bias, Causality, and Downstream Action Issues
The summary does not establish that the paper solves downstream-action or diagnosis-opportunity bias for this project. Any use for the project should preserve uncertainty about target timing, label validity, and clinical actionability.

## Portability and Implementation Signals
Portability to a US Epic cardiology setting remains uncertain unless the paper specifically validates across sites, systems, or common data models. The paper should be treated as direct evidence only where its population and data match the project.

## Key Extracted Claims
The reported average accuracy is 0.85 and ROC AUC is 0.86. Stable class precision/recall/F1 were 0.94/0.84/0.90, and transition class precision/recall/F1 were 0.71/0.88/0.79.

## What This Paper Supports
- Supports the outline section(s) associated with dementia, MCI, or Alzheimer disease prediction evidence.
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
Author-stated limitations: Not extracted in detail in this draft.

Missing or ambiguous information: The paper uses both 36-month and 48-month language. A later review should reconcile the exact target horizon from the methods and cohort construction.
