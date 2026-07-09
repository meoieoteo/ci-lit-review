# Consolidated Review: john2022_dementia_prediction_validation

## Consolidation Status
consolidated_complete

## One-Sentence Takeaway
John et al. shows that many published dementia prediction models cannot be externally validated because they omit essential target, timing, and model-specification details.

## Bottom Line for This Literature Review
This is a high-value validation and reproducibility paper. It should be used with Lu et al. to argue that our contribution must include rigorous target definition, timing, reporting, validation, and recalibration planning rather than relying on model architecture novelty.

## What This Paper Should Be Cited For
- `validation_quality`
- `calibration_or_thresholding`
- `implementation_or_transportability`
- `target_definition`
- `ehr_to_common_data_model`

## What This Paper Should Not Be Cited For
- Evidence that unstructured EHR text improves dementia prediction.
- Evidence for cardiology-specific cognitive-risk workflows.
- A validated label for current unmet cognitive care need.

## Evidence Strength
- `strong_direct_evidence` for reporting and external-validation barriers.
- `moderate_direct_evidence` for OMOP/OHDSI transportability framing.
- `methodological_caution` for underreported dementia prediction models.

## Key Contributions
- Demonstrates that external validation is often impossible from published reports.
- Identifies missing index dates, predictor windows, model specifications, and recalibration details as practical barriers.
- Shows the value of common data model infrastructure for validation.

## Key Limitations
- Does not address EHR text.
- Does not address cardiology workflow.
- Does not solve dementia label validity or diagnosis-opportunity bias.

## Agreements Across Reviewers
All review passes agree this paper is central for validation, reporting, reproducibility, and transportability.

## Tensions or Disagreements Across Reviewers
No major disagreement. The main caution is that validation feasibility does not equal label validity or clinical utility.

## Label, Target, and Timing Takeaways
Target and time-window reporting are essential. Missing index date or predictor-window detail prevents leakage assessment and external validation.

## Validation and Transportability Takeaways
External validation and recalibration require full model specification and common operational definitions.

## Bias and Downstream-Action Takeaways
The paper does not directly analyze downstream-action bias, but it reinforces the reporting needed to detect it.

## Implications for Study Design
Our study should publish enough detail for external validation: index date, observation window, prediction horizon, label algorithm, full predictor definitions, model specification, baseline risk, calibration, and validation design.

## Claims to Carry Forward
- Existing dementia prediction models are frequently underreported for external validation.
- Common data model infrastructure can support transportability testing.
- Calibration and model specification details are not optional for clinical prediction.

## Claims to Treat Cautiously
- Any claim that validated existing models are ready for cardiology deployment.
- Any inference that structured-data models answer the EHR-text question.

## Open Questions
- Which reporting checklist should our study follow: TRIPOD, TRIPOD+AI, OHDSI PLP conventions, or a project-specific superset?
- Which external or temporal validation setting is feasible for our data?

## Recommended Next Action
Use this paper to strengthen the validation section of `literature_review_state.md` and prioritize exact source checks before manuscript citation.
