# Specialist Review: Validation

## Specialist Scope
Assessment of validation, calibration, transportability, and implementation implications for the ClinicalBERT functional-status extraction study.

## Bottom Line
`externally_validated_but_incomplete`. The paper has useful validation across multiple sites in one health system, but not independent health-system validation or risk-score calibration.

## Validation Design Summary
The YNHH annotated set was split for training, validation, and internal testing. Northeast Medical Group and Greenwich Hospital samples served as additional validation sites.

## Development and Validation Separation
Adequate for a note-extraction study. The paper separates development and validation samples and includes two additional sites.

## Internal Validation
Strong discrimination was reported at the development site.

## Temporal Validation
Not a central design feature.

## External Validation
Partial. Additional sites are within the same health system, so this is stronger than random holdout but weaker than independent health-system validation.

## Transportability
Promising but uncertain. The approach depends on local cardiology documentation, note sections, annotation rules, and Epic-derived note structure.

## Calibration
Not reported. Less central for extraction than for risk scoring, but confidence calibration would matter if model outputs drive workflow.

## Thresholds and Operating Points
Operational thresholds are not the main reported contribution. Deployment yield is reported as added capture beyond explicit NYHA mentions.

## Clinical Utility
The paper demonstrates increased functional-status capture. It does not test downstream clinical outcomes or decision utility.

## Subgroup and Fairness Evaluation
AUROC was reported across race, sex, and ejection-fraction categories.

## Robustness and Sensitivity Analyses
Multi-site validation and deployment across unannotated notes are useful robustness signals.

## Reporting Completeness
Good for a clinical NLP extraction paper: note sections, model family, annotation approach, and interpretation methods are described.

## Reproducibility
Moderate. Reproduction would require local annotation, sectioning rules, and documentation-style validation.

## Fit to Pre-Cardiology Risk Scoring
Useful as validation precedent for note-derived concepts, not as evidence for cognitive-risk calibration or thresholds.

## Strengths
- Multi-site validation within outpatient cardiovascular care.
- Large deployment corpus.
- Clear comparison to explicit documentation.

## Concerns
- No independent health-system validation.
- No calibration.
- Extraction utility is not the same as risk-score utility.

## Missing Information
External transport to other health systems and calibration of model probabilities.

## Implications for This Literature Review
Supports local validation of cardiology-note concept extraction before incorporating note-derived concepts into a risk model.

## Recommended Follow-up
Use this as a template for validation of cognitive/functional/caregiver concept extraction from notes.
