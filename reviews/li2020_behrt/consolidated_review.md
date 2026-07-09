# Consolidated Review: li2020_behrt

## Consolidation Status
consolidated_complete

## One-Sentence Takeaway
li2020_behrt contributes longitudinal EHR representation background to the review, but its direct relevance to pre-cardiology cognitive-risk scoring depends on target, label, timing, and validation fit.

## Bottom Line for This Literature Review
Use this paper as background or methodological analogy rather than as a complete solution for the project.

## What This Paper Should Be Cited For
- longitudinal EHR representation background
- Relevant outline context where source-checked.

## What This Paper Should Not Be Cited For
- A complete pre-cardiology cognitive-risk model.
- A solved downstream-action-bias strategy.
- Cardiology-specific clinical utility unless source review later confirms it.

## Evidence Strength
- `useful_analogy`

## Key Contributions
BEHRT achieved absolute average-precision improvements of 8.0-10.8 percentage points compared with prior deep EHR models when predicting onset of 301 conditions.

## Key Limitations
Not extracted in this draft.

## Agreements Across Reviewers
All review passes agree that the paper should be used with scope limits and should not be overread as deployment-ready evidence for this project.

## Tensions or Disagreements Across Reviewers
No major internal disagreement in this generated review set. The main tension is between potential relevance to the outline and limited direct fit to the exact cardiology encounter-level task.

## Label, Target, and Timing Takeaways
Target/outcome: Onset prediction for 301 medical conditions.

Timing: index = Prediction points are based on patient EHR timelines and prior events.; observation = Longitudinal primary care and linked secondary care histories.; horizon = Future onset of 301 conditions.

## Validation and Transportability Takeaways
Average precision score for future disease prediction.

## Bias and Downstream-Action Takeaways
The paper does not resolve downstream-action or diagnosis-opportunity bias for this project unless later source review shows otherwise.

## Implications for Study Design
The paper informs the study design mainly through longitudinal EHR representation background. Any direct design adoption should be checked against the project's encounter-level index date and pre-index-only predictor rule.

## Claims to Carry Forward
- The paper is relevant to longitudinal EHR representation background.
- It may support the corresponding outline section after source-checking.

## Claims to Treat Cautiously
- Claims about clinical deployment, calibration, thresholds, or cardiology workflow.
- Claims about label validity if operational definitions are unclear.

## Open Questions
- Does the source document provide enough detail on labels, timing, validation, and implementation to support a strong manuscript claim?

## Recommended Next Action
Use this consolidated review to update `literature_review_state.md`; source-check before using the paper as a central citation.
