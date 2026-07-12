# Primary Review: wang2021_cognitive_decline_notes

## Review Status

Complete.

## Review-Relevant Contribution

Wang et al. provide strong direct evidence that clinical notes can reveal cognitive decline before structured MCI diagnosis and that supervised NLP can detect those signals at scale.

## Publication Status and Evidence Weight

Publication status: peer-reviewed JAMA Network Open article. Evidence weight: high for note-based cognitive-decline detection; moderate for prospective risk prediction because the cohort was selected by later MCI diagnosis and lacked external validation.

## Fit to Problem Statement

Fit is strong for dementia/cognitive-risk detection from EHR notes. Fit is weaker for cardiology-specific workflows and prospective pre-encounter prediction.

## Evidence Category

Direct peer-reviewed evidence.

## Clinical Target

Evidence of progressive cognitive decline spanning subjective cognitive decline, MCI, and dementia in notes preceding MCI diagnosis.

## Data and Cohort Relevance

Patients were aged 50 or older in Mass General Brigham and had initial MCI diagnosis in 2019. Notes from the preceding four years were evaluated.

## EHR Text Relevance

Very high. The model operates on note sections and directly addresses information not captured in structured EHR fields.

## Label or Outcome Relevance

The label is carefully defined and manually annotated with expert involvement. It is section-level evidence of decline rather than patient-level incident dementia.

## Modeling Relevance

The paper compares deep learning with logistic regression, random forest, SVM, and XGBoost baselines. It also evaluates performance on a non-keyword-filtered dataset, which strengthens the argument beyond keyword search.

## Validation and Utility Signals

Internal validation is strong for a note-classification study, including two reference datasets, AUROC/AUPRC, bootstrap CIs, and TRIPOD reporting. There is no external validation or clinical implementation evaluation.

## Bias/Causality/Downstream Action Issues

The study is diagnostic/phenotyping rather than causal. Cohort selection on MCI diagnosis may limit generalizability to undiagnosed patients. Documentation patterns, specialty access, and clinician attention may influence signals.

## Portability/Implementation Signals

The authors note that word embeddings and models may need retraining across institutions. XGBoost is presented as a lower-compute alternative when GPU resources are unavailable.

## Key Extracted Claims

- Notes before MCI diagnosis contain detectable evidence of cognitive decline.
- Deep learning achieved AUROC 0.971/AUPRC 0.933 in keyword-filtered sections and AUROC 0.997/AUPRC 0.929 in non-keyword-filtered sections.
- Keyword search had low PPV despite sensitivity in dataset II.
- XGBoost was a strong conventional baseline.

## What This Paper Supports

Use to support inclusion of clinical notes, section-level NLP, and supervised models for cognitive-decline evidence before structured diagnosis.

## What This Paper Does Not Support

Do not use it as external-validation evidence, general-population dementia-risk prediction, or evidence of benefit in a cardiology workflow.

## Default Specialist Reviews Called

All default specialist reviewers completed.

## Additional Specialist Reviews Needed

None required.

## Primary Reviewer Notes

This should be one of the anchor papers for note-based cognitive decline detection, with careful wording about the selected MCI cohort.
