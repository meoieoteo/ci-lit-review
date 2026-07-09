# Primary Review: li2020_behrt

## Review Status
primary_review_complete

## Review-Relevant Contribution
This paper provides longitudinal EHR representation background. This review is drafted from the neutral summary and available repository source status (`full_text`); the source PDF was not deeply re-extracted in this pass.

## Fit to Problem Statement
Indirect fit to the current pre-cardiology cognitive-risk project. Its main value is as methodological or representation background rather than as a complete cardiology-specific solution.

## Evidence Category
- `longitudinal_ehr_representation`
- `unstructured_ehr_text`

## Clinical Target
Onset prediction for 301 medical conditions.

## Data and Cohort Relevance
Clinical Practice Research Datalink linked with hospital and administrative datasets in the UK.

Population: Nearly 1.6 million individuals in the model evaluation described in the abstract.

## EHR Text Relevance
Relevant because the paper concerns clinical text, NLP, speech/language, or language-model methods.

Inputs or predictors: Structured EHR concepts such as diagnoses, medications, measurements, age, segment, and positional/time information.

## Label or Outcome Relevance
Onset prediction for 301 medical conditions.

Index date or time origin: Prediction points are based on patient EHR timelines and prior events.

Observation window: Longitudinal primary care and linked secondary care histories.

Prediction horizon or follow-up: Future onset of 301 conditions.

## Modeling Relevance
The authors adapt transformer self-attention to EHR sequences and use BERT-style pre-training/fine-tuning ideas for disease trajectory modeling.

## Validation and Utility Signals
Average precision score for future disease prediction.

## Bias, Causality, and Downstream Action Issues
The summary does not establish that the paper solves downstream-action or diagnosis-opportunity bias for this project. Any use for the project should preserve uncertainty about target timing, label validity, and clinical actionability.

## Portability and Implementation Signals
Portability to a US Epic cardiology setting remains uncertain unless the paper specifically validates across sites, systems, or common data models. The paper should be treated as analogy or background unless later specialist review establishes direct fit.

## Key Extracted Claims
BEHRT achieved absolute average-precision improvements of 8.0-10.8 percentage points compared with prior deep EHR models when predicting onset of 301 conditions.

## What This Paper Supports
- Supports the outline section(s) associated with longitudinal EHR representation background.
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

Missing or ambiguous information: This is structured longitudinal EHR modeling, not clinical-note modeling.
