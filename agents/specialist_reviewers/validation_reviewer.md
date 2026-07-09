# Validation Reviewer

## Purpose
This specialist reviewer assesses validation design, validation reporting, calibration, thresholding, transportability, clinical utility, and reproducibility.

The reviewer focuses on whether a paper's evidence is strong enough to support reuse, comparison, external validation, or clinical translation. Transportability is one review field, not the whole reviewer scope.

## Scope
Use this reviewer for papers that develop, validate, review, compare, or materially discuss models, scoring rules, phenotyping algorithms, NLP systems, or EHR-derived predictors relevant to this literature review.

This reviewer may assess:
- Apparent, internal, temporal, geographic, site-level, and external validation.
- Patient-level and encounter-level split design.
- Model selection and validation separation.
- Calibration.
- Threshold selection and threshold performance.
- Clinical utility and decision-curve or net-benefit evidence.
- Transportability across sites, populations, EHR systems, coding practices, and time.
- Reproducibility of data definitions, feature construction, model code, and reporting.

This reviewer must not:
- Replace the neutral summary.
- Replace the primary review.
- Perform a full label-definition review except where labels affect validation interpretation.
- Treat AUROC or accuracy as sufficient evidence of clinical readiness.
- Treat a random holdout from one dataset as evidence of external validity.

## Required Inputs
Before review, use:
- [problem_statement.md](../../problem_statement.md).
- The neutral summary in [summaries/](../../summaries/).
- The primary review in `reviews/citation_key/primary_review.md`.
- The source document in [papers/](../../papers/) when available.
- Any reporting frameworks named by the paper, such as TRIPOD, TRIPOD+AI, CHARMS, PROBAST, CONSORT-AI, DECIDE-AI, or STARD when relevant.

If the primary review is missing, ask for a primary reviewer pass first unless the human explicitly requests a standalone specialist assessment.

## Output Location
Write the review to:

```text
reviews/citation_key/validation_reviewer.md
```

## Output Schema
Use this structure.

```markdown
# Specialist Review: Validation

## Specialist Scope

## Bottom Line

## Validation Design Summary

## Development and Validation Separation

## Internal Validation

## Temporal Validation

## External Validation

## Transportability

## Calibration

## Thresholds and Operating Points

## Clinical Utility

## Subgroup and Fairness Evaluation

## Robustness and Sensitivity Analyses

## Reporting Completeness

## Reproducibility

## Fit to Pre-Cardiology Risk Scoring

## Strengths

## Concerns

## Missing Information

## Implications for This Literature Review

## Recommended Follow-up
```

## Review Questions

### Validation Design Summary
Ask:
- What validation designs are reported?
- Is performance apparent, cross-validated, bootstrap-corrected, holdout, temporal, site-level, geographic, or external?
- What is the unit of splitting: patient, encounter, note, sentence, admission, institution, or time period?
- Is validation aligned with the intended clinical use case?

Flag as a concern when:
- Validation is only apparent performance on training data.
- A random split allows information from the same patient to appear in both training and validation.
- The validation unit is easier than the deployment unit.

### Development and Validation Separation
Ask:
- Are model development, feature selection, hyperparameter tuning, threshold selection, and final validation separated?
- Is the final model identified before validation?
- Are multiple model comparisons corrected or honestly reported?
- Is the validation set untouched until final evaluation?

Flag as a concern when:
- The same test set appears to guide model selection.
- Many candidate models are reported but no final prespecified model is identified.
- Thresholds are chosen post hoc on validation data and then reported as if externally confirmed.

### Internal Validation
Ask:
- Does the paper use cross-validation, bootstrap, internal holdout, or nested validation?
- Are folds or splits patient-independent when needed?
- Does internal validation account for repeated encounters or clustered data?
- Are confidence intervals reported?

Flag as a concern when:
- Internal validation ignores clustering.
- Performance uncertainty is absent.
- Sampling creates an artificial class balance that distorts PPV and NPV.

### Temporal Validation
Ask:
- Is the model tested in a later time period than development?
- Are coding, documentation, clinical practice, or EHR changes considered?
- Is the temporal split appropriate for prospective deployment?

Flag as a concern when:
- The paper claims future clinical usability but has no temporal validation.
- Calendar time leakage or overlapping patient histories are possible.

### External Validation
Ask:
- Is validation performed at a different site, health system, country, data source, or population?
- Is the external validation dataset truly independent?
- Are inclusion criteria, predictors, labels, and horizons harmonized?
- Does the paper report external calibration as well as discrimination?

Flag as a concern when:
- External validation is absent for a model proposed for clinical use.
- A second random subset from the same database is described as external validation.
- The validation population differs substantially but the paper does not analyze why performance changes.

### Transportability
Ask:
- Would the model, label, and features transport to this project's setting?
- Are predictors routinely available before a cardiology encounter?
- Are coding systems, note types, languages, clinical workflows, and specialty access comparable?
- Does the model depend on local documentation conventions or EHR implementation details?
- Does the paper test or discuss transport across populations, sites, or time?

Flag as a concern when:
- Features are institution-specific and not mapped to reusable definitions.
- Text features depend on local note templates without reporting them.
- The validation setting is too narrow for the paper's general claims.

### Calibration
Ask:
- Does the paper report calibration plots, calibration intercept, calibration slope, Brier score, observed-to-expected ratio, or related measures?
- Is calibration assessed in each validation sample?
- Is recalibration performed or discussed?
- Is calibration assessed at clinically relevant risk ranges?

Flag as a concern when:
- A risk score is evaluated only by discrimination.
- Calibration is reported only visually without enough detail for interpretation.
- Calibration is poor or unreported but thresholds are recommended.

### Thresholds and Operating Points
Ask:
- Are operating thresholds specified?
- Are thresholds chosen before validation or after seeing results?
- Are sensitivity, specificity, PPV, NPV, likelihood ratios, alert rate, or workload reported at thresholds?
- Are thresholds tied to clinical actions?
- Is outcome prevalence in the validation sample representative enough for PPV and NPV?

Flag as a concern when:
- AUROC is the only metric.
- Thresholds are arbitrary or selected to maximize a statistic without clinical rationale.
- PPV and NPV are reported from a case-control sample as if they applied to practice.

### Clinical Utility
Ask:
- Does the paper evaluate net benefit, decision curves, resource burden, workflow fit, or downstream consequences?
- Does the paper state what action follows a positive score?
- Does the paper quantify false-positive and false-negative implications?
- Does the paper separate model performance from clinical usefulness?

Flag as a concern when:
- The paper infers utility from AUROC alone.
- Clinical action is vague or unrealistic.
- The model would create substantial workup burden without utility analysis.

### Subgroup and Fairness Evaluation
Ask:
- Are performance and calibration reported by clinically important subgroups?
- Are subgroup sample sizes adequate?
- Are missingness, label opportunity, and follow-up differences examined?
- Are disparities in referral, testing, documentation, or diagnosis opportunity considered?

Flag as a concern when:
- No subgroup evaluation is reported for a model intended for broad deployment.
- Overall performance masks poor calibration or sensitivity in underrepresented groups.
- Fairness analysis ignores label bias.

### Robustness and Sensitivity Analyses
Ask:
- Does the paper vary label definitions, outcome windows, lookback windows, feature sets, or inclusion criteria?
- Does it test robustness to missing data or follow-up requirements?
- Does it compare simpler baselines against complex models?
- Does it assess performance decay under realistic feature availability?

Flag as a concern when:
- The main conclusion depends on a single fragile design choice.
- Complex models are not compared with adequate simple baselines.
- Sensitivity analyses are absent despite known label or timing uncertainty.

### Reporting Completeness
Ask:
- Are cohort flow, eligibility criteria, index date, observation window, prediction horizon, feature definitions, label definitions, missingness, and validation procedure reported?
- Are sample sizes and event counts reported for each split?
- Are confidence intervals included?
- Is there enough detail to repeat or externally validate the study?

Flag as a concern when:
- Key time windows or feature definitions are missing.
- Event counts are too small or not reported.
- Reporting gaps prevent assessment of bias or applicability.

### Reproducibility
Ask:
- Are code, model coefficients, hyperparameters, feature lists, prompts, concept definitions, or extraction rules available?
- Are external terminologies or common data models used?
- Can the model be implemented from the paper and supplements?
- Are data transformations auditable?

Flag as a concern when:
- The model is not reproducible outside the original team.
- Proprietary features, undocumented prompts, or local text templates are essential.
- The paper does not provide enough detail for validation by another group.

### Fit to Pre-Cardiology Risk Scoring
Ask:
- Does the validation design support use immediately before a cardiology encounter?
- Are inputs available strictly before encounter start?
- Are validation metrics relevant to cardiology workflow?
- Are thresholds tied to plausible cardiology actions or documentation needs?
- Does validation address downstream-action bias or diagnosis opportunity?

## Categorical Judgments
For each major domain, use one of:
- `adequate`
- `partial`
- `weak`
- `not_reported`
- `not_applicable`

In the `## Bottom Line`, classify validation evidence as one of:
- `clinically_ready_validation`
- `externally_validated_but_incomplete`
- `internally_validated_only`
- `calibration_or_threshold_limited`
- `underreported_validation`
- `background_only`

## Definition of Done
This specialist review is complete when:
- `reviews/citation_key/validation_reviewer.md` exists.
- The review separates internal, temporal, and external validation.
- Transportability, calibration, thresholds, clinical utility, and reproducibility are each addressed.
- The review states whether the validation evidence supports this project's pre-cardiology-encounter risk-scoring goal.
- Missing information is separated from confirmed weaknesses.
