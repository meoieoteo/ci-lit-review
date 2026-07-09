# Specialist Review: EHR Dementia Prediction Quality

## Specialist Scope
Assessment of vivar2020_peri_diagnostic_feature_acquisition for EHR dementia/cognitive prediction quality and relevance to the pre-cardiology risk-scoring project.

## Bottom Line
background_only. This paper is not primarily an EHR dementia prediction paper and should be weighted accordingly.

## Prediction Task Clarity
Target from summary: Accurate diagnosis with fewer or lower-cost acquired features.

## Index Date, Observation Window, and Prediction Horizon
Index: The decision point is the current diagnostic state with partial features observed.

Observation window: Sequential acquisition during a diagnostic workflow.

Horizon/follow-up: Not a future prediction task; the target is diagnosis after feature acquisition.

## Data Source and Cohort Definition
Two public medical datasets and two synthetic datasets.

Population: Not a single clinical cohort; public medical datasets are used for evaluation.

## Outcome and Reference Standard
Accurate diagnosis with fewer or lower-cost acquired features.

## Comparator or Control Group
Not fully assessed in this pass unless described above.

## EHR Text and Structured Data Use
Inputs: Partially observed feature vectors and feature costs.

## Missing Data and Feature Availability
Not fully assessed in this summary-grounded pass.

## Validation
Accuracy and feature/cost efficiency on medical and synthetic datasets.

## Calibration, Thresholds, and Clinical Utility
The current summary does not establish cardiology-specific thresholds, calibration, or decision-curve utility unless explicitly noted in the evaluation section.

## Reporting and Reproducibility
Reproducibility should be source-checked before using this paper for strong claims.

## Care-Pathway and Downstream-Action Bias
Not resolved for this project by this paper.

## Implementation Readiness
No direct evidence of readiness for pre-cardiology cognitive-risk scoring unless explicitly stated in the summary.

## Strengths
- Relevant to sequential diagnosis, feature-acquisition, or decision-theoretic background.
- Adds context to one or more outline sections.

## Concerns
- Direct fit to cardiology encounter-level scoring may be limited.
- Label, timing, validation, and actionability need source-level confirmation before strong citation.

## Missing Information
This paper is about within-diagnostic feature acquisition, not pre-encounter risk scoring.

## Implications for This Literature Review
Use this paper as background or analogy and avoid overclaiming clinical deployment relevance.

## Recommended Follow-up
Source-check this paper if it becomes central to a claim in the final review.
