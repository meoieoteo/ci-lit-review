# EHR Dementia Prediction Quality Review: wang2021_cognitive_decline_notes

## Review Status

Complete.

## Dementia-Relevance

High. The paper targets cognitive decline before MCI diagnosis and includes subjective cognitive decline, MCI, and dementia-related evidence.

## Prediction Versus Phenotyping

Primarily note phenotyping/diagnostic detection. It is temporally before MCI diagnosis, but the cohort is selected by that later diagnosis.

## Clinical Specificity

Good for evidence of progressive cognitive decline. Less specific for AD etiology, dementia subtype, and incident dementia.

## Feature Quality

High for note evidence. Notes are segmented into sections, and the model works on section-level text rather than entire heterogeneous notes.

## Model Quality

Strong internal model comparison with multiple baselines. Deep learning performs best, but XGBoost is close and less resource intensive.

## Implementation Quality

The model is plausible for screening but not clinically deployed in this paper. No downstream evaluation is reported.

## Review Use

Anchor evidence for note-based cognitive-decline detection. Pair with external validation and implementation papers when discussing clinical deployment.
