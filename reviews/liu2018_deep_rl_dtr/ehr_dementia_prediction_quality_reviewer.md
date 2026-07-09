# Specialist Review: EHR Dementia Prediction Quality

## Specialist Scope
Assessment of liu2018_deep_rl_dtr for EHR dementia/cognitive prediction quality and relevance to the pre-cardiology risk-scoring project.

## Bottom Line
background_only. This paper is not primarily an EHR dementia prediction paper and should be weighted accordingly.

## Prediction Task Clarity
Target from summary: Dynamic treatment policies with high expected reward, including survival and relapse-related reward structure.

## Index Date, Observation Window, and Prediction Horizon
Index: Transplant and subsequent treatment decision stages.

Observation window: Treatment decisions from initial conditioning and prophylaxis through acute and chronic GVHD treatment stages up to four years.

Horizon/follow-up: Four-year treatment-regime horizon after transplantation.

## Data Source and Cohort Definition
Center for International Blood and Marrow Transplant Research registry.

Population: 6,021 leukemia patients who underwent allogeneic hematopoietic cell transplantation.

## Outcome and Reference Standard
Dynamic treatment policies with high expected reward, including survival and relapse-related reward structure.

## Comparator or Control Group
Not fully assessed in this pass unless described above.

## EHR Text and Structured Data Use
Inputs: Patient clinical states, treatment histories, and high-dimensional treatment options.

## Missing Data and Feature Availability
Not fully assessed in this summary-grounded pass.

## Validation
Top-N expert-action prediction accuracy and expected reward under learned dynamic treatment regimes.

## Calibration, Thresholds, and Clinical Utility
The current summary does not establish cardiology-specific thresholds, calibration, or decision-curve utility unless explicitly noted in the evaluation section.

## Reporting and Reproducibility
Reproducibility should be source-checked before using this paper for strong claims.

## Care-Pathway and Downstream-Action Bias
Not resolved for this project by this paper.

## Implementation Readiness
No direct evidence of readiness for pre-cardiology cognitive-risk scoring unless explicitly stated in the summary.

## Strengths
- Relevant to dynamic treatment regime or reinforcement-learning background.
- Adds context to one or more outline sections.

## Concerns
- Direct fit to cardiology encounter-level scoring may be limited.
- Label, timing, validation, and actionability need source-level confirmation before strong citation.

## Missing Information
This is treatment-policy work rather than risk-score development.

## Implications for This Literature Review
Use this paper as background or analogy and avoid overclaiming clinical deployment relevance.

## Recommended Follow-up
Source-check this paper if it becomes central to a claim in the final review.
