# Consolidated Review: janisch2020_costly_features

## Consolidation Status
consolidated_complete

## One-Sentence Takeaway
janisch2020_costly_features contributes sequential diagnosis, feature-acquisition, or decision-theoretic background to the review, but its direct relevance to pre-cardiology cognitive-risk scoring depends on target, label, timing, and validation fit.

## Bottom Line for This Literature Review
Use this paper as background or methodological analogy rather than as a complete solution for the project.

## What This Paper Should Be Cited For
- sequential diagnosis, feature-acquisition, or decision-theoretic background
- Relevant outline context where source-checked.

## What This Paper Should Not Be Cited For
- A complete pre-cardiology cognitive-risk model.
- A solved downstream-action-bias strategy.
- Cardiology-specific clinical utility unless source review later confirms it.

## Evidence Strength
- `useful_analogy`

## Key Contributions
The proposed method performs robustly across average budget, hard budget, and sparse/missing-feature settings, outperforming prior algorithms in the authors' experiments.

## Key Limitations
The authors note that theoretical guarantees are lost when using neural function approximation.

## Agreements Across Reviewers
All review passes agree that the paper should be used with scope limits and should not be overread as deployment-ready evidence for this project.

## Tensions or Disagreements Across Reviewers
No major internal disagreement in this generated review set. The main tension is between potential relevance to the outline and limited direct fit to the exact cardiology encounter-level task.

## Label, Target, and Timing Takeaways
Target/outcome: Correct class prediction while respecting feature acquisition cost/budget.

Timing: index = Not applicable.; observation = Not applicable.; horizon = Not applicable.

## Validation and Transportability Takeaways
Performance is evaluated across datasets and budget settings.

## Bias and Downstream-Action Takeaways
The paper does not resolve downstream-action or diagnosis-opportunity bias for this project unless later source review shows otherwise.

## Implications for Study Design
The paper informs the study design mainly through sequential diagnosis, feature-acquisition, or decision-theoretic background. Any direct design adoption should be checked against the project's encounter-level index date and pre-index-only predictor rule.

## Claims to Carry Forward
- The paper is relevant to sequential diagnosis, feature-acquisition, or decision-theoretic background.
- It may support the corresponding outline section after source-checking.

## Claims to Treat Cautiously
- Claims about clinical deployment, calibration, thresholds, or cardiology workflow.
- Claims about label validity if operational definitions are unclear.

## Open Questions
- Does the source document provide enough detail on labels, timing, validation, and implementation to support a strong manuscript claim?

## Recommended Next Action
Use this consolidated review to update `literature_review_state.md`; source-check before using the paper as a central citation.

## New Specialist Review Addendum
The new specialist reviews confirm no direct EHR text or schema contribution. The paper may later inform feature availability and acquisition-cost fields, but it should stay out of the first risk-score data-transformation and NLP sections.
