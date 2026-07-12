# Specialist Review: Label Definition

## Specialist Scope

Assessment of the dementia-risk label, control definition, timing, and downstream-action risks in Li et al.

## Bottom Line

`usable_with_caveats`. The target is clear at a high level: future incident dementia diagnosis versus no dementia/MCI diagnosis. It is useful for studying future coded dementia risk, but it is not an adjudicated cognitive-impairment label and is vulnerable to diagnosis-opportunity and false-negative control problems.

## Label Summary

The label is binary: incident dementia case status versus matched control status. Cases had incident dementia; patients with prior dementia or MCI were excluded from the case cohort. Controls had no dementia or MCI diagnosis and were matched to cases by sex, race, and age within five years of the matching case's disease index date.

## Target Construct

The construct is closest to `future_coded_dementia_diagnosis`. It is not directly `current_unmet_cognitive_care_need`, `current_undocumented_cognitive_impairment`, or adjudicated future cognitive impairment.

## Label Source and Operational Definition

The source appears to be EHR diagnosis status in INPC. The main article does not report the exact dementia/MCI code list, diagnostic algorithm, number of codes required, provider type, encounter type, or how conflicting evidence was handled.

## Index Date and Label Timing

Cases have a disease index date. Controls are matched within five years of the case disease index date. Inputs are notes from one- or two-year observation periods before the prediction horizon. Prediction horizons are six months and one year. The paper is reasonably clear about window lengths but not about the exact operational timestamp of incident dementia.

## Positive Case Definition

Positive cases are patients with incident dementia. Prior MCI or dementia excludes patients from the case cohort. The paper does not state whether incident dementia required one code, repeated codes, problem-list entry, specialist diagnosis, or another rule.

## Negative or Control Definition

Controls have no dementia or MCI diagnosis and are matched to cases. This is a weak negative definition for true cognitive status because controls may include patients with undocumented or unrecognized cognitive impairment.

## Indeterminate or Excluded Cases

Patients with MCI or previous dementia are excluded from the case cohort. The paper does not describe indeterminate cases, ambiguous cognitive symptoms, borderline evidence, or controls with cognitive complaints but no code.

## Label Validity Evidence

No chart review, cognitive test reference standard, specialist adjudication, or cited validation performance for the incident dementia label is reported in the main text. Label validity is therefore partial for coded diagnosis and weak for true disease state.

## Misclassification Risks

False negatives are plausible among controls with unrecognized cognitive impairment or insufficient diagnostic opportunity. False positives are possible if dementia codes are nonspecific, rule-out, historical, or administratively carried forward. Differential misclassification could track utilization, specialty access, primary-care continuity, race, age, and documentation intensity.

## Downstream-Action and Diagnosis-Opportunity Bias

The label depends on a future dementia diagnosis. Two similar patients could differ in label status because one had more follow-up, screening, referral, or documentation. The paper does not measure diagnostic opportunity or adjust for care-pathway differences.

## Leakage Risks

The explicit observation windows and prediction horizons reduce leakage risk compared with vague designs. Remaining risk depends on how the disease index date is operationalized and whether notes shortly before diagnosis contain diagnostic workup, cognitive testing plans, or near-label language. This risk is higher for the six-month horizon than for longer horizons.

## Fit to Pre-Cardiology Risk Scoring

The timing design is useful for a pre-cardiology risk model, but the label would need adaptation. For this project, future coded dementia diagnosis should be separated from current unmet cognitive care need and from post-index cardiology-triggered diagnostic workup.

## Strengths

- Explicit observation periods and prediction horizons.
- Controls matched on age, sex, and race.
- Prior dementia and MCI excluded from cases.
- Notes are restricted to pre-horizon observation windows.

## Concerns

- Exact dementia and MCI label algorithms are not reported in the main text.
- Controls are diagnosis-negative, not cognitively adjudicated negative.
- Future diagnosis is a documentation and care-opportunity outcome.
- Case-control downsampling changes prevalence and deployment interpretation.

## Missing Information

- Dementia and MCI code lists.
- Number and timing of codes required for incident dementia.
- Whether diagnosis sources include inpatient, outpatient, problem list, claims, or mixed EHR domains.
- Follow-up requirements for controls.
- Label validation against cognitive testing or chart review.

## Implications for This Literature Review

Use this paper to support notes-only future dementia diagnosis prediction with explicit timing, but cite it cautiously in label-validity discussions. It is a good example of why future diagnosis labels must be treated as observable care-pathway outcomes unless validated.

## Recommended Follow-up

Source-check supplements or linked repository material for diagnosis-code definitions and cohort-construction code before using exact label claims.
