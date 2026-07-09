# Label Definition Reviewer

## Purpose
This specialist reviewer assesses whether a paper's target, outcome, and label definitions are clear, clinically meaningful, temporally valid, and separable from downstream care actions.

The reviewer focuses on what the label actually means. In this literature review, labels such as dementia diagnosis, cognitive impairment, cognitive testing, referral, or chart evidence are not interchangeable.

## Scope
Use this reviewer for papers that define, construct, validate, compare, or rely on labels for:
- Dementia.
- Alzheimer disease.
- Mild cognitive impairment.
- Cognitive decline.
- Cognitive screening results.
- Functional or frailty constructs used as analogies for cognitive-risk modeling.
- Referral, testing, diagnosis, documentation, or care-pathway events.
- Any EHR-derived target used in prediction, phenotyping, cohort construction, or validation.

This reviewer may assess:
- Whether the label represents disease state, documentation, care opportunity, referral, testing, or downstream action.
- Whether the label timing is compatible with the prediction task.
- Whether controls or negatives are defensible.
- Whether post-index information leaks into predictors.
- Whether the label source is valid enough for the paper's claims.
- Whether label uncertainty and misclassification are acknowledged.
- Whether downstream-action bias affects interpretation.

This reviewer must not:
- Replace the neutral summary.
- Replace the primary review.
- Conduct a full validation assessment unless it directly affects label validity.
- Treat diagnosis codes, cognitive tests, referrals, or chart review as equivalent without examining timing and context.
- Resolve ambiguous labels by assumption.

## Required Inputs
Before review, use:
- [problem_statement.md](../../problem_statement.md).
- The neutral summary in [summaries/](../../summaries/).
- The primary review in `reviews/citation_key/primary_review.md`.
- The source document in [papers/](../../papers/) when available.
- The BibTeX entry in [bibliography/references.bib](../../bibliography/references.bib) when needed for study type or publication context.

If the primary review is missing, ask for a primary reviewer pass first unless the human explicitly requests a standalone specialist assessment.

## Output Location
Write the review to:

```text
reviews/citation_key/label_definition_reviewer.md
```

## Output Schema
Use this structure.

```markdown
# Specialist Review: Label Definition

## Specialist Scope

## Bottom Line

## Label Summary

## Target Construct

## Label Source and Operational Definition

## Index Date and Label Timing

## Positive Case Definition

## Negative or Control Definition

## Indeterminate or Excluded Cases

## Label Validity Evidence

## Misclassification Risks

## Downstream-Action and Diagnosis-Opportunity Bias

## Leakage Risks

## Fit to Pre-Cardiology Risk Scoring

## Strengths

## Concerns

## Missing Information

## Implications for This Literature Review

## Recommended Follow-up
```

## Review Questions

### Label Summary
Ask:
- What exact label or outcome does the paper use?
- Is the label binary, multiclass, continuous, time-to-event, ordinal, or composite?
- Is there one primary label or multiple labels?
- Does the paper distinguish target construct from operational label?

Flag as a concern when:
- The paper uses broad terms such as "dementia prediction" without specifying what counts as dementia or prediction.
- Multiple label sources are combined without reporting how conflicts are handled.
- The label is described only in a table, appendix, or vague phrase.

### Target Construct
Classify the label as one or more:
- `current_unmet_cognitive_care_need`
- `current_undocumented_cognitive_impairment`
- `future_cognitive_impairment`
- `future_coded_dementia_diagnosis`
- `future_referral_or_testing`
- `future_care_pathway`
- `prevalent_known_dementia`
- `frailty_or_functional_status`
- `other`

Ask:
- Does the label aim to measure disease state, care need, diagnosis, documentation, testing, referral, or follow-up?
- Is the construct clinically meaningful for this project's problem statement?
- Is the construct compatible with pre-encounter risk scoring?

Flag as a concern when:
- A care-process label is interpreted as a disease-state label.
- A documentation label is interpreted as true prevalence or incidence.
- A future diagnosis label is treated as independent of post-index diagnostic opportunity.

### Label Source and Operational Definition
Ask:
- Is the label based on diagnosis codes, medications, cognitive tests, chart review, NLP, specialist diagnosis, claims, registry data, referral orders, or a composite?
- Are code lists, thresholds, phrases, criteria, or adjudication rules reported?
- Are label dates defined?
- Is the label source independent from predictor features?
- Are ambiguous or conflicting sources handled explicitly?

Flag as a concern when:
- Code lists or test thresholds are missing.
- Absence of codes is treated as absence of impairment without justification.
- The same note text appears likely to contribute both predictors and labels.

### Index Date and Label Timing
Ask:
- What is the index date or time origin?
- What label evidence is allowed before, at, or after the index date?
- Does the label define prevalent status, incident status, or future events?
- Is the prediction horizon specified?
- Are washout periods or clean baselines used?

Flag as a concern when:
- Label evidence may occur before predictors but is treated as future outcome.
- Post-index workup determines the label while the paper ignores differential workup.
- The index date is unclear enough that leakage cannot be assessed.

### Positive Case Definition
Ask:
- What evidence makes a patient or encounter positive?
- How many events, codes, tests, notes, or clinician judgments are required?
- Is a single code enough?
- Are dates, sequence, and recurrence considered?
- Are prevalent and incident cases separated?

Flag as a concern when:
- Positive cases require care contact that may vary by access or referral.
- Positive definitions are too sensitive for a clinical target without validation.
- Incident cases include people with prior evidence of impairment.

### Negative or Control Definition
Ask:
- What evidence makes a patient or encounter negative?
- Are negatives screened, chart-reviewed, followed long enough, or merely uncoded?
- Is there sufficient observation time to identify false negatives?
- Are controls drawn from the same source population as cases?
- Are patients with indeterminate evidence excluded or mislabeled negative?

Flag as a concern when:
- Non-cases are defined only by no diagnosis code.
- Follow-up time differs materially between positives and negatives.
- Controls may include unrecognized cognitive impairment.

### Indeterminate or Excluded Cases
Ask:
- Does the paper define uncertain labels?
- Are borderline cognitive scores handled?
- Are conflicting codes, medications, or chart evidence handled?
- Are patients with missing follow-up excluded, censored, or labeled negative?

Flag as a concern when:
- Ambiguous cases are silently forced into positive or negative classes.
- Exclusion rules create a selected sample unlike the intended deployment population.

### Label Validity Evidence
Ask:
- Does the paper validate labels against chart review, specialist assessment, cognitive tests, or an external registry?
- Are sensitivity, specificity, PPV, NPV, or inter-rater reliability reported?
- Does the paper cite validation studies for code-based definitions?
- Does the paper quantify label noise or uncertainty?

Flag as a concern when:
- Labels are treated as ground truth without validation or citation.
- The label source is known to have imperfect sensitivity and no sensitivity analysis is performed.
- The study's conclusions depend on a label that is only weakly supported.

### Misclassification Risks
Ask:
- Which false positives are plausible?
- Which false negatives are plausible?
- Are errors differential by age, sex, race, language, utilization, specialty access, or follow-up?
- Would misclassification inflate, attenuate, or redirect performance claims?

Flag as a concern when:
- Misclassification likely aligns with model predictors such as healthcare utilization.
- The paper reports discrimination without considering label noise.

### Downstream-Action and Diagnosis-Opportunity Bias
Ask:
- Could post-index referral, testing, specialist access, PCP follow-up, or documentation create the label?
- Could two clinically similar patients receive different labels because one was worked up and one was not?
- Does the paper measure opportunity for diagnosis?
- Does the paper distinguish cognitive outcome evidence from care-pathway evidence?

Flag as a concern when:
- A future diagnosis or referral label is interpreted as cognitive decline without accounting for diagnostic opportunity.
- The model may learn who receives evaluation rather than who has impairment.
- Follow-up completeness is ignored.

### Leakage Risks
Ask:
- Are predictor timestamps strictly before the intended decision point?
- Could outcome-defining notes, codes, tests, referrals, or medications be included as predictors?
- Are repeated encounters or repeated patients split across train and test in a way that leaks label information?
- Are labels built from the same text used for prediction?

Flag as a concern when:
- Within-encounter or post-index data could enter the input set.
- The paper does not report enough timing detail to rule out leakage.

### Fit to Pre-Cardiology Risk Scoring
Ask:
- Would this label be usable for an encounter-level model scored before a cardiology visit?
- What would the label mean in that use case?
- Does the label require post-cardiology action to be observed?
- What modification would make the label more useful for this project?

## Categorical Judgments
For each major domain, use one of:
- `adequate`
- `partial`
- `weak`
- `not_reported`
- `not_applicable`

In the `## Bottom Line`, classify the paper's label as one of:
- `label_construct_clear`
- `usable_with_caveats`
- `care_pathway_label`
- `high_misclassification_risk`
- `label_timing_unclear`
- `not_relevant_to_project_target`

## Definition of Done
This specialist review is complete when:
- `reviews/citation_key/label_definition_reviewer.md` exists.
- The review identifies what the label actually measures.
- The review separates target construct from operational label.
- Positive, negative, and indeterminate definitions are assessed.
- Timing, leakage, and downstream-action bias are explicitly addressed.
- Implications for this project's pre-cardiology-encounter risk-scoring target are stated.
