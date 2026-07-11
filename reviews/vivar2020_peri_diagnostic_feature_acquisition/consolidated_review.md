# Consolidated Review: vivar2020_peri_diagnostic_feature_acquisition

## Consolidation Status
consolidated_complete

## One-Sentence Takeaway
vivar2020_peri_diagnostic_feature_acquisition contributes sequential diagnosis, feature-acquisition, or decision-theoretic background to the review, but its direct relevance to pre-cardiology cognitive-risk scoring depends on target, label, timing, and validation fit.

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
The proposed approach is reported to be more cost- and feature-efficient than prior approaches while achieving higher overall accuracy.

## Key Limitations
The paper discusses limitations of prior RL and attribution approaches; detailed limitations of the proposed method are not extracted in this draft.

## Agreements Across Reviewers
All review passes agree that the paper should be used with scope limits and should not be overread as deployment-ready evidence for this project.

## Tensions or Disagreements Across Reviewers
No major internal disagreement in this generated review set. The main tension is between potential relevance to the outline and limited direct fit to the exact cardiology encounter-level task.

## Label, Target, and Timing Takeaways
Target/outcome: Accurate diagnosis with fewer or lower-cost acquired features.

Timing: index = The decision point is the current diagnostic state with partial features observed.; observation = Sequential acquisition during a diagnostic workflow.; horizon = Not a future prediction task; the target is diagnosis after feature acquisition.

## Validation and Transportability Takeaways
Accuracy and feature/cost efficiency on medical and synthetic datasets.

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
The new specialist reviews confirm no direct EHR text or schema role. The paper may later inform observed/missing/acquirable feature metadata and acquisition costs, but it is not part of the first EHR text or Epic pipeline argument.
