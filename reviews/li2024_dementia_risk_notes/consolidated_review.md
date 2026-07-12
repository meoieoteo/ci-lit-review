# Consolidated Review: li2024_dementia_risk_notes

## Consolidation Status

consolidated_complete

## One-Sentence Takeaway

Li et al. provides direct evidence that longitudinal medical notes can support future dementia-diagnosis risk prediction when observation windows and prediction horizons are explicit, but the evidence remains internally validated and label-limited.

## Bottom Line for This Literature Review

This is a central paper for EHR-text dementia risk modeling and long-note content selection. It should be cited for notes-only risk prediction and timing design, while carrying caveats about balanced case-control sampling, coded diagnosis labels, lack of calibration, and no external validation.

## What This Paper Should Be Cited For

- `ehr_text_signal`
- `longitudinal_ehr_modeling`
- `dementia_prediction_performance`
- `target_definition`
- `validation_quality`

## What This Paper Should Not Be Cited For

Do not cite it for clinical readiness, real-world PPV, cardiology-specific workflow, validated cognitive impairment labels, external transportability, or interpretable cognitive concept extraction.

## Publication Status and Evidence Weight

Peer-reviewed final journal article. Moderate direct evidence: topically close to the project, but not enough for deployment claims.

## Evidence Strength

- `moderate_direct_evidence`
- `methodological_caution`

## Key Contributions

- Defines explicit one- and two-year observation periods and six-month and one-year prediction horizons.
- Uses medical notes only.
- Proposes decision-focused sentence selection for long clinical text.
- Holds Longformer classification architecture constant while comparing content-selection methods.
- Reports internal cross-validated AUCs up to 81.64 for shorter horizon settings.

## Key Limitations

- EHR diagnosis label lacks reported code list or adjudicated validation.
- Controls are diagnosis-negative rather than cognitively confirmed negative.
- Balanced case-control design prevents direct interpretation of real-world precision, PPV, workload, or calibration.
- No external, temporal, subgroup, or clinical utility validation.
- No concept-level NLP outputs.

## Agreements Across Reviewers

All reviewers agree the paper is directly relevant for notes-only dementia risk prediction and long-note modeling. All also agree that label and validation limitations must be carried forward.

## Tensions or Disagreements Across Reviewers

The modeling contribution is stronger than the clinical deployment evidence. The paper is valuable for method design, but its future diagnosis label may partly reflect diagnostic opportunity and documentation rather than underlying cognitive state alone.

## Label, Target, and Timing Takeaways

The target is future coded dementia diagnosis, not current unmet cognitive care need. The observation-window/prediction-horizon framing is useful and should be adopted in our study-design template. The exact disease index and code algorithms need source checking.

## Validation and Transportability Takeaways

Internal cross-validation supports method comparison but not external deployment. Any local adaptation needs temporal/site validation, calibration, subgroup analysis, and prevalence-aware operating points.

## Bias and Downstream-Action Takeaways

The future diagnosis label is susceptible to diagnostic opportunity. Shorter horizon models may perform better partly because notes contain near-diagnosis recognition or workup signals.

## Implications for Study Design

For a pre-cardiology model, this paper supports using defined lookback windows, horizons, and long-note content-selection comparisons. It also argues for separating notes-only models from structured-plus-text models and for measuring whether text models learn cognitive evidence or care-pathway documentation.

## Claims to Carry Forward

- Medical notes alone contain signal for future dementia diagnosis risk.
- Content selection matters for transformer models over longitudinal notes.
- Observation period and prediction horizon materially affect performance.
- Generic summarization is not necessarily the best preprocessing for disease-specific prediction.

## Claims to Treat Cautiously

- Accuracy, precision, and F1 under real-world prevalence.
- Any claim of clinical utility or deployability.
- Any claim that the model detects true cognitive impairment rather than future diagnosis documentation.
- Any claim that the method transports to cardiology notes or Epic without local validation.

## Open Questions

- What exact dementia and MCI code definitions were used?
- How would the model calibrate in an unbalanced deployment cohort?
- What note types and sections drive predictions?
- Would structured features improve or dominate notes-only prediction?
- How much of the signal reflects diagnosis opportunity, cognitive workup, or utilization?

## Recommended Next Action

Use as a direct modeling anchor in Sections 3, 6, 7, 8, and 10. Before manuscript use, source-check the code repository or supplements for label definitions and inspect whether selected sentences can inform the project's note-concept inventory.
