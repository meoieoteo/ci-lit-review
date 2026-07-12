# Validation Review: wang2021_cognitive_decline_notes

## Review Status

Complete.

## Validation Design

Five-fold cross-validation on keyword-filtered dataset I and evaluation on a separate randomly sampled, non-keyword-filtered dataset II.

## Metrics

AUROC, AUPRC, PPV, sensitivity, and bootstrap confidence intervals.

## Main Results

The deep learning model achieved AUROC 0.971/AUPRC 0.933 in dataset I and AUROC 0.997/AUPRC 0.929 in dataset II. At a 0.5 cutoff, sensitivity was above 0.92 in both datasets and PPV was 0.848 in dataset I and 0.771 in dataset II.

## Strengths

AUPRC is appropriate for imbalanced data. Dataset II directly tests whether performance depends on keyword filtering. Multiple baselines are reported.

## Limitations

No external validation, no temporal deployment evaluation, no calibration reporting, no subgroup fairness analysis, and no patient-level clinical utility evaluation.

## Transportability

Uncertain. The authors explicitly state that documentation variation across systems may require retraining word embeddings and models.

## Use in Review

Use as strong internal validation for note-section classification, but not as evidence of cross-system performance.
