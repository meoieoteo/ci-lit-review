# Specialist Review: Validation

## Specialist Scope

Validation of cognitive-impairment text classification.

## Bottom Line

Sequence-level performance is high, but deployment-level validation is not shown.

## Validation Design Summary

90/10 split over annotated sequences.

## Development and Validation Separation

Holdout split is reported; patient-level independence needs confirmation.

## Internal Validation

Internal holdout only.

## Temporal Validation

None.

## External Validation

None.

## Transportability

Unproven outside MGB notes and keyword-selected snippets.

## Calibration

Not reported.

## Thresholds and Operating Points

Sensitivity and specificity are reported, but threshold selection is not a deployment threshold.

## Clinical Utility

Not established.

## Subgroup and Fairness Evaluation

Not reported.

## Robustness and Sensitivity Analyses

Limited in short paper.

## Reporting Completeness

Short source omits many implementation details.

## Reproducibility

ClinicalBERT baseline is reproducible in principle; annotations are not fully reusable.

## Fit to Pre-Cardiology Risk Scoring

Useful as component validation only.

## Strengths

Clear baseline comparison and high holdout metrics.

## Concerns

No external, patient-level, calibration, or workflow validation.

## Missing Information

Split unit and annotation reliability.

## Implications for This Literature Review

Do not treat snippet AUC as patient-risk evidence.

## Recommended Follow-up

Cite for NLP feasibility with publication-status caution.
