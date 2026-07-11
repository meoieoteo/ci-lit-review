# Consolidated Review: pellegrini2018_neuroimaging_ml_review

## Consolidation Status
consolidated_complete

## One-Sentence Takeaway
pellegrini2018_neuroimaging_ml_review contributes dementia, MCI, or Alzheimer disease prediction evidence to the review, but its direct relevance to pre-cardiology cognitive-risk scoring depends on target, label, timing, and validation fit.

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
Most studies assessed AD versus healthy controls, used ADNI, support vector machines, and T1-weighted MRI. Accuracy was highest for AD versus healthy controls and poorer for healthy control versus MCI versus AD and MCI converter versus non-converter tasks. Combined data types improved accuracy more than sample size, data source, or ML method.

## Key Limitations
The authors conclude that machine learning did not yet differentiate clinically relevant disease categories sufficiently and called for more diverse datasets, multimodal data, and clinical integration.

## Agreements Across Reviewers
All review passes agree that the paper should be used with scope limits and should not be overread as deployment-ready evidence for this project.

## Tensions or Disagreements Across Reviewers
No major internal disagreement in this generated review set. The main tension is between potential relevance to the outline and limited direct fit to the exact cardiology encounter-level task.

## Label, Target, and Timing Takeaways
Target/outcome: Diagnostic categories spanning healthy aging, MCI, and dementia.

Timing: index = Varied by included study.; observation = Varied by included study.; horizon = Varied; some studies considered MCI converter versus non-converter classification.

## Validation and Transportability Takeaways
Reported accuracy across included studies.

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
The new specialist reviews confirm no direct EHR NLP or schema role. The paper should be used only as AD/MCI neuroimaging ML background and as contrast with routine EHR-based prediction.
