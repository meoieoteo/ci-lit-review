# Consolidated Review: lu2026_ehr_dementia_prediction_review

## Consolidation Status
consolidated_complete

## One-Sentence Takeaway
Lu et al. shows that EHR dementia prediction is promising but clinically immature because target definitions, labels, calibration, validation, and reporting are often weak.

## Bottom Line for This Literature Review
This is one of the central anchor papers. It should frame the review's main methodological claim: the hard part is not choosing a newer model, but defining the target, labels, timing, validation, and care-pathway bias carefully.

## What This Paper Should Be Cited For
- `problem_framing`
- `target_definition`
- `label_construction`
- `validation_quality`
- `calibration_or_thresholding`
- `downstream_action_bias`
- `ehr_text_signal`

## What This Paper Should Not Be Cited For
- A deployable dementia prediction model.
- Proof that unstructured text outperforms structured data.
- A cardiology-specific workflow solution.
- An operational recipe for downstream-action-adjusted labels.

## Evidence Strength
- `strong_direct_evidence` for field-level quality gaps.
- `methodological_caution` for target, label, validation, and implementation risks.

## Key Contributions
- Reviews 56 studies and 434 developed models.
- Shows weak reference standards and unclear target definitions.
- Shows sparse calibration and external validation.
- Undercuts architecture-first framing by finding no clear internal AUROC advantage for AI methods.

## Key Limitations
- Heterogeneous literature prevents meta-analysis.
- Dependent on incomplete published reporting.
- Does not solve label construction or cardiology deployment.

## Agreements Across Reviewers
All reviews agree this is a design-constraint paper, not a source of deployable model evidence.

## Tensions or Disagreements Across Reviewers
No major disagreement. The only caution is that broad review counts should not be overinterpreted as model-level conclusions without supplementary extraction.

## Label, Target, and Timing Takeaways
The field often collapses known dementia, unrecognized current dementia, and future dementia diagnosis. Our project must not.

## Validation and Transportability Takeaways
External validation, calibration, thresholds, and reporting are insufficient in the field and must be designed from the start.

## Bias and Downstream-Action Takeaways
Diagnosis-code labels can reflect referral, testing, documentation, coding, and specialist access.

## Implications for Study Design
The study should anchor rows at cardiology encounter start, use only pre-index predictors, define labels and outcome windows explicitly, and pre-plan calibration and validation.

## Claims to Carry Forward
- EHR dementia prediction models are often high risk of bias.
- AUROC is insufficient for clinical decision support.
- Better target and label design may be a more important contribution than algorithm novelty.

## Claims to Treat Cautiously
- Any claim about the superiority of a specific unstructured-text method from this review alone.
- Any claim that current EHR dementia models are ready for cardiology deployment.

## Open Questions
- Which unstructured-note dementia models in the supplement deserve direct review?
- What label strategy best avoids diagnosis-opportunity bias?

## Recommended Next Action
Use this paper as the core quality anchor in the state file and cross-paper synthesis.
