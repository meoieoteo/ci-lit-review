# Specialist Review: EHR Dementia Prediction Quality

## Specialist Scope

Assessment of Li et al. as an EHR-based dementia prediction paper, using target clarity, label validity, validation, and implementation concerns emphasized in the dementia EHR prediction literature.

## Bottom Line

`promising_but_undervalidated`. The paper has a clearer prediction task than many EHR dementia studies because it specifies observation periods and prediction horizons, and it directly uses EHR notes. Its clinical evidence is limited by internal validation, balanced case-control sampling, unvalidated coded diagnosis labels, absent calibration, and absent clinical utility testing.

## Prediction Task Clarity

The task is future dementia risk prediction from medical notes. The target is not current dementia detection and not current unmet cognitive care need. The paper explicitly distinguishes detection models from risk prediction models and evaluates six-month and one-year horizons.

## Index Date, Observation Window, and Prediction Horizon

The study uses one- and two-year observation periods and six-month or one-year prediction horizons. Controls are matched around the disease index date of cases. The timing design is a strength, though the exact operational definition of disease index date is not fully specified.

## Data Source and Cohort Definition

Data come from INPC through Regenstrief. The initial cohort includes 4,796 incident dementia cases and 21,440 controls, downsampled to 4,796 controls for a balanced dataset. Patients with MCI or prior dementia are excluded from cases; controls have no dementia or MCI diagnosis.

## Outcome and Reference Standard

The reference standard is EHR diagnosis status for incident dementia. The main text does not report code lists, clinical adjudication, cognitive testing, or validation of the diagnosis algorithm. This is adequate for a future coded-diagnosis target, but weak for true cognitive impairment.

## Comparator or Control Group

Controls are no-dementia/no-MCI diagnosis controls matched on sex, race, and age within five years. This is a common but limited comparator because uncoded cognitive impairment may remain in controls.

## EHR Text and Structured Data Use

The model uses medical notes only. It does not use structured diagnoses, medications, labs, procedures, demographics, or cognitive tests as predictors in the model evaluated here. This isolates note signal but does not test the best multimodal EHR model.

## Missing Data and Feature Availability

Missingness is not deeply reported. The paper notes that long observation periods may be impractical because older records may not be available, and it limits observation periods to one or two years. It does not quantify note absence, sparse histories, or care-utilization missingness.

## Validation

Validation is internal three-fold cross-validation. No external, temporal, site-level, or prospective validation is reported for this model.

## Calibration, Thresholds, and Clinical Utility

Calibration is absent. Binary operating metrics are reported, but threshold choice is not tied to a clinical action. Clinical utility is asserted as potential support for primary care referral decisions, but not measured.

## Reporting and Reproducibility

The model and content-selection algorithm are described in substantial detail, and code is reported as available. Reproducibility is limited by restricted data and missing operational label/note metadata details.

## Care-Pathway and Downstream-Action Bias

The future dementia label depends on diagnosis and documentation opportunity. The study does not measure primary-care contact, cognitive testing, neurology referral, or other care-pathway variables that might make the outcome observable. This matters for this review because the project explicitly worries that future diagnosis is partly caused by downstream clinical action.

## Implementation Readiness

Not clinically ready for this project's use. The method is implementation-relevant for long-note processing, but a cardiology-facing model would need local Epic extraction, encounter anchoring, calibration, thresholds, subgroup analysis, and label validation.

## Strengths

- Explicit risk-prediction framing rather than vague dementia prediction.
- Clear observation windows and horizons.
- Notes-only design with long-text method comparison.
- Baselines held to the same Longformer classifier.
- Multi-system EHR network source.

## Concerns

- Unvalidated coded diagnosis outcome.
- Case-control balancing and downsampling.
- No external validation or calibration.
- No real-world clinical utility evaluation.
- Limited reporting of note types and EHR schema details.

## Missing Information

- Dementia and MCI code definitions.
- Follow-up requirements and censoring rules.
- Note-type inventory and timestamp availability.
- Site-level or subgroup performance.
- Calibration and decision thresholds.

## Implications for This Literature Review

This paper should be cited as direct evidence that medical notes can support future dementia diagnosis risk prediction with explicit timing. It should also be used as an example of the validation and label limitations that remain even in well-framed notes-only prediction studies.

## Recommended Follow-up

Pair this paper with stronger validation and label-definition evidence before making claims about clinical deployment or real-world performance.
