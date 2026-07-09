# Primary Review: pellegrini2018_neuroimaging_ml_review

## Review Status
primary_review_complete

## Review-Relevant Contribution
This paper provides dementia, MCI, or Alzheimer disease prediction evidence. This review is drafted from the neutral summary and available repository source status (`full_text`); the source PDF was not deeply re-extracted in this pass.

## Fit to Problem Statement
Direct or moderate fit to the current pre-cardiology cognitive-risk project. Its main value is as dementia/cognitive prediction context rather than as a complete cardiology-specific solution.

## Evidence Category
- `dementia_prediction`
- `longitudinal_ehr_representation`
- `sequential_diagnosis`

## Clinical Target
Diagnostic categories spanning healthy aging, MCI, and dementia.

## Data and Cohort Relevance
Published studies from 2006 to late 2016.

Population: Participants in included neuroimaging studies, commonly healthy controls, MCI participants, and people with AD or other dementia types.

## EHR Text Relevance
Limited direct EHR-text relevance based on the summary. If used in this review, it should mainly support non-text methods, study design, or background framing.

Inputs or predictors: Mostly neuroimaging, especially T1-weighted MRI, sometimes combined with other data types.

## Label or Outcome Relevance
Diagnostic categories spanning healthy aging, MCI, and dementia.

Index date or time origin: Varied by included study.

Observation window: Varied by included study.

Prediction horizon or follow-up: Varied; some studies considered MCI converter versus non-converter classification.

## Modeling Relevance
The authors reviewed 111 studies, assessed study quality, and compared reported accuracy across disease boundaries, data sources, sample sizes, and ML methods.

## Validation and Utility Signals
Reported accuracy across included studies.

## Bias, Causality, and Downstream Action Issues
The summary does not establish that the paper solves downstream-action or diagnosis-opportunity bias for this project. It is most useful as later-stage sequential-decision or causal framing, not as a first risk-score implementation.

## Portability and Implementation Signals
Portability to a US Epic cardiology setting remains uncertain unless the paper specifically validates across sites, systems, or common data models. The paper should be treated as direct evidence only where its population and data match the project.

## Key Extracted Claims
Most studies assessed AD versus healthy controls, used ADNI, support vector machines, and T1-weighted MRI. Accuracy was highest for AD versus healthy controls and poorer for healthy control versus MCI versus AD and MCI converter versus non-converter tasks. Combined data types improved accuracy more than sample size, data source, or ML method.

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
Author-stated limitations: The authors conclude that machine learning did not yet differentiate clinically relevant disease categories sufficiently and called for more diverse datasets, multimodal data, and clinical integration.

Missing or ambiguous information: This paper is neuroimaging-focused rather than EHR-text-focused.
