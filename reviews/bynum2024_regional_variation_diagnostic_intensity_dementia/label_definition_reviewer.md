# Specialist Review: Label Definition

## Specialist Scope

Assessment of ADRD diagnosis as an outcome label and diagnosis-intensity as a label-observation construct.

## Bottom Line

usable_with_caveats. The operational label is clear as a new claims-coded ADRD diagnosis, and the paper is useful precisely because it does not equate diagnosed ADRD with true ADRD incidence.

## Label Summary

The label is new ADRD diagnosis in 2019 based on a validated ICD-10-CM claims algorithm.

## Target Construct

`future_coded_dementia_diagnosis`; `future_care_pathway`; indirectly `diagnosis_opportunity`.

## Label Source and Operational Definition

Inpatient, professional outpatient, selected outpatient hospital, home health, and hospice claims. The exact algorithm is cited to prior validated work and supplements.

## Index Date and Label Timing

Calendar year 2019; 2018 is a lookback year to distinguish new from existing ADRD diagnosis.

## Positive Case Definition

Beneficiaries with an ADRD diagnosis identified by the claims algorithm in 2019 and not already identified during the lookback period.

## Negative or Control Definition

Beneficiaries without new ADRD diagnosis in 2019. This means "not coded as newly diagnosed," not proven dementia-free.

## Indeterminate or Excluded Cases

The paper does not define indeterminate dementia status; the analysis is claims-based.

## Label Validity Evidence

The ADRD algorithm is described as validated and cited, but this study does not perform new chart/cognitive-test validation.

## Misclassification Risks

False negatives include undiagnosed or undocumented dementia. False positives may occur through coding errors or nonspecific diagnosis use.

## Downstream-Action and Diagnosis-Opportunity Bias

This is the core contribution. The paper measures variation in diagnostic intensity and argues that observed diagnosis rates reflect more than underlying population risk.

## Leakage Risks

Not relevant to a prediction feature/label split. For this project, the lesson is that post-index coded dementia outcomes could reflect post-index diagnostic opportunity.

## Fit to Pre-Cardiology Risk Scoring

High as label-bias evidence, not as a direct label design. It supports modeling or stratifying diagnosis opportunity if the project uses future coded diagnosis.

## Strengths

- Explicit observed-to-expected diagnosis-intensity framing.
- Separates diagnosed cases from underlying risk.
- Subgroup and geography analyses are directly relevant to label observability.

## Concerns

- Claims diagnosis remains an imperfect proxy.
- Expected rates are model-based rather than adjudicated true incidence.
- Causes of regional variation remain unresolved.

## Missing Information

Full supplement/code-list source check if used for exact operational replication.

## Implications for This Literature Review

Use as a central Section 5 citation for diagnosis-opportunity bias and "diagnostic intensity."

## Recommended Follow-up

Extract exact ADRD code algorithm from supplement or cited validation paper before manuscript methods claims.
