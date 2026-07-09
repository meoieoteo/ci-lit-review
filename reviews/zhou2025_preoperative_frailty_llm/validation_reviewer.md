# Specialist Review: Validation

## Specialist Scope
Assessment of validation design, cross-label testing, calibration, and transportability.

## Bottom Line
`calibration_or_threshold_limited`. The cross-label validation is highly informative, but external validation and calibration are absent.

## Validation Design Summary
The study uses train/validation/test splits and cross-label testing between VES-13 and eFI datasets.

## Development and Validation Separation
Partial. Development and validation are separated within each dataset.

## Internal Validation
Strong within-label performance is reported for some models, especially RoBERTa trained and validated on VES-13.

## Temporal Validation
Not established.

## External Validation
Absent.

## Transportability
Limited by single-center spine-surgery population, anesthesia notes, and 512-token truncation.

## Calibration
Not reported.

## Thresholds and Operating Points
Frailty thresholds are defined for VES-13 and eFI, but clinical deployment thresholds for model outputs are not established.

## Clinical Utility
Not established beyond classification performance.

## Subgroup and Fairness Evaluation
Not a central extracted finding.

## Robustness and Sensitivity Analyses
Cross-label testing is a major robustness strength.

## Reporting Completeness
Adequate for model comparison, though deployment reproduction would require more preprocessing and hyperparameter detail.

## Reproducibility
Moderate. Model families and splits are described, but local notes and labels matter.

## Fit to Pre-Cardiology Risk Scoring
High methodological fit for label comparison; low direct deployment fit.

## Strengths
- Cross-label testing directly exposes construct mismatch.
- Multiple transformer models compared.
- Bootstrapped confidence intervals reported.

## Concerns
- No external validation.
- No calibration.
- Narrow population and note type.

## Missing Information
Calibration, external transport, demographic subgroup performance, and threshold utility.

## Implications for This Literature Review
Use as evidence that internal AUC can be misleading when the label construct is unstable.

## Recommended Follow-up
Apply the cross-label-testing idea to candidate dementia/cognitive labels in our study design.
