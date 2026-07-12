# Specialist Review: Validation

## Specialist Scope

Validation design, calibration, thresholds, utility, and transportability.

## Bottom Line

internally_validated_only. Manual chart-review validation is valuable, but validation is small, single-system, and not external; calibration and net benefit are not established.

## Validation Design Summary

The model was trained on coded cases and matched controls, then applied to controls. Validation used dementia-specialist manual review of an initial 20 subjects and then 120 controls sampled across risk-score bins.

## Development and Validation Separation

Partial. The manual chart-review validation is separate from the weak-supervision training label, but the threshold estimation uses a modeled relationship from the stratified validation sample.

## Internal Validation

The paper reports chart-review-based ROC estimation among uncoded controls. It does not report conventional train/test or cross-validation performance for the logistic regression model in a way that fully separates feature/model development from validation.

## Temporal Validation

Not reported.

## External Validation

Not reported.

## Transportability

Limited. The setting is VA Puget Sound/VHA, with mostly male older Veterans and VHA-specific note types and coding practices.

## Calibration

Not reported as standard risk-score calibration. The paper fits a linear relationship between score bins and estimated undiagnosed dementia rates, but this is not a full calibration assessment.

## Thresholds and Operating Points

Thresholds are reported. A threshold of 0.061 had sensitivity and specificity around 0.825 and 0.832; other thresholds traded sensitivity and specificity.

## Clinical Utility

The paper proposes targeted clinical assessment for high-risk patients but does not evaluate net benefit, workload, acceptability, or downstream outcomes.

## Subgroup and Fairness Evaluation

Not reported. The authors note limited generalizability to women because the cohort is mostly male.

## Robustness and Sensitivity Analyses

The unclear validation category is handled under two assumptions. Broader sensitivity analyses for windows, feature sets, or labels are not reported.

## Reporting Completeness

Adequate for high-level understanding; incomplete for reimplementation. The paper reports cohort definitions, time windows, broad feature types, and thresholds, but not enough feature/model detail for direct external reproduction.

## Reproducibility

Partial. LDA/stable-topic methods are described, but exact topic models, code, feature lists, and coefficients are not fully available in the main paper.

## Fit to Pre-Cardiology Risk Scoring

Useful design analogue but not deployment evidence. It does not validate a score at the cardiology encounter or tie thresholds to cardiology actions.

## Strengths

- Manual specialist review of uncoded patients.
- Threshold performance reported.
- Explicitly acknowledges weak labels.

## Concerns

- No external validation.
- No calibration or net-benefit analysis.
- Small validation sample relative to intended case-finding use.

## Missing Information

- Patient-independent split details for model development.
- Calibration plot/intercept/slope.
- Implementation workload at chosen thresholds.

## Implications for This Literature Review

Use as moderate evidence that structured-plus-note features can support undiagnosed dementia case finding, not as proof of clinical readiness.

## Recommended Follow-up

Extract exact validation-sample design and threshold details if citing performance numbers.
