# Primary Review: wornow2023_ehrshot

## Review Status

Complete.

## Review-Relevant Contribution

EHRSHOT contributes a structured-EHR benchmark and few-shot evaluation framework for clinical foundation models. It is relevant to modeling strategy, especially when discussing sample efficiency and comparisons against count-based baselines.

## Publication Status and Evidence Weight

Publication status: preprint. Evidence weight: indirect and lower publication weight. It is technically useful but not dementia-specific and not peer-reviewed in the downloaded source.

## Fit to Problem Statement

Fit is moderate for modeling strategy and weak for the clinical target. It does not address dementia, cognitive impairment, notes, cardiology encounters, or downstream clinical action.

## Evidence Category

Indirect benchmark / methodological support.

## Clinical Target

No dementia or cardiology target. Tasks include operational outcomes, lab prediction, new diagnoses, and chest X-ray findings.

## Data and Cohort Relevance

The benchmark uses longitudinal Stanford Medicine structured EHR data from 6,739 selected patients, with a pretrained model built from 2.57 million patients. This is relevant to general EHR modeling but not to our specific cohort.

## EHR Text Relevance

Low. The released benchmark excludes clinical text. Chest X-ray labels are derived from radiology reports using a labeler, but the text itself is not released and the model does not ingest notes.

## Label or Outcome Relevance

The paper is useful for thinking about precise prediction times, horizons, and task definitions. Its labels are not cognitive-risk labels.

## Modeling Relevance

High. The paper shows that a structured-EHR foundation model can improve few-shot performance over count-based GBM at low k, while the count-based model can outperform the foundation model for some new-diagnosis tasks at higher k.

## Validation and Utility Signals

The benchmark has train/validation/test splits and repeated few-shot evaluations. It lacks external-site validation and clinical utility evaluation.

## Bias/Causality/Downstream Action Issues

The paper is not causal. It discusses privacy and data governance. It does not test clinical actionability, fairness, calibration, or subgroup harms in the main results.

## Portability/Implementation Signals

The code and model weights are released under access controls, and the pipeline uses structured EHR data. Portability remains uncertain because results are from Stanford only.

## Key Extracted Claims

- EHRSHOT includes 6,739 longitudinal Stanford Medicine patients, 41.6 million clinical events, and 921,499 encounters.
- CLMBR-T-base has 141M parameters and is pretrained on structured EHR data from 2.57 million patients.
- The benchmark defines 15 few-shot clinical prediction tasks.
- CLMBR-T-base outperforms count-based GBM for k <= 64 across aggregate task categories.
- GBM can outperform CLMBR-T-base on assignment-of-new-diagnosis tasks at larger k.

## What This Paper Supports

Use it to support the need for few-shot evaluation, strong structured baselines, transparent benchmark definitions, and caution that foundation models are not uniformly better.

## What This Paper Does Not Support

Do not use it for dementia prediction, note-based phenotyping, external generalizability, or clinical implementation.

## Default Specialist Reviews Called

All default specialist reviewers completed.

## Additional Specialist Reviews Needed

None required.

## Primary Reviewer Notes

This paper pairs well with Wornow's npj foundation-model review: one provides the critique, the other provides a benchmark attempting to test sample efficiency.
