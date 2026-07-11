# Consolidated Review: amini2024_speech_ad_progression

## Consolidation Status
consolidated_complete

## One-Sentence Takeaway
amini2024_speech_ad_progression contributes dementia, MCI, or Alzheimer disease prediction evidence to the review, but its direct relevance to pre-cardiology cognitive-risk scoring depends on target, label, timing, and validation fit.

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
- `background_context`

## Key Contributions
The best model using text, demographics, APOE, and health factors achieved AUC 78.5 and F1 79.9. Text-only and text-plus-demographics models performed similarly. Traditional neuropsychological test scores had AUC 71.3, and MMSE had AUC 60.7.

## Key Limitations
The authors frame the work as an automated screening/prognosis approach requiring further development for remote and broad deployment.

## Agreements Across Reviewers
All review passes agree that the paper should be used with scope limits and should not be overread as deployment-ready evidence for this project.

## Tensions or Disagreements Across Reviewers
No major internal disagreement in this generated review set. The main tension is between potential relevance to the outline and limited direct fit to the exact cardiology encounter-level task.

## Label, Target, and Timing Takeaways
Target/outcome: Binary progression from MCI to AD within six years.

Timing: index = The neuropsychological test interview associated with MCI status is the time origin.; observation = The model uses speech from neuropsychological testing at baseline. Follow-up identifies progression over a six-year window.; horizon = Progression to AD within six years.

## Validation and Transportability Takeaways
Metrics included AUC, accuracy, sensitivity, precision, specificity, and F1 score.

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
The NLP/concept-extraction review treats this as cognitive-language evidence from speech transcripts, not routine EHR-note concept extraction. The EHR schema/CDM review adds that the Framingham speech and neuropsychological data structure has minimal direct relevance to Epic encounter-level transformation.
