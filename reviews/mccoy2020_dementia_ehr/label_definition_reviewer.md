# Specialist Review: Label Definition

## Specialist Scope

Future coded dementia diagnosis after inpatient discharge.

## Bottom Line

The outcome is longitudinal and clinically relevant, but it measures future recorded diagnosis rather than true incident disease.

## Label Summary

Time to first inpatient or outpatient dementia diagnosis code.

## Target Construct

`future_coded_dementia_diagnosis`

## Label Source and Operational Definition

EHR diagnosis codes.

## Index Date and Label Timing

Hospital discharge is the index; dementia codes after index define incident events.

## Positive Case Definition

New dementia diagnosis code during follow-up.

## Negative or Control Definition

No dementia code before censoring, death, end of data, or eight years.

## Indeterminate or Excluded Cases

Patients with prior/current dementia code at index were excluded.

## Label Validity Evidence

No adjudicated cognitive reference standard is central to the outcome.

## Misclassification Risks

Uncoded dementia among negatives and nonspecific coding among positives.

## Downstream-Action and Diagnosis-Opportunity Bias

Patients whose discharge notes mention cognition may receive more diagnostic attention.

## Leakage Risks

Discharge notes may include early recognition of cognitive impairment that precedes formal coding.

## Fit to Pre-Cardiology Risk Scoring

Useful analogy for future diagnosis labels, not a cardiology encounter label.

## Strengths

Clear time-to-event design and exclusion of prior coded dementia.

## Concerns

Coded diagnosis is not independent of future care opportunity.

## Missing Information

Chart-validation performance of the dementia code outcome.

## Implications for This Literature Review

Carry forward distinction between disease state and coded diagnosis.

## Recommended Follow-up

Cite with diagnosis-opportunity caveat.
