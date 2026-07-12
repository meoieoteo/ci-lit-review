# Specialist Review: Label Definition

## Specialist Scope

Assessment of whether Steinberg et al. contributes label-definition evidence relevant to cognitive-risk modeling.

## Bottom Line

`not_applicable` for dementia labels. The paper defines five operational clinical prediction outcomes clearly enough for its representation-learning experiments, but none are cognitive, dementia, MCI, referral, testing, or care-pathway labels.

## Label Summary

The outcomes are inpatient mortality, long admission, ICU transfer the following day, 30-day readmission, and abnormal HbA1c in a non-diabetic patient.

## Target Construct

`other`. These are general clinical prediction outcomes used to test representation learning.

## Label Source and Operational Definition

Labels come from structured EHR events and lab-result context. The paper gives concise definitions and prediction times in Table 1.

## Index Date and Label Timing

Timing is outcome-specific and clearly stated: admission, discharge, each inpatient day, or before an HbA1c result is returned.

## Positive Case Definition

Operational event definitions are reported for each outcome.

## Negative or Control Definition

Non-events within the task-specific source populations are treated as negatives.

## Indeterminate or Excluded Cases

Not central to the paper and not discussed in detail.

## Label Validity Evidence

The paper does not focus on label validation. It uses outcomes as benchmark tasks.

## Misclassification Risks

Not reviewed in depth because labels are not central to this paper's relevance for this project.

## Downstream-Action and Diagnosis-Opportunity Bias

Not addressed.

## Leakage Risks

The temporal split and outcome-specific prediction times reduce obvious leakage risk, but this review did not find a detailed leakage audit.

## Fit to Pre-Cardiology Risk Scoring

The paper's timing discipline is useful by analogy; its labels are not directly useful.

## Strengths

- Prediction times are stated.
- Temporal train/development/test split is used.

## Concerns

- No relevance to dementia label construction.
- No discussion of clinical label validity.

## Missing Information

Detailed outcome-code definitions and event-extraction logic are not the paper's focus.

## Implications for This Literature Review

Do not cite this paper for label construction. Use it only as structured-EHR representation context.

## Recommended Follow-up

None for label definition.
