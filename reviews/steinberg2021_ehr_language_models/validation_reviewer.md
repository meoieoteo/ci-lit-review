# Specialist Review: Validation

## Specialist Scope

Validation design and reporting for Steinberg et al.'s structured-EHR representation-learning experiments.

## Bottom Line

The validation design is methodologically useful because it uses temporal splits and strong baselines. It remains insufficient for clinical utility claims because calibration, thresholds, clinical actions, and external validation are absent.

## Validation Design Summary

Data through December 31, 2015 were used for training, January 1, 2016 through July 1, 2016 for development, and August 1, 2016 through August 1, 2017 for held-out testing.

## Development and Validation Separation

Training, development, and held-out test periods are separated by calendar time. Hyperparameter tuning uses the development period; final evaluation uses held-out test data.

## Internal Validation

The study includes held-out temporal internal validation within one institutional data environment.

## Temporal Validation

Temporal validation is a strength of the paper.

## External Validation

No external site validation is performed.

## Transportability

Untested. The authors explicitly state that cross-institution generalization of CLMBR representations was not explored.

## Calibration

Calibration is not reported.

## Thresholds and Operating Points

Thresholds and operating points are not clinically analyzed.

## Clinical Utility

No clinical utility, decision curve, net benefit, or workflow evaluation is reported.

## Subgroup and Fairness Evaluation

Not reported.

## Robustness and Sensitivity Analyses

The paper varies representation method, downstream model class, training sample size, and language-model objective. These are strong methodological sensitivity analyses.

## Reporting Completeness

Good for representation methodology, hyperparameter grids, and AUROC comparisons. Limited for calibration and implementation utility.

## Reproducibility

The paper reports an OHDSI-compatible CLMBR implementation in `ehr_ml.clmbr`, which is useful for reproducibility.

## Fit to Pre-Cardiology Risk Scoring

Useful for designing a structured baseline and learned representation comparison; not sufficient for clinical validation of a cardiology cognitive-risk score.

## Strengths

- Temporal split.
- Multiple strong baselines.
- Subsampling experiments.
- Bootstrap uncertainty estimates.
- Open-source implementation note.

## Concerns

- No external validation.
- No calibration.
- No threshold or utility analysis.
- Outcomes differ from this project's target.

## Missing Information

Subgroup performance, calibration, and site transportability.

## Implications for This Literature Review

Use as validation-design context for structured representation methods, especially the importance of comparing against count-based gradient-boosting baselines.

## Recommended Follow-up

When designing local experiments, include CLMBR-like representation only after a strong structured baseline is implemented.
