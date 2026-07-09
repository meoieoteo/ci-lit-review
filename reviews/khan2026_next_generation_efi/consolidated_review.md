# Consolidated Review: khan2026_next_generation_efi

## Consolidation Status
consolidated_complete

## One-Sentence Takeaway
Khan et al. is a strong concept-feature analogue showing how structured EHR plus note-derived geriatric deficits can support interpretable risk representation.

## Bottom Line for This Literature Review
This paper should inform feature design, especially the cognitive/frailty note-concept inventory. It should not be cited as direct dementia prediction evidence or as validated cardiology deployment evidence.

## What This Paper Should Be Cited For
- `note_concept_extraction`
- `longitudinal_ehr_modeling`
- `ehr_text_signal`
- `background_only` for cognitive-risk labels

## What This Paper Should Not Be Cited For
- Dementia diagnosis or cognitive impairment labels.
- External validation.
- US Epic cardiology transportability.
- Causal effects.

## Evidence Strength
- `useful_analogy`
- `moderate_direct_evidence` for note-derived deficit representation.

## Key Contributions
- Combines structured EHR and note-derived deficits.
- Includes age-related neurocognitive problems and other cognitive-adjacent deficits.
- Uses interpretable concept features rather than only raw embeddings.

## Key Limitations
- Preprint status.
- Not dementia-specific.
- No external validation.
- Documentation and utilization may shape both features and outcomes.

## Agreements Across Reviewers
All reviews agree that the concept-feature strategy is valuable but indirect.

## Tensions or Disagreements Across Reviewers
No major disagreement. The main tension is promise for feature design versus weak direct fit to the cardiology target.

## Label, Target, and Timing Takeaways
The eFI is a frailty-deficit construct, not a cognitive impairment label. It illustrates how note concepts can be longitudinally represented.

## Validation and Transportability Takeaways
Internal validation and comparator-index performance are useful; cross-system transport remains unproven.

## Bias and Downstream-Action Takeaways
Recorded deficits and utilization outcomes can reflect healthcare contact intensity.

## Implications for Study Design
Use this to seed candidate note concepts: neurocognitive problems, falls, mobility, sensory impairment, loneliness, assistance needs, and functional limitations.

## Claims to Carry Forward
- Interpretable note-derived deficits are a plausible middle path between structured data and opaque text embeddings.

## Claims to Treat Cautiously
- That eFI-style deficits directly measure dementia or unmet cognitive care need.
- That Finnish NLP extraction will transport to US Epic data.

## Open Questions
- Which eFI deficit concepts map most directly to cardiology cognitive-risk scoring?
- How should documentation opportunity be modeled for note-derived deficits?

## Recommended Next Action
Use this paper when building the first cognitive/frailty note-concept inventory.
