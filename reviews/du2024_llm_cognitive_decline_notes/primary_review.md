# Primary Review: du2024_llm_cognitive_decline_notes

## Review Status

Complete.

## Review-Relevant Contribution

Du et al. directly compare GPT-4, Llama 2, locally trained models, and an ensemble for detecting cognitive decline from real clinical notes.

## Publication Status and Evidence Weight

Publication status: peer-reviewed with prior preprint. Evidence weight: direct and moderate-to-high for internal model comparison; moderate for broader claims because models, prompts, and sites may not generalize.

## Fit to Problem Statement

Strong for EHR-note cognitive-decline modeling and LLM strategy. Weak for cardiology-specific screening and prospective clinical utility.

## Evidence Category

Direct model-comparison evidence.

## Clinical Target

Section-level evidence of cognitive decline spanning SCD, MCI, and dementia.

## Data and Cohort Relevance

MGB patients aged 50 or older with initial MCI diagnosis in 2019; notes from the preceding four years. This mirrors Wang 2021.

## EHR Text Relevance

Very high. The paper evaluates real clinical notes in HIPAA-compliant cloud LLM environments.

## Label or Outcome Relevance

The label definition is strong for note evidence but not a patient-level incident dementia endpoint.

## Modeling Relevance

High. The key finding is that GPT-4 did not outperform locally trained task-specific models, but an ensemble of GPT-4, DNN, and XGBoost improved performance.

## Validation and Utility Signals

Internal evaluation on a non-keyword-filtered test set is useful. The paper lacks external validation, calibration, subgroup analysis, and prospective deployment evaluation.

## Bias/Causality/Downstream Action Issues

No causal design. LLM performance may reflect prompt design, deployment environment, model version, documentation style, and selected cohort.

## Portability/Implementation Signals

The HIPAA-compliant Azure/OpenAI and AWS/Llama setup is implementation-relevant, but local validation and model-version monitoring would be required.

## Key Extracted Claims

- GPT-4 was better than Llama 2 but did not outperform locally trained traditional models.
- Error-analysis-based prompting improved GPT-4.
- The majority-vote ensemble reached precision 90.2%, recall 94.2%, and F1 92.1%.
- Only two cases were incorrectly predicted by all three ensemble components among 63 samples missed by at least one model.

## What This Paper Supports

Use it to argue that LLMs should be evaluated against local task-specific baselines and may be most valuable as complementary components.

## What This Paper Does Not Support

Do not use it to claim standalone LLM superiority, external generalizability, or clinical outcome benefit.

## Default Specialist Reviews Called

All default specialist reviewers completed.

## Additional Specialist Reviews Needed

None required.

## Primary Reviewer Notes

This is an important companion to Wang 2021 because it updates the same task for the LLM era.
