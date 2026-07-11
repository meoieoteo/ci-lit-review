# Consolidated Review: adejumo2024_hf_functional_status_nlp

## Consolidation Status
consolidated_complete

## One-Sentence Takeaway
Adejumo et al. shows that supervised ClinicalBERT models can extract clinically meaningful functional-status information from outpatient cardiology notes, substantially increasing capture beyond explicit NYHA mentions.

## Bottom Line for This Literature Review
This is a strong methods analogue for cardiology-note concept extraction. It should be cited for the feasibility of extracting underdocumented clinical state from cardiology notes, not for dementia prediction.

## What This Paper Should Be Cited For
- `ehr_text_signal`
- `note_concept_extraction`
- `implementation_or_transportability`
- cardiology-note NLP workflow

## What This Paper Should Not Be Cited For
- Dementia prediction.
- Cognitive impairment labels.
- Downstream-action bias.
- Calibrated risk scoring.

## Evidence Strength
- `moderate_direct_evidence` for cardiology-note NLP extraction.
- `useful_analogy` for cognitive/functional note-concept extraction.

## Key Contributions
- Demonstrates note-derived clinical-state capture in outpatient cardiovascular care.
- Uses sectioning, expert annotation, ClinicalBERT, and multi-site validation.
- Shows added capture beyond explicit NYHA documentation.

## Key Limitations
- Not dementia-specific.
- Documentation-dependent labels.
- No independent health-system validation.
- No calibration or action-linked risk thresholds.

## Agreements Across Reviewers
All reviews agree this paper is useful as a methods analogue but not direct cognitive-risk evidence.

## Tensions or Disagreements Across Reviewers
No major disagreement. The main caution is that extraction performance should not be confused with patient-outcome risk prediction.

## Label, Target, and Timing Takeaways
The label is current documented functional status in encounter notes. A cognitive analogue would need explicit annotation rules and strict pre-index timing.

## Validation and Transportability Takeaways
Validation across multiple sites in one health system is useful, but local documentation dependence remains.

## Bias and Downstream-Action Takeaways
Documentation practices may encode care process and clinician behavior.

## Implications for Study Design
Supports building interpretable note-derived concepts and validating them locally before using them in a cognitive-risk model.

## Claims to Carry Forward
- Cardiology notes can contain recoverable clinical-state information not captured by explicit structured fields.
- Sectioned clinical-note NLP is a plausible feature-extraction strategy.

## Claims to Treat Cautiously
- That similar performance will transfer to cognitive concepts.
- That extracted documentation equals true patient state.

## Open Questions
- Which cognitive, functional, caregiver, and navigation concepts should be annotated first?
- How much local annotation is required for reliable transfer?

## Recommended Next Action
Use this paper in the EHR-text and note-concept sections; source-check the supplement for annotation, sectioning, and Epic extraction details.

## New Specialist Review Addendum
The NLP/concept-extraction review strengthens this paper's role as a central cardiology-note concept-extraction analogue. The EHR schema/CDM review adds that the Epic Clarity and note-sectioning details are highly relevant to local implementation, but the paper should not be treated as an OMOP or common-data-model template.
