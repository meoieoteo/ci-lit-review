# Consolidated Review: grueso2021_mci_ad_ml_review

## Consolidation Status
consolidated_complete

## One-Sentence Takeaway
grueso2021_mci_ad_ml_review contributes dementia, MCI, or Alzheimer disease prediction evidence to the review, but its direct relevance to pre-cardiology cognitive-risk scoring depends on target, label, timing, and validation fit.

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
Of 116 reviewed studies, most used ADNI data, MRI, and SVM. SVM had mean accuracy around 75.4%, while convolutional neural networks had mean accuracy around 78.5%. MRI plus PET studies generally performed better than single-modality studies.

## Key Limitations
The review highlights concerns about generalizability, heavy reliance on ADNI, and clinically relevant prediction remaining difficult.

## Agreements Across Reviewers
All review passes agree that the paper should be used with scope limits and should not be overread as deployment-ready evidence for this project.

## Tensions or Disagreements Across Reviewers
No major internal disagreement in this generated review set. The main tension is between potential relevance to the outline and limited direct fit to the exact cardiology encounter-level task.

## Label, Target, and Timing Takeaways
Target/outcome: Stable MCI versus progressive MCI / conversion to AD dementia.

Timing: index = Varied by included study, usually baseline MCI assessment.; observation = Varied by included study; the review notes follow-up definitions such as three years for ADNI and one year for AddNeuroMed in some contexts.; horizon = Progression from MCI to AD dementia during study-specific follow-up periods.

## Validation and Transportability Takeaways
The review reports accuracy and AUC where available.

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
