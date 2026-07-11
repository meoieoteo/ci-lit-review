# Consolidated Review: rasmy2021_medbert

## Consolidation Status
consolidated_complete

## One-Sentence Takeaway
rasmy2021_medbert contributes longitudinal EHR representation background to the review, but its direct relevance to pre-cardiology cognitive-risk scoring depends on target, label, timing, and validation fit.

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
Med-BERT improved AUC by 2.67-3.92%, 3.20-7.12%, and 2.02-4.71% across cohorts compared with GRU, Bi-GRU, and RETAIN. It was especially helpful with 300-500 fine-tuning samples.

## Key Limitations
Not extracted in this draft.

## Agreements Across Reviewers
All review passes agree that the paper should be used with scope limits and should not be overread as deployment-ready evidence for this project.

## Tensions or Disagreements Across Reviewers
No major internal disagreement in this generated review set. The main tension is between potential relevance to the outline and limited direct fit to the exact cardiology encounter-level task.

## Label, Target, and Timing Takeaways
Target/outcome: Disease-prediction outcomes for heart failure and pancreatic cancer.

Timing: index = Varied by downstream disease-prediction task.; observation = Longitudinal EHR diagnosis histories before prediction.; horizon = Varied by task; evaluated tasks included heart failure in patients with diabetes and pancreatic cancer prediction.

## Validation and Transportability Takeaways
AUC improvement across three fine-tuning cohorts and experiments with small training sample sizes.

## Bias and Downstream-Action Takeaways
The paper does not resolve downstream-action or diagnosis-opportunity bias for this project unless later source review shows otherwise.

## Implications for Study Design
The paper informs the study design mainly through longitudinal EHR representation background. It is relevant to structured visit/code sequence modeling, not to fixed-vector tabular baselines or note-text extraction. Any direct design adoption should be checked against the project's encounter-level index date and pre-index-only predictor rule.

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

## New Specialist Review Addendum
The NLP/concept-extraction review clarifies that Med-BERT is structured-code sequence modeling, not note extraction. The EHR schema/CDM review strengthens its role as a structured longitudinal representation source, while warning that diagnosis-code absence, visit grouping, and pre-index sequence construction must be handled explicitly. The summary backfill adds that it should be treated as a variable-length visit/code sequence model, with irregular-time handling still requiring source checking.
