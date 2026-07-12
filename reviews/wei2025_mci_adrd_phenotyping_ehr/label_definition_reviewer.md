# Specialist Review: Label Definition

## Specialist Scope

Assessment of the MCI/ADRD chart-review label in Wei et al.

## Bottom Line

`label_construct_clear`. The paper defines a clinically relevant MCI/ADRD diagnosis phenotype using manual chart review, which is stronger than code-only labels. Caveats are single-reviewer labeling, uncertain-case exclusion, and no subtype/severity label.

## Label Summary

The primary outcome is binary confirmed MCI or ADRD diagnosis by manual chart review.

## Target Construct

`prevalent_known_dementia` and MCI/ADRD case-finding. It is not future risk prediction.

## Label Source and Operational Definition

A neurologist manually reviewed notes in four MED/ICD sampling strata and assigned final yes/no MCI/ADRD status. A web-based tool highlighted keywords in notes. Cases marked uncertain were excluded.

## Index Date and Label Timing

The paper is visit/patient phenotyping rather than pre-index prediction. If a patient had medication or ICD records, only notes after first medication or ICD evidence were selected. ICD assignment allowed one day before and after a visit.

## Positive Case Definition

Manual chart-review positive for MCI/ADRD.

## Negative or Control Definition

Manual chart-review negative for MCI/ADRD.

## Indeterminate or Excluded Cases

112 uncertain manually annotated cases, accounting for 765 visits, were excluded.

## Label Validity Evidence

Manual neurologist chart review is a meaningful reference standard relative to ICD-only phenotyping. However, no inter-rater reliability, adjudication process, or independent second-reviewer validation is reported.

## Misclassification Risks

Uncertain-case exclusion likely improves apparent label clarity but may reduce generalizability to ambiguous real-world patients. False positives often involved cognitive-like symptoms from alternative causes. False negatives often involved sparse mentions by non-cognitive specialists.

## Downstream-Action and Diagnosis-Opportunity Bias

The label identifies documented diagnosis status. It does not solve under-recognition in patients with no clinical documentation. Stratified sampling helps evaluate hidden positives in MED-/ICD- patients, but the target remains documented chart evidence.

## Leakage Risks

Because notes used as predictors are also the chart-review source, the model may learn explicit diagnosis terms used to create the label. This is acceptable for phenotyping but would be leakage for future pre-diagnosis risk prediction.

## Fit to Pre-Cardiology Risk Scoring

Useful for creating or validating labels from chart evidence, but not directly usable as a pre-cardiology future-risk label.

## Strengths

- Manual chart-review reference standard.
- Includes MED-/ICD- stratum, allowing discovery beyond obvious code/medication positives.
- Excludes uncertain cases rather than forcing them into binary labels.
- Reports error analysis.

## Concerns

- Single neurologist reviewer is reported.
- No inter-rater reliability.
- Uses same note corpus as label source and predictor source.
- No subtype or severity distinction.

## Missing Information

Annotation guide details, adjudication rules, inter-rater reliability, and exact handling of conflicting chart evidence.

## Implications for This Literature Review

Wei is valuable for the label-definition section because it demonstrates a stronger-than-code-only chart-review phenotype and documents why ICD-only phenotyping can fail.

## Recommended Follow-up

Use as a model for local validation sampling, but design local review with double annotation, adjudication, and an indeterminate class.
