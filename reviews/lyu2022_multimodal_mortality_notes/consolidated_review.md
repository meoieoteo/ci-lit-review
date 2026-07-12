# Consolidated Review: lyu2022_multimodal_mortality_notes

## Consolidation Status

consolidated_complete

## One-Sentence Takeaway

Lyu 2022 is a multimodal transformer methods citation for ICU mortality, not dementia or cardiology evidence.

## Bottom Line for This Literature Review

Use only for background on fusing structured time series and note embeddings with interpretation methods.

## What This Paper Should Be Cited For

`longitudinal_ehr_modeling`; `ehr_text_signal`; `background_only`

## What This Paper Should Not Be Cited For

Do not cite for dementia labels, cognitive note concepts, or clinical utility in cardiology.

## Publication Status and Evidence Weight

Conference/preprint-style methods work with indirect relevance.

## Evidence Strength

`useful_analogy`; `background_context`; `lower_publication_weight`

## Key Contributions

Multimodal transformer fusion, first-48-hour window, held-out test performance, integrated gradients/Shapley interpretation.

## Key Limitations

ICU mortality target, no external validation, no calibration emphasis, note-availability selection.

## Agreements Across Reviewers

All reviewers categorize it as method background.

## Tensions or Disagreements Across Reviewers

None.

## Label, Target, and Timing Takeaways

Clear ICU mortality timing is a useful contrast to murkier dementia labels.

## Validation and Transportability Takeaways

Held-out MIMIC performance does not imply transport.

## Bias and Downstream-Action Takeaways

ICU treatments shape both notes and mortality.

## Implications for Study Design

If using multimodal transformers, preserve strict pre-index feature windows and report calibration.

## Claims to Carry Forward

Structured EHR and notes can be fused in transformer architectures.

## Claims to Treat Cautiously

ICU benchmark gains do not establish outpatient dementia model utility.

## Open Questions

Would a simpler model match performance in a dementia EHR setting?

## Recommended Next Action

Use only in methods background.
