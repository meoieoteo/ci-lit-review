# Consolidated Review: shao2019_probable_dementia_ehr

## Consolidation Status

consolidated_complete

## One-Sentence Takeaway

Shao et al. is a direct, useful example of using structured EHR data plus note-derived topic features to identify probable undiagnosed dementia, but its evidence is not sufficient for clinical deployment without stronger validation and workflow analysis.

## Bottom Line for This Literature Review

This paper should be carried forward as a central Section 8 candidate for the fixed-feature structured-plus-text rung of the modeling ladder. It also supports the label-definition argument that dementia diagnosis codes are useful but incomplete.

## What This Paper Should Be Cited For

- `ehr_text_signal`
- `note_concept_extraction`
- `dementia_prediction_performance`
- `label_construction`
- `validation_quality`

Specifically, cite it for a structured-plus-unstructured EHR approach to probable undiagnosed dementia case finding and for the idea of using imperfect coded labels as a silver standard with chart-review validation.

## What This Paper Should Not Be Cited For

Do not cite it as evidence of cardiology deployment readiness, external validation, calibration, clinical utility, or superiority of text-only models.

## Publication Status and Evidence Weight

Peer-reviewed version of record. Evidence strength is moderate direct evidence, limited by single-system VA data, mostly male cohort, weak supervision, and lack of external validation.

## Evidence Strength

- `moderate_direct_evidence`
- `methodological_caution`

## Key Contributions

- Demonstrates structured plus unstructured EHR feature construction for probable dementia.
- Makes the underdiagnosis problem explicit.
- Uses manual specialist review of uncoded controls.

## Key Limitations

- No external validation.
- No standard calibration or decision-curve analysis.
- Limited reproducibility of exact feature set.
- Diagnosis opportunity remains a major bias concern.

## Agreements Across Reviewers

All reviewers agree that the paper is directly relevant and methodologically informative, but not clinically ready.

## Tensions or Disagreements Across Reviewers

The primary review sees strong modeling relevance; specialist reviews emphasize that the NLP features are topics rather than clinically validated concepts.

## Label, Target, and Timing Takeaways

The target is closer to current undocumented dementia than future risk. Three-year pre-index history is clear, but care-pathway documentation may still drive the label.

## Validation and Transportability Takeaways

Manual review strengthens the paper, but external validation and transportability to Epic/cardiology are untested.

## Bias and Downstream-Action Takeaways

Specialty-coded dementia and uncoded controls reflect diagnosis opportunity, not only disease state.

## Implications for Study Design

The project should include a structured baseline and a structured-plus-note-concept/topic model before testing embeddings or LLMs. It should also define indeterminate labels and plan chart-review validation.

## Claims to Carry Forward

- Absence of dementia codes is not equivalent to absence of dementia.
- Note-derived fixed features can help identify probable undiagnosed dementia.
- Silver-standard labels need validation against expert review or stronger clinical evidence.

## Claims to Treat Cautiously

- Reported AUC and threshold metrics should not be generalized without source-context caveats.
- Topic features should not be equated with portable cognitive concepts.

## Open Questions

- Which exact note-derived topic/concept families would transport to outpatient cardiology?
- How much incremental value did text add beyond structured features?
- How would calibration perform in a new health system?

## Recommended Next Action

Use this paper as a high-priority source for Section 8 synthesis and consider a source-check pass if citing exact performance or feature examples.
