# Consolidated Review: benmiled2023_dementia_notes

## Consolidation Status

consolidated_complete

## One-Sentence Takeaway

Ben Miled 2023 supports one-year dementia prediction from note-derived UMLS concepts, but its external-institution results show that portability is fragile.

## Bottom Line for This Literature Review

This is direct evidence for clinical-note dementia signal and one of the clearest warnings that EHR text models require local validation.

## What This Paper Should Be Cited For

`ehr_text_signal`; `note_concept_extraction`; `dementia_prediction_performance`; `implementation_or_transportability`

## What This Paper Should Not Be Cited For

Do not cite it as evidence that dementia note models generalize across institutions without validation.

## Publication Status and Evidence Weight

Peer-reviewed direct evidence with moderate weight; transportability and case-control label limitations reduce its strength for deployment claims.

## Evidence Strength

`moderate_direct_evidence`; `methodological_caution`

## Key Contributions

One-year horizon, final-year note exclusion, comparison of embeddings versus UMLS concepts, and external institution testing.

## Key Limitations

External degradation, uncertain calibration, matched case-control design, and diagnosis-code label dependence.

## Agreements Across Reviewers

All reviewers agree the paper is direct and useful but dominated by transportability cautions.

## Tensions or Disagreements Across Reviewers

No major disagreement.

## Label, Target, and Timing Takeaways

The one-year prediction gap is a useful leakage-control precedent, but future coded diagnosis remains care-pathway dependent.

## Validation and Transportability Takeaways

External testing is the major contribution because it shows performance loss.

## Bias and Downstream-Action Takeaways

Diagnosis opportunity remains a threat to interpreting incident dementia labels.

## Implications for Study Design

Plan local validation and possibly recalibration for every note-feature representation, even when using UMLS concepts.

## Claims to Carry Forward

Medical notes can support one-year dementia prediction; UMLS concept features may be useful.

## Claims to Treat Cautiously

Internal performance does not imply cross-institution performance.

## Open Questions

Which concept features failed to transport, and why?

## Recommended Next Action

Use for direct evidence and transportability caution in the review.
