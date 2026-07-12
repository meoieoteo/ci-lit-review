# Validation Review: wornow2023_ehrshot

## Review Status

Complete.

## Validation Design

Benchmark train/validation/test design with few-shot evaluation. Models are trained with k positive and k negative examples for k from 1 to 128, plus full-data comparisons.

## Metrics

AUROC and AUPRC.

## Main Results

CLMBR-T-base outperforms count-based GBM across aggregate task categories for k <= 64. Performance advantages are strongest in data-poor regimes and shrink with more labeled data. GBM outperforms CLMBR-T-base on assignment-of-new-diagnosis tasks at k > 64.

## Strengths

The benchmark is explicit, reproducible in design, and compares against a strong count-based baseline. It releases code, task definitions, and model weights under access controls.

## Limitations

No external validation. One institution. One foundation model. No clinical utility analysis. Some tasks have very small positive test counts. No main calibration, fairness, or subgroup analyses are emphasized in the extracted text.

## Transportability

Unknown. The authors expect some drop at other institutions but do not quantify it.

## Use in Review

Use to support few-shot validation as a design requirement and to warn that model ranking can reverse by task and label availability.
