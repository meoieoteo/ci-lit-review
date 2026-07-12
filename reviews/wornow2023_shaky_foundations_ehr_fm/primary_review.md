# Primary Review: wornow2023_shaky_foundations_ehr_fm

## Review Status

Complete.

## Review-Relevant Contribution

This review provides methodological guardrails for evaluating clinical language models and EHR foundation models. It is not dementia-specific, but it directly informs how we should discuss LLMs, transformers, and foundation-model approaches in an EHR cognitive-risk review.

## Publication Status and Evidence Weight

Publication status: peer-reviewed narrative review in npj Digital Medicine. Evidence weight: moderate as methodological background; indirect for dementia prediction.

## Fit to Problem Statement

Fit is strong for modeling-strategy discussion and weak for the clinical target. It does not address dementia, cognitive impairment, or pre-cardiology screening directly.

## Evidence Category

Indirect background / methodological framing.

## Clinical Target

No specific dementia or cardiology target. The paper reviews clinical foundation models broadly.

## Data and Cohort Relevance

The paper discusses EHR text and structured EMR data across many models, but it is not an original cohort study.

## EHR Text Relevance

High for the clinical-language-model portion. The review distinguishes clinical text models from structured EHR foundation models and notes that many clinical language models are trained on MIMIC-III or PubMed.

## Label or Outcome Relevance

No dementia label. The relevant point is that evaluation tasks often fail to map to outcomes or decisions that health systems actually need.

## Modeling Relevance

High. The paper cautions that foundation-model claims should be tested against specific benefits: predictive performance, sample efficiency, deployment cost, new applications, multimodality, and human-AI interfaces.

## Validation and Utility Signals

The central contribution is an evaluation critique: AUROC, AUPRC, F1, and accuracy do not by themselves establish clinical usefulness. The authors recommend ranking metrics under capacity constraints, calibration, subgroup fairness, human evaluation, and usability studies.

## Bias/Causality/Downstream Action Issues

The review explicitly raises bias, miscalibration, overfitting, automation bias, and the need to evaluate clinical utility and harm.

## Portability/Implementation Signals

The review emphasizes limitations from private data, lack of model-weight sharing for structured EHR foundation models, dataset concentration, and interoperability problems.

## Key Extracted Claims

- The review identified 84 clinical foundation models: 50 clinical language models and 34 foundation models for EMRs.
- Most models were evaluated on tasks that provide limited evidence of health-system usefulness.
- Most evaluations focus on predictive accuracy, while other claimed foundation-model benefits are under-tested.
- Clinical foundation models need evaluation tied to clinical utility, capacity, calibration, fairness, usability, and deployment burden.

## What This Paper Supports

Use this paper to justify skepticism about EHR foundation-model and LLM claims when evaluation does not match the intended clinical workflow.

## What This Paper Does Not Support

Do not use it as direct evidence for dementia detection, cardiology encounter screening, or a specific model choice for our task.

## Default Specialist Reviews Called

All default specialist reviewers completed.

## Additional Specialist Reviews Needed

None required.

## Primary Reviewer Notes

This should be a high-value background citation for Section 8, especially when contrasting foundation models with targeted, locally validated clinical prediction models.
