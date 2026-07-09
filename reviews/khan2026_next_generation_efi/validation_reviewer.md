# Specialist Review: Validation

## Specialist Scope
Assessment of validation, calibration, transportability, and reproducibility for the next-generation eFI preprint.

## Bottom Line
`internally_validated_only`. The paper is promising but undervalidated for this project's purposes.

## Validation Design Summary
The NLP-NER extractors report F1 scores across deficit items. Outcome models use a 70/30 train-test split and compare eFI with HFRS and CCI.

## Development and Validation Separation
Partial. Train-test split supports internal validation, but external validation is absent.

## Internal Validation
Useful. Held-out test C-index and NLP F1 scores support internal performance.

## Temporal Validation
Not clearly established.

## External Validation
Not established.

## Transportability
Limited by Finnish healthcare data, language, documentation practices, and public-sector data environment.

## Calibration
Not clearly established from the summary.

## Thresholds and Operating Points
Frailty severity categories are used, but action-linked clinical thresholds for cardiology cognitive risk are not established.

## Clinical Utility
Associations with outcomes and utilization are reported, but clinical workflow utility is not tested.

## Subgroup and Fairness Evaluation
Not a central extracted finding.

## Robustness and Sensitivity Analyses
Comparisons against HFRS and CCI are useful, but not enough for external transport.

## Reporting Completeness
Partial. Supplementary extraction is needed for NLP-NER and count-model details.

## Reproducibility
Concept features are more reproducible than opaque embeddings, but local implementation would require terminology and NLP adaptation.

## Fit to Pre-Cardiology Risk Scoring
Useful for feature design, not direct validation of a cognitive-risk model.

## Strengths
- Large longitudinal cohort.
- Interpretable features.
- Structured plus text data.
- Comparator indices.

## Concerns
- Preprint.
- No independent external validation.
- Calibration and deployment thresholds not established.

## Missing Information
Full NLP training/validation details, calibration, subgroup performance, and transportability tests.

## Implications for This Literature Review
Use as support for concept extraction and frailty/cognitive-adjacent features, not for deployment-ready risk prediction.

## Recommended Follow-up
Source-check supplementary methods and monitor peer-review status.
