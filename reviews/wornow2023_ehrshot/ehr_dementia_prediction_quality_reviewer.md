# EHR Dementia Prediction Quality Review: wornow2023_ehrshot

## Review Status

Complete.

## Dementia-Relevance

Indirect. No dementia, MCI, cognitive impairment, or cognitive-screening task is included in the reviewed material.

## Prediction Versus Phenotyping

The paper is a benchmark of prediction tasks with defined prediction times, not a dementia phenotyping study.

## Clinical Specificity

Low for dementia. Moderate for general EHR prediction methodology.

## Feature Quality

The structured-EHR feature space is broad: demographics, diagnoses, procedures, labs, medications, and other coded events. It excludes clinical notes, which are central to many dementia-detection strategies.

## Model Quality

The paper provides a strong comparison between a pretrained structured-EHR model and count-based GBM. It is especially useful because it shows that foundation models may help most when labeled examples are scarce, but are not universally superior.

## Implementation Quality

The benchmark is designed for reproducibility rather than clinical deployment. It does not evaluate workflow, care impact, or prospective use.

## Review Use

Use to inform modeling strategy, not as dementia-prediction evidence.
