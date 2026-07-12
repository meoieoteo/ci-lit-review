# Specialist Review: Label Definition

## Specialist Scope

Assessment of the dementia labels and probable-undetected-dementia target.

## Bottom Line

usable_with_caveats. The paper is unusually explicit that ICD codes are an imperfect silver standard, but the development label still depends on specialty-clinic coding and the validation label relies on retrospective chart review of sampled controls.

## Label Summary

The development label is binary coded dementia case versus uncoded control. The validation label for sampled controls is chart-review classification as dementia, non-dementia, or unclear.

## Target Construct

The most relevant construct is `current_undocumented_cognitive_impairment` or probable undiagnosed dementia. The development label also includes `prevalent_known_dementia`.

## Label Source and Operational Definition

Cases required at least one specialty-clinic dementia ICD-9 code from a specified list, first diagnosis at age 65 or older, and sufficient prior notes. Controls had no dementia-related diagnoses and no anti-dementia medications over the three-year period.

## Index Date and Label Timing

For cases, predictors came from the three years before first dementia diagnosis. For controls, predictors came from three years before a random visit index date. Chart-review validation examined notes within the three-year analysis period.

## Positive Case Definition

Positive cases for development were specialty-coded dementia cases. Positive cases in validation were controls judged by dementia specialists to show dementia signs consistent with DSM-5 guidance.

## Negative or Control Definition

Controls were defined by absence of dementia diagnosis codes and anti-dementia medications. This is intentionally imperfect because the study's goal was to find undiagnosed cases within that group.

## Indeterminate or Excluded Cases

The validation review allowed an "unclear" category. Sensitivity and specificity were reported under two assumptions: unclear as dementia and unclear as non-dementia.

## Label Validity Evidence

Two dementia specialists manually reviewed records. The initial 20-subject review had high agreement between ICD-coded dementia status and clinician-assigned diagnosis. The 120-control validation sample was also manually reviewed.

## Misclassification Risks

False negatives are expected among uncoded controls. False positives may occur among patients with nonspecific cognitive symptoms, delirium, depression, medication effects, or documentation suggestive of cognitive concerns without dementia.

## Downstream-Action and Diagnosis-Opportunity Bias

Substantial. Specialty-clinic coded dementia depends on referral, evaluation, and documentation. The paper recognizes underdiagnosis but does not measure diagnosis opportunity or care access.

## Leakage Risks

The paper excludes the first diagnosis date from case predictors, but the three-year notes may include prediagnostic cognitive workup, clinician concern, or referral-related documentation. For the project's encounter-level design, stricter pre-cardiology cutoffs would be needed.

## Fit to Pre-Cardiology Risk Scoring

Partial. The label concept is relevant to current unmet cognitive care need, but the paper is patient-level and not tied to cardiology encounters.

## Strengths

- Explicitly distinguishes ICD codes from true dementia status.
- Uses chart review to validate likely undiagnosed cases.
- Handles unclear validation labels transparently.

## Concerns

- Development positives depend on specialty-clinic diagnosis opportunity.
- Controls are initially uncoded rather than confirmed dementia-free.
- Chart review from EHR notes is not equivalent to direct cognitive assessment.

## Missing Information

- Detailed adjudication criteria for difficult chart-review cases.
- Whether post-referral or workup notes were present before index.
- Label performance by demographic or utilization subgroup.

## Implications for This Literature Review

This is a strong label-design example because it makes the "absence of code is not absence of dementia" problem operational.

## Recommended Follow-up

Use as a source-check priority for label-definition and diagnosis-opportunity sections.
