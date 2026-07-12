# Consolidated Review: wei2025_mci_adrd_phenotyping_ehr

## Consolidation Status

consolidated_complete

## One-Sentence Takeaway

Wei et al. shows that chart-review-labeled MCI/ADRD phenotyping improves substantially when clinical-note features are combined with ICD and medication features.

## Bottom Line for This Literature Review

This is a direct anchor for MCI/ADRD EHR phenotyping, note signal, and code-only label limitations. It should not be treated as future dementia risk prediction.

## What This Paper Should Be Cited For

- `label_construction`
- `ehr_text_signal`
- `note_concept_extraction`
- `validation_quality`
- `implementation_or_transportability`

## What This Paper Should Not Be Cited For

Future risk prediction, cardiology workflow, ADRD subtype/severity classification, adjudicated cognitive testing, calibration, or national generalizability.

## Publication Status and Evidence Weight

Peer-reviewed journal article. Strong direct relevance for phenotyping; moderate clinical generalizability because validation is limited to two Boston institutions and uncertain cases were excluded.

## Evidence Strength

- `strong_direct_evidence`
- `methodological_caution`

## Key Contributions

- Manual chart-review reference labels for MCI/ADRD.
- ICD, medication, and note features compared directly.
- Note-only model far outperformed ICD-only and medication-only models.
- Combined model achieved AUROC/AUPRC 0.97 in combined data.
- Site experiments and error analysis are reported.

## Key Limitations

- No future prediction horizon.
- No calibration.
- No inter-rater reliability.
- No subtype or severity labels.
- Boston-only sites.
- Date-range discrepancy between abstract and methods.

## Agreements Across Reviewers

All reviewers agree Wei is direct evidence for note-enhanced MCI/ADRD phenotyping and stronger than code-only label evidence.

## Tensions or Disagreements Across Reviewers

The label is stronger than ICD-only, but the same notes support both chart review and model features, so it is phenotype extraction rather than independent future risk prediction.

## Label, Target, and Timing Takeaways

Manual chart review and an uncertain category are useful design elements. For local work, uncertain cases should be retained as an explicit class or adjudication queue rather than simply discarded.

## Validation and Transportability Takeaways

Two-site validation is useful but geographically narrow. Local validation should include calibration, subgroup performance, and external or temporal testing.

## Bias and Downstream-Action Takeaways

The model identifies documented MCI/ADRD, not all true impairment. False negatives among non-cognitive specialists show documentation opportunity matters.

## Implications for Study Design

Use Wei's MED/ICD strata as a template for enriched chart-review sampling. Include notes-only, structured-only, and combined baselines. Separate explicit diagnosis terms from pre-diagnosis cognitive evidence in concept inventories.

## Claims to Carry Forward

- Clinical notes substantially improve MCI/ADRD phenotyping over ICD-only features.
- Simple TF-IDF plus logistic regression can be highly competitive.
- Site-specific documentation patterns affect performance.

## Claims to Treat Cautiously

- Estimated 99.88% random-sample accuracy.
- Generalization beyond Boston.
- Use for undiagnosed impairment or future risk.

## Open Questions

- What would performance be with double-adjudicated labels?
- How does the model perform in cardiology notes or non-academic EHRs?
- Which selected terms represent pre-diagnosis evidence versus explicit known diagnosis?

## Recommended Next Action

Promote to reviewed evidence base and use in Sections 4, 6, 10, and 11. Source-check the repository before adopting code lists or feature lists.
