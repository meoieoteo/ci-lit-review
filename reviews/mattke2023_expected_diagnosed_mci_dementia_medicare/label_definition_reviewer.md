# Specialist Review: Label Definition

## Specialist Scope

Assessment of MCI/dementia diagnosis labels and expected-vs-observed detection.

## Bottom Line

usable_with_caveats. The paper is valuable because it shows diagnosis labels are incomplete; the labels themselves should not be treated as disease truth.

## Label Summary

Observed labels are claims-documented MCI and dementia. Expected labels are model-estimated cognitive states from HRS.

## Target Construct

`current_undocumented_cognitive_impairment`; `future_coded_dementia_diagnosis`; `prevalent_known_dementia`

## Label Source and Operational Definition

MCI requires two claims with ICD-10 G31.84 or ICD-9 331.83 on separate days. Dementia uses a modified CCW algorithm.

## Index Date and Label Timing

Rolling three-year observation windows from 2015-2019.

## Positive Case Definition

Two claims for MCI on separate days or dementia by modified CCW algorithm.

## Negative or Control Definition

Absence of documented diagnosis within claims window; not a confirmed negative.

## Indeterminate or Excluded Cases

Overlapping MCI/dementia cases were assigned by midpoint-year/latest-claim rules.

## Label Validity Evidence

Expected rates are based on HRS cognitive/proxy assessments and Langa-Kabeto-Weir classifications. Claims algorithms are cited, but MCI claims label is not independently validated here.

## Misclassification Risks

MCI false negatives are substantial. Dementia coding may overdiagnose overall but underdetect in some subgroups.

## Downstream-Action and Diagnosis-Opportunity Bias

High. Documented diagnosis depends on detection, documentation, coverage, and likely care access.

## Leakage Risks

Not a prediction model. For this project, future claims diagnosis should not be treated as independent of post-index diagnosis opportunity.

## Fit to Pre-Cardiology Risk Scoring

Strong caution for label design. Supports avoiding uncoded controls as true negatives.

## Strengths

National Medicare coverage, expected-vs-observed framing, subgroup results.

## Concerns

Expected MCI is based on CIND/cognitive tests, not clinical diagnosis; model accuracy is moderate.

## Missing Information

Supplemental code lists and algorithm details need source check before replication.

## Implications for This Literature Review

Core evidence for label misclassification and diagnosis opportunity.

## Recommended Follow-up

Use to justify indeterminate/unknown cognitive status rather than labeling uncoded patients negative.
