# Specialist Review: Validation

## Specialist Scope

Validation design, site testing, calibration, clinical utility, and reproducibility for Wei et al.

## Bottom Line

Validation is stronger than many single-site phenotyping studies because it includes two institutions, nested cross-validation, bootstrap confidence intervals, site train/test experiments, and error analysis. It remains limited by same-region sites, no calibration, no external validation beyond Boston, and enriched sampling.

## Validation Design Summary

The paper reports five-fold stratified nested cross-validation, grid-search hyperparameter tuning, 1,000 bootstrap iterations for confidence intervals, and site train/test experiments across MGH and BIDMC.

## Development and Validation Separation

Nested cross-validation supports separation of model selection and performance estimation. Site experiments provide additional generalizability checks.

## Internal Validation

Strong internal validation. In combined MGH+BIDMC data, logistic regression with ICD+medication+note features achieved AUROC 0.97 and AUPRC 0.97.

## Temporal Validation

No explicit temporal validation is reported.

## External Validation

Site transfer between MGH and BIDMC is useful but not full external validation because both are Boston-area academic medical centers.

## Transportability

Transportability is partly tested across two institutions, but the authors note geographic and EHR-format limitations. Performance was lower on BIDMC test data than MGH test data.

## Calibration

Calibration is not reported.

## Thresholds and Operating Points

Classification metrics are reported, but no clinically justified threshold or workload analysis is provided.

## Clinical Utility

The paper frames the model for large-scale research phenotyping. It does not evaluate clinical workflow utility, decision support, or patient outcome effects.

## Subgroup and Fairness Evaluation

The paper reports performance across MED/ICD sampling strata but not demographic subgroup performance or calibration.

## Robustness and Sensitivity Analyses

Robustness analyses include input-ablation comparisons, model-class comparisons, site experiments, and random-sample error estimation.

## Reporting Completeness

Good for features, ICD categories, medications, metrics, and site experiments. Less complete for chart-review reliability, calibration, and date-range consistency.

## Reproducibility

The paper reports data/code availability URLs and gives code/medication groups. Reuse requires checking repository contents and local EHR mapping.

## Fit to Pre-Cardiology Risk Scoring

Useful as a phenotyping validation model, not as validation of future pre-cardiology risk scoring.

## Strengths

- Manual chart-review labels.
- Two-site experiments.
- Confidence intervals.
- Error analysis.
- Notes-only and structured-only comparisons.

## Concerns

- No calibration.
- Enriched sample.
- Same-region sites.
- Uncertain cases excluded.
- No demographic fairness evaluation.

## Missing Information

Inter-rater reliability, calibration, threshold selection, and source-date discrepancy resolution.

## Implications for This Literature Review

Use Wei as stronger direct evidence for note-enhanced MCI/ADRD phenotyping, with caveats about validation scope and ambiguous cases.

## Recommended Follow-up

Source-check repository and consider adopting its four-stratum sampling logic for local chart-review validation.
