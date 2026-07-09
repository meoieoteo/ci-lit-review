# Specialist Review: Validation

## Specialist Scope
Assessment of validation design, transportability, calibration, reporting, and reproducibility in John et al. 2022.

## Bottom Line
`externally_validated_but_incomplete`. The paper is one of the most important validation references in the current review, but it mainly shows that external validation is often blocked by incomplete reporting.

## Validation Design Summary
The paper reviews published dementia prediction models for external-validatability and externally validates selected models using observational health data mapped to OMOP CDM.

## Development and Validation Separation
adequate for the external validation of selected existing models. The validated models were developed elsewhere and tested in observational databases.

## Internal Validation
not_applicable as the main contribution; the paper validates existing models rather than developing new ones.

## Temporal Validation
not_reported in the current summary.

## External Validation
adequate and central. This is the key paper for showing both the value and difficulty of external validation.

## Transportability
strong direct relevance. Walters and Nori transported reasonably to some databases, but model portability varied and could be limited by incomplete reporting and database differences.

## Calibration
partial. Calibration is considered, but recalibration can be impossible when original model details such as baseline hazard are missing.

## Thresholds and Operating Points
not_reported in the current summary. The paper is stronger for validation feasibility than threshold policy.

## Clinical Utility
weak for direct clinical utility. The paper does not define cardiology actions or decision thresholds.

## Subgroup and Fairness Evaluation
not_reported in the current summary.

## Robustness and Sensitivity Analyses
partial. External validation across databases is a robustness strength, but the summary does not provide details on sensitivity analyses.

## Reporting Completeness
strong. Reporting completeness is the central contribution.

## Reproducibility
strong. The paper highlights that full model specification, index date, predictor window, and time-at-risk are necessary for reproducibility.

## Fit to Pre-Cardiology Risk Scoring
High methodological fit. Our study should be designed so another group could externally validate the model from the report.

## Strengths
- Direct external validation focus.
- Common-data-model orientation.
- Concrete reporting-gap findings.

## Concerns
- Not cardiology-specific.
- Not text-based.
- Does not directly test clinical utility.

## Missing Information
- Exact database-level performance details from the current summary.
- Threshold and net-benefit analyses.
- Subgroup calibration.

## Implications for This Literature Review
This paper should be cited for why external validation, complete reporting, and recalibration details must be designed in from day one.

## Recommended Follow-up
- Prioritize this paper in the validation section.
- Use it to update the study-design template's reporting checklist.
