# Validation Review: du2024_llm_cognitive_decline_notes

## Review Status

Complete.

## Validation Design

Prompt/model development used a keyword-filtered dataset; testing used a non-keyword-filtered annotated dataset. The ensemble combines GPT-4, attention-based DNN, and XGBoost by majority vote.

## Metrics

Confusion-matrix metrics including precision, recall/sensitivity, specificity, F1, and NPV.

## Main Results

The ensemble achieved precision 90.2%, recall 94.2%, and F1 92.1%, significantly outperforming individual models. GPT-4 did not outperform the locally trained models.

## Strengths

Direct comparison of LLMs and local models on real EHR notes; prompt refinement documented; error-profile comparison supports ensemble rationale.

## Limitations

No external validation, no calibration or fairness evaluation, model versions may become obsolete, and the ensemble needs larger testing outside the original dataset.

## Transportability

Unknown. LLM prompting may be portable, but performance depends on local documentation and task definitions.

## Use in Review

Use to support explicit validation of LLMs against local baselines and ensemble strategies.
