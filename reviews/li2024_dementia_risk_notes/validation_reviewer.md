# Specialist Review: Validation

## Specialist Scope

Validation design, calibration, transportability, reproducibility, and clinical-utility assessment for Li et al.'s notes-only dementia risk model.

## Bottom Line

The validation is useful for internal method comparison but insufficient for clinical deployment. The paper reports three-fold cross-validation and uncertainty across folds, but no external validation, calibration, temporal validation, real-prevalence PPV, or decision-curve analysis.

## Validation Design Summary

The paper uses three-fold cross-validation. It compares content-selection methods by feeding each selected text representation into the same Longformer classifier. Metrics include AUC, precision, sensitivity, specificity, F1, and accuracy.

## Development and Validation Separation

The proposed method separates supervised sentence selection on training data from unsupervised sentence selection for held-out patients. However, the paper does not fully specify whether all hyperparameter choices, threshold decisions, and content-selection settings were finalized without using validation results across multiple model comparisons.

## Internal Validation

Internal validation is the main evidence. Reported AUC for the proposed method was 78.43 with one-year observation, one-year horizon, and 1,024-token summaries; 77.15 with 4,096-token summaries in the same timing setting; and 80.34 to 81.64 for six-month horizons depending on observation period and token limit.

## Temporal Validation

No temporal validation is reported. The study does not test whether a model trained on earlier calendar years works in later years.

## External Validation

No external validation is reported. The data come from INPC, a multi-system regional EHR network, but validation remains internal to that data source.

## Transportability

Transportability is untested. The use of routine notes supports possible portability, but note templates, authoring practices, diagnosis coding, and availability of prior notes may differ materially across Epic instances or health systems.

## Calibration

Calibration is not reported. The model emits a dementia-risk score, but no calibration plot, calibration slope/intercept, Brier score, observed-to-expected ratio, or recalibration analysis is provided.

## Thresholds and Operating Points

The paper reports precision, sensitivity, specificity, F1, and accuracy at a binary threshold, but does not specify a clinically justified threshold or a threshold selected before final validation. The authors note that thresholds could be customized by disease prevalence and false-positive tolerance.

## Clinical Utility

Clinical utility is discussed conceptually for primary care, but not evaluated. No decision-curve analysis, workload estimate, referral-impact model, false-positive burden analysis, or prospective outcome analysis is reported for this model.

## Subgroup and Fairness Evaluation

No subgroup performance or calibration analysis is reported. This is a gap because dementia diagnosis opportunity and note documentation may vary by age, race, sex, access, and utilization.

## Robustness and Sensitivity Analyses

The paper varies observation period, prediction horizon, token limit, and content-selection method. These are meaningful sensitivity analyses for model design. It does not vary label definitions, outcome-code definitions, note-type inclusion, or prevalence assumptions.

## Reporting Completeness

Reporting is good for model architecture, content-selection process, and major performance tables. Reporting is incomplete for label operationalization, note-type/source metadata, exact index-date definition, patient-level split details across folds, missingness, and calibration.

## Reproducibility

The paper states that training and inference code are available under PDMlaboratory and that data are available from Regenstrief subject to restrictions and permission. The algorithm is described in detail, but full replication would still require restricted EHR data and missing cohort/label details.

## Fit to Pre-Cardiology Risk Scoring

The validation supports methodological plausibility for pre-encounter note-based risk scoring, not cardiology deployment. A cardiology model would need encounter-anchored validation, local calibration, natural-prevalence evaluation, and threshold analysis tied to cardiology actions.

## Strengths

- Patient-level note histories with explicit observation and horizon settings.
- Multiple content-selection baselines under the same classifier architecture.
- Fold-level standard deviations reported.
- Sensitivity to observation period, horizon, and token limit explored.

## Concerns

- Balanced case-control sample invalidates direct real-world PPV/workload interpretation.
- No external or temporal validation.
- No calibration.
- No subgroup analysis.
- No clinical utility analysis.

## Missing Information

- Split unit and safeguards against repeated-patient leakage across folds, beyond the patient-level framing.
- Full threshold-selection procedure.
- Natural-prevalence operating characteristics.
- Site-level performance within INPC.
- Calibration and subgroup performance.

## Implications for This Literature Review

This is a strong internal method-comparison paper for long-note content selection, but only moderate evidence for deployable dementia risk prediction. It should be paired with validation-quality caveats whenever cited.

## Recommended Follow-up

Before manuscript use, source-check the repository for code, cohort definitions, and any calibration or external validation not included in the article.
