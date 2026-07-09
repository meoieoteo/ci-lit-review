# Specialist Review: EHR Dementia Prediction Quality

## Specialist Scope
Assessment of grammenos2024_explainable_mci_ad for EHR dementia/cognitive prediction quality and relevance to the pre-cardiology risk-scoring project.

## Bottom Line
methodologically_informative. This paper is relevant to dementia or cognitive prediction and should be weighted accordingly.

## Prediction Task Clarity
Target from summary: Stable MCI versus MCI transition to Alzheimer disease.

## Index Date, Observation Window, and Prediction Horizon
Index: Baseline ADNI visit.

Observation window: Longitudinal data from baseline through follow-up visits, including a 48-month observation framing in the methods.

Horizon/follow-up: The abstract describes a 36-month prediction period; the introduction and methods also discuss 48-month transition framing.

## Data Source and Cohort Definition
ADNIMERGE data from ADNI phases ADNI1, ADNI2, ADNI3, and ADNI-GO.

Population: The paper describes an initial ADNI dataset of 2378 participants and a modeled MCI cohort with stable and transition groups after preprocessing.

## Outcome and Reference Standard
Stable MCI versus MCI transition to Alzheimer disease.

## Comparator or Control Group
Not fully assessed in this pass unless described above.

## EHR Text and Structured Data Use
Inputs: ADNI clinical, cognitive, imaging, genetic, biomarker, and demographic variables available in ADNIMERGE.

## Missing Data and Feature Availability
Not fully assessed in this summary-grounded pass.

## Validation
Five-fold cross-validation is reported with precision, recall, F1, accuracy, and ROC AUC.

## Calibration, Thresholds, and Clinical Utility
The current summary does not establish cardiology-specific thresholds, calibration, or decision-curve utility unless explicitly noted in the evaluation section.

## Reporting and Reproducibility
Reproducibility should be source-checked before using this paper for strong claims.

## Care-Pathway and Downstream-Action Bias
Not resolved for this project by this paper.

## Implementation Readiness
No direct evidence of readiness for pre-cardiology cognitive-risk scoring unless explicitly stated in the summary.

## Strengths
- Relevant to dementia, MCI, or Alzheimer disease prediction evidence.
- Adds context to one or more outline sections.

## Concerns
- Direct fit to cardiology encounter-level scoring may be limited.
- Label, timing, validation, and actionability need source-level confirmation before strong citation.

## Missing Information
The paper uses both 36-month and 48-month language. A later review should reconcile the exact target horizon from the methods and cohort construction.

## Implications for This Literature Review
Use this paper as direct dementia/cognitive prediction context and avoid overclaiming clinical deployment relevance.

## Recommended Follow-up
Source-check this paper if it becomes central to a claim in the final review.
