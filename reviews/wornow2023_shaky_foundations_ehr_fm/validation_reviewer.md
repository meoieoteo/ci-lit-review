# Validation Review: wornow2023_shaky_foundations_ehr_fm

## Review Status

Complete.

## Validation Design

Narrative review, not an original validation study.

## Metrics

The paper critiques common metrics such as AUROC, AUPRC, F1, accuracy, ROUGE, METEOR, and BLEU when used without clinical context.

## Main Results

The authors conclude that most clinical foundation-model evaluations demonstrate improved predictive accuracy but give limited evidence for health-system usefulness, sample efficiency, deployment simplification, multimodality, or human-AI interface value.

## Strengths

The paper provides a practical evaluation agenda: top-K/ranking metrics under capacity constraints, calibration, subgroup fairness, human evaluation, small-label performance, deployment cost, and usability.

## Limitations

The review is not systematic, does not revalidate models, and does not quantify risk of bias across studies.

## Transportability

The paper highlights transportability concerns from MIMIC/PubMed concentration, private training data, lack of FEMR model sharing, and heterogeneous EHR schemas.

## Use in Review

Use as a validation-quality standard for judging LLM/foundation-model papers rather than as primary evidence of any clinical model's performance.
