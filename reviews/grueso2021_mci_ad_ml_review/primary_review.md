# Primary Review: grueso2021_mci_ad_ml_review

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
Stable MCI versus progressive MCI / conversion to AD dementia.

## Data and Cohort Relevance
Published studies identified through database searches; most included studies used ADNI.

Population: Participants in included studies generally included stable MCI, progressive MCI, AD, and healthy control groups.

## EHR Text Relevance
Limited direct EHR-text relevance based on the summary. If used in this review, it should mainly support non-text methods, study design, or background framing.

Inputs or predictors: Mainly neuroimaging features from MRI and PET, sometimes combined with genetic, cognitive, or other clinical variables.

## Label or Outcome Relevance
Stable MCI versus progressive MCI / conversion to AD dementia.

Index date or time origin: Varied by included study, usually baseline MCI assessment.

Observation window: Varied by included study; the review notes follow-up definitions such as three years for ADNI and one year for AddNeuroMed in some contexts.

Prediction horizon or follow-up: Progression from MCI to AD dementia during study-specific follow-up periods.

## Modeling Relevance
The authors followed PRISMA-style review methods and extracted study design, data source, neuroimaging modality, features, classifier, validation method, accuracy, and AUC.

## Validation and Utility Signals
The review reports accuracy and AUC where available.

## Bias, Causality, and Downstream Action Issues
The summary does not establish that the paper solves downstream-action or diagnosis-opportunity bias for this project. Any use for the project should preserve uncertainty about target timing, label validity, and clinical actionability.

## Portability and Implementation Signals
Portability to a US Epic cardiology setting remains uncertain unless the paper specifically validates across sites, systems, or common data models. The paper should be treated as direct evidence only where its population and data match the project.

## Key Extracted Claims
Of 116 reviewed studies, most used ADNI data, MRI, and SVM. SVM had mean accuracy around 75.4%, while convolutional neural networks had mean accuracy around 78.5%. MRI plus PET studies generally performed better than single-modality studies.

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
Author-stated limitations: The review highlights concerns about generalizability, heavy reliance on ADNI, and clinically relevant prediction remaining difficult.

Missing or ambiguous information: This review is focused largely on neuroimaging, not EHR text.
