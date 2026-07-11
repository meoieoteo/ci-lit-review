# Consolidated Review: grammenos2024_explainable_mci_ad

## Consolidation Status
consolidated_complete

## One-Sentence Takeaway
grammenos2024_explainable_mci_ad contributes dementia, MCI, or Alzheimer disease prediction evidence to the review, but its direct relevance to pre-cardiology cognitive-risk scoring depends on target, label, timing, and validation fit.

## Bottom Line for This Literature Review
Use this paper as a dementia/cognitive prediction reference rather than as a complete solution for the project.

## What This Paper Should Be Cited For
- dementia, MCI, or Alzheimer disease prediction evidence
- Relevant outline context where source-checked.

## What This Paper Should Not Be Cited For
- A complete pre-cardiology cognitive-risk model.
- A solved downstream-action-bias strategy.
- Cardiology-specific clinical utility unless source review later confirms it.

## Evidence Strength
- `moderate_direct_evidence`

## Key Contributions
The reported average accuracy is 0.85 and ROC AUC is 0.86. Stable class precision/recall/F1 were 0.94/0.84/0.90, and transition class precision/recall/F1 were 0.71/0.88/0.79.

## Key Limitations
Not extracted in detail in this draft.

## Agreements Across Reviewers
All review passes agree that the paper should be used with scope limits and should not be overread as deployment-ready evidence for this project.

## Tensions or Disagreements Across Reviewers
No major internal disagreement in this generated review set. The main tension is between potential relevance to the outline and limited direct fit to the exact cardiology encounter-level task.

## Label, Target, and Timing Takeaways
Target/outcome: Stable MCI versus MCI transition to Alzheimer disease.

Timing: index = Baseline ADNI visit.; observation = Longitudinal data from baseline through follow-up visits, including a 48-month observation framing in the methods.; horizon = The abstract describes a 36-month prediction period; the introduction and methods also discuss 48-month transition framing.

## Validation and Transportability Takeaways
Five-fold cross-validation is reported with precision, recall, F1, accuracy, and ROC AUC.

## Bias and Downstream-Action Takeaways
The paper does not resolve downstream-action or diagnosis-opportunity bias for this project unless later source review shows otherwise.

## Implications for Study Design
The paper informs the study design mainly through dementia, MCI, or Alzheimer disease prediction evidence. Any direct design adoption should be checked against the project's encounter-level index date and pre-index-only predictor rule.

## Claims to Carry Forward
- The paper is relevant to dementia, MCI, or Alzheimer disease prediction evidence.
- It may support the corresponding outline section after source-checking.

## Claims to Treat Cautiously
- Claims about clinical deployment, calibration, thresholds, or cardiology workflow.
- Claims about label validity if operational definitions are unclear.

## Open Questions
- Does the source document provide enough detail on labels, timing, validation, and implementation to support a strong manuscript claim?

## Recommended Next Action
Use this consolidated review to update `literature_review_state.md`; source-check before using the paper as a central citation.

## New Specialist Review Addendum
The new specialist reviews narrow the paper's contribution to cognitive-prediction context. It does not inform EHR note concept extraction or Epic/CDM data transformation because ADNI/ADNIMERGE variables are standardized research data rather than operational cardiology EHR data.
