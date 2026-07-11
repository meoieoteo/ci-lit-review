# Consolidated Review: zhou2025_preoperative_frailty_llm

## Consolidation Status
consolidated_complete

## One-Sentence Takeaway
Zhou et al. shows that transformer performance depends strongly on whether frailty is labeled by patient questionnaire or EHR-derived index, making it a key warning for cognitive-risk label design.

## Bottom Line for This Literature Review
This paper should be cited primarily for label construct risk and cross-label validation, not for architecture choice or deployment readiness.

## What This Paper Should Be Cited For
- `label_construction`
- `note_concept_extraction`
- `validation_quality`
- `methodological_caution`

## What This Paper Should Not Be Cited For
- Dementia prediction.
- Cardiology workflow.
- External validation.
- Calibrated clinical thresholds.

## Evidence Strength
- `useful_analogy`
- `methodological_caution`

## Key Contributions
- Compares VES-13 and eFI labels.
- Shows asymmetric cross-label transfer.
- Demonstrates that label choice changes what text models learn.

## Key Limitations
- Frailty rather than cognition.
- Single-center surgical cohort.
- No external validation or calibration.
- Token truncation and note-type specificity.

## Agreements Across Reviewers
All reviews agree the label-source lesson is the main contribution.

## Tensions or Disagreements Across Reviewers
No major disagreement. The paper is strong as analogy but weak as direct evidence.

## Label, Target, and Timing Takeaways
Operational labels can encode different constructs even when they share the same clinical name.

## Validation and Transportability Takeaways
Cross-label testing is valuable; external transport is not established.

## Bias and Downstream-Action Takeaways
EHR-derived labels may reflect documentation and testing opportunity.

## Implications for Study Design
Candidate cognitive labels should be compared against each other before model development.

## Claims to Carry Forward
- Label source can dominate model behavior.
- Cross-label validation can reveal construct mismatch.

## Claims to Treat Cautiously
- That a high AUC means the model captures the intended clinical state.
- That EHR-derived proxy labels are interchangeable with direct clinical assessments.

## Open Questions
- Which cognitive labels should be cross-tested in our data?

## Recommended Next Action
Use this paper in the label-definition section and in study-design discussions about candidate labels.

## New Specialist Review Addendum
The NLP/concept-extraction review strengthens this paper as a warning against treating direct transformer note classification as interpretable concept extraction. The EHR schema/CDM review adds that the VES-13 versus eFI contrast is a schema and provenance lesson: every candidate label needs source, evidence date, and construct class recorded.
