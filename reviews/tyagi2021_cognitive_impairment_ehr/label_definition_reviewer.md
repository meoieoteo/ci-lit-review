# Specialist Review: Label Definition

## Specialist Scope

Annotated note-sequence evidence of cognitive impairment.

## Bottom Line

The label is useful for NLP extraction but is not a patient-level disease or risk label.

## Label Summary

Sequence-level Yes/No/Neither labels for cognitive impairment evidence.

## Target Construct

`current_undocumented_cognitive_impairment`; `other`

## Label Source and Operational Definition

Human annotation of keyword-centered note snippets.

## Index Date and Label Timing

No patient-level index date is defined.

## Positive Case Definition

Text sequence contains evidence of MCI or dementia.

## Negative or Control Definition

Text sequence does not contain cognitive impairment evidence.

## Indeterminate or Excluded Cases

Neither class captures non-decisive text.

## Label Validity Evidence

Annotation provides a task-specific reference standard; full reliability details are limited in the short source.

## Misclassification Risks

Snippet context may omit temporality, negation, or longitudinal evidence.

## Downstream-Action and Diagnosis-Opportunity Bias

Keyword sampling favors already documented cognitive concerns.

## Leakage Risks

Not a future-risk design; labels and predictors are the same text segment.

## Fit to Pre-Cardiology Risk Scoring

Useful as an extractor component, not as an outcome label.

## Strengths

Separates cognitive impairment evidence from concern alone.

## Concerns

Sequence-level label cannot be interpreted as patient status.

## Missing Information

Detailed annotation reliability and patient-level aggregation.

## Implications for This Literature Review

Helps define note evidence labels for concept extraction.

## Recommended Follow-up

Use only for NLP feature-label design.
