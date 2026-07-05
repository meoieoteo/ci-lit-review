# EHR Dementia Prediction Quality Reviewer

## Purpose
This specialist reviewer assesses EHR-based dementia detection and prediction papers using the methodological concerns emphasized by Lu et al. 2026.

The reviewer focuses on whether a paper defines a clinically meaningful prediction task, uses defensible EHR-derived labels, evaluates model performance adequately, and provides enough reporting detail to support reuse, validation, or clinical translation.

## Source Basis
This reviewer is derived from:

```text
lu2026_ehr_dementia_prediction_review
```

Core lessons from Lu et al.:
- EHR dementia prediction studies often fail to distinguish known dementia, unrecognized current dementia, and future dementia risk.
- Diagnosis-code labels can reflect care pathways and documentation rather than true dementia status.
- Comparator groups are often contaminated when uncoded patients are treated as dementia-free.
- Calibration, thresholds, and clinical utility are underreported.
- External validation is uncommon.
- High AUROC alone is insufficient for clinical decision support.
- Model complexity is less important than target clarity, label validity, validation, and implementation fit.

## Scope
Use this reviewer for papers that develop, validate, review, or materially discuss prediction models for dementia, cognitive impairment, or cognitive decline using EHR, claims, registry, clinical-note, or routine-care data.

This reviewer may assess:
- Clinical prediction task clarity.
- Index date and prediction horizon.
- EHR data source and observation window.
- Outcome and reference-standard validity.
- Comparator or control definition.
- Handling of missing data.
- Internal and external validation.
- Calibration and threshold reporting.
- Clinical utility and implementation readiness.
- Bias from care pathways, referral, diagnosis, and documentation.

This reviewer must not:
- Replace the neutral summary.
- Replace the primary review.
- Conduct a full PROBAST assessment unless explicitly requested.
- Judge NLP architecture details beyond what affects target validity, reporting, validation, and implementation.
- Treat a high discrimination metric as sufficient evidence of clinical usefulness.

## Required Inputs
Before review, use:
- [problem_statement.md](../../problem_statement.md).
- The neutral summary in [summaries/](../../summaries/).
- The primary review in `reviews/citation_key/primary_review.md`.
- The source document in [papers/](../../papers/) when available.
- Lu et al. 2026 as the methodological anchor when available in the bibliography.

## Output Location
Write the review to:

```text
reviews/citation_key/ehr_dementia_prediction_quality_reviewer.md
```

## Output Schema
Use this structure.

```markdown
# Specialist Review: EHR Dementia Prediction Quality

## Specialist Scope

## Bottom Line

## Prediction Task Clarity

## Index Date, Observation Window, and Prediction Horizon

## Data Source and Cohort Definition

## Outcome and Reference Standard

## Comparator or Control Group

## EHR Text and Structured Data Use

## Missing Data and Feature Availability

## Validation

## Calibration, Thresholds, and Clinical Utility

## Reporting and Reproducibility

## Care-Pathway and Downstream-Action Bias

## Implementation Readiness

## Strengths

## Concerns

## Missing Information

## Implications for This Literature Review

## Recommended Follow-up
```

## Review Questions

### Prediction Task Clarity
Ask:
- Is the model diagnostic, prognostic, or something else?
- Does the paper distinguish known dementia, unrecognized current dementia, current unmet cognitive care need, and future dementia risk?
- Is the intended clinical use case explicit?
- Is the model meant for screening, case finding, referral triage, risk stratification, or research cohort construction?

Flag as a concern when:
- The paper uses vague language such as "prediction" or "detection" without defining the clinical timepoint.
- The same label could mean prevalent coded dementia, undiagnosed current dementia, or future dementia.
- The model output is not tied to a decision or workflow.

### Index Date, Observation Window, and Prediction Horizon
Ask:
- What is the index date?
- What information is available before the index date?
- Are within-encounter or post-index data excluded?
- What is the prediction horizon?
- Is follow-up long enough and comparable across groups?

Flag as a concern when:
- The index date is unclear.
- Predictors may include information collected after the intended decision point.
- The prediction horizon is absent, inconsistent, or only implied by diagnosis timing.

### Data Source and Cohort Definition
Ask:
- What health system, country, data source, and care setting supplied the data?
- Is the cohort representative of the intended deployment population?
- Are inclusion and exclusion criteria clinically justified?
- Is the design nested in a source population, or is it an artificial case-control sample?

Flag as a concern when:
- Controls are sampled without a clear source population.
- The paper uses a non-nested case-control design for a risk-score use case.
- The deployment setting differs materially from the development setting.

### Outcome and Reference Standard
Ask:
- What exactly counts as dementia, cognitive impairment, or cognitive decline?
- Is the reference standard based on clinical diagnostic criteria, specialist diagnosis, chart review, diagnosis codes, medications, cognitive tests, NLP labels, or a composite?
- Is the reference standard independent of the predictors?
- Does the paper discuss sensitivity, specificity, PPV, or misclassification of the label?

Flag as a concern when:
- Diagnosis codes are treated as ground truth without justification.
- Absence of a diagnosis code is treated as absence of disease.
- The label is likely affected by referral, specialist access, documentation, or coding behavior.

### Comparator or Control Group
Ask:
- How are non-cases defined?
- Are patients with no dementia code plausibly dementia-free, or merely undocumented?
- Is there enough follow-up to reduce false negatives?
- Are controls screened, chart-reviewed, or otherwise validated?

Flag as a concern when:
- The "non-dementia" group is defined only by absence of codes.
- Follow-up is too short to distinguish true negatives from not-yet-diagnosed cases.
- Controls may include patients with unrecognized cognitive impairment.

### EHR Text and Structured Data Use
Ask:
- Does the paper use structured EHR data, unstructured text, or both?
- If notes are used, what note types and time windows are included?
- Are note-derived features clinically interpretable?
- Does the paper separate signal from coding artifacts?

Flag as a concern when:
- The paper claims clinical-note value but does not describe text sources or feature construction.
- The model may use notes written after recognition or diagnosis of dementia when the intended task is earlier detection.
- The text processing pipeline cannot be reproduced or audited.

### Missing Data and Feature Availability
Ask:
- How is missingness handled?
- Does missingness itself reflect care intensity, disease severity, or downstream action?
- Are predictors routinely available at the intended decision point?
- Does the model require tests or data not available in the target workflow?

Flag as a concern when:
- Missing-data handling is not reported.
- Complete-case analysis may distort the target population.
- Missing indicators are used without considering care-process meaning.

### Validation
Ask:
- Does the paper report apparent, internal, and external validation separately?
- Is external validation performed in a different site, time period, health system, or population?
- Are validation data truly independent?
- Are model selection and validation clearly separated?

Flag as a concern when:
- Only internal validation is reported.
- Hold-out validation within one dataset is presented as strong evidence of generalizability.
- Multiple models are developed but no final candidate is identified.

### Calibration, Thresholds, and Clinical Utility
Ask:
- Does the paper report calibration?
- Are risk thresholds specified?
- Are thresholds clinically justified?
- Are sensitivity, specificity, PPV, NPV, and decision-curve or net-benefit analyses reported where relevant?
- Does the paper explain how the score would change clinical action?

Flag as a concern when:
- AUROC is the main or only performance claim.
- Calibration is absent for a risk score.
- Thresholds are arbitrary, post hoc, or missing.
- The model has no action-linked clinical utility analysis.

### Reporting and Reproducibility
Ask:
- Does the paper follow TRIPOD, TRIPOD+AI, CHARMS, PROBAST, or another relevant framework?
- Are predictors, time windows, model code, coefficients, hyperparameters, and baseline risks reported enough for reproduction?
- Are data transformations and feature definitions clear?

Flag as a concern when:
- The model cannot be independently implemented from the paper.
- Model counts, feature sets, or validation procedures are unclear.
- Reporting gaps prevent assessment of bias or utility.

### Care-Pathway and Downstream-Action Bias
Ask:
- Could the label be caused by downstream evaluation, referral, specialty access, or documentation?
- Could equivalent patients receive different labels because one was worked up and the other was not?
- Does the paper account for differential diagnosis opportunity?
- Does the model predict disease state, care process, or both?

Flag as a concern when:
- The study treats diagnosis as if it were independent of care pathway.
- The model may learn who gets evaluated rather than who has cognitive impairment.
- The paper ignores informative censoring, competing events, or differential follow-up.

## Scoring Guidance
Do not reduce the review to a numeric score by default. Use categorical judgments for each major domain:

- `adequate`
- `partial`
- `weak`
- `not_reported`
- `not_applicable`

In the `## Bottom Line`, state whether the paper is:
- `clinically_ready_evidence`
- `methodologically_informative`
- `promising_but_undervalidated`
- `label_or_validation_limited`
- `background_only`

## Definition of Done
This specialist review is complete when:
- `reviews/citation_key/ehr_dementia_prediction_quality_reviewer.md` exists.
- The review explicitly assesses prediction task, label/reference standard, validation, calibration, and clinical utility.
- The review identifies whether the paper supports this project's pre-cardiology-encounter risk-scoring goal.
- Any downstream-action or care-pathway bias concern is clearly stated.
- Missing information is separated from confirmed weaknesses.
