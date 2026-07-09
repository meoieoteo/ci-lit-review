# Specialist Review: EHR Dementia Prediction Quality

## Specialist Scope
Direct application of the EHR dementia prediction quality reviewer to Lu et al. 2026.

## Bottom Line
`label_or_validation_limited`. This review is the central quality-warning paper for EHR dementia prediction.

## Prediction Task Clarity
The paper's critique is that many included studies do not clearly distinguish diagnostic detection, unrecognized current dementia, known dementia, and future dementia risk.

## Index Date, Observation Window, and Prediction Horizon
Weak across the included literature. Index dates, observation windows, and prediction horizons are often unclear or inconsistently reported.

## Data Source and Cohort Definition
The included models use routine EHR data from heterogeneous clinical populations, often single-country datasets. Cohort construction is frequently underreported or weak.

## Outcome and Reference Standard
Outcome definitions are a major weakness. Many studies use diagnosis codes, medication codes, rule-based definitions, specialist clinic codes, chart review, or ML labels. Only a small minority use established clinical diagnostic criteria.

## Comparator or Control Group
Frequently concerning because patients without dementia codes may not be true negatives.

## EHR Text and Structured Data Use
Most models use structured data only. Unstructured text is promising but underused and not yet shown to solve clinical deployment problems.

## Missing Data and Feature Availability
Missing data and feature availability are part of the broader reporting and analysis concerns.

## Validation
External validation is uncommon. Only 47 of 434 developed models were externally validated.

## Calibration, Thresholds, and Clinical Utility
Calibration and thresholds are sparse. AUROC dominates reporting and is insufficient for clinical decision support.

## Reporting and Reproducibility
Poor reporting limits reuse, bias assessment, and implementation.

## Care-Pathway and Downstream-Action Bias
Diagnosis-code outcomes may reflect recognition, referral, access, documentation, and coding rather than cognitive state alone.

## Implementation Readiness
Not ready. The review reports no clear path to routine clinical implementation for most models.

## Strengths
- Directly relevant systematic review.
- Large model count.
- Uses CHARMS, TRIPOD+AI, and PROBAST.
- Highlights target, label, calibration, and validation weaknesses.

## Concerns
- Heterogeneity prevents formal meta-analysis.
- Findings depend on published reporting quality.
- Does not provide an operational label solution.

## Missing Information
Supplementary extraction is needed for model-level details, especially unstructured-note models.

## Implications for This Literature Review
This paper should anchor our quality checklist and motivate the project's methodological contribution.

## Recommended Follow-up
Use it with John et al. for validation/reporting and with Zhou et al. for label-construct concerns.
