# Primary Review: spoto2025_diagnostic_signal_decay_dementia

## Review Status

primary_complete

## Citation Key

`spoto2025_diagnostic_signal_decay_dementia`

## Core Question

Does the paper help explain why dementia diagnosis labels can vary across care settings, regions, and documentation practices rather than reflecting only underlying cognitive disease?

## Answer

Yes. The paper directly supports the idea that dementia diagnosis codes can change, degrade, or become less specific across repeated hospitalizations and that geographic and demographic context is associated with coding-pattern differences. It is, however, an arXiv preprint and should carry lower publication weight than peer-reviewed Section 5 evidence.

## Relevance to Problem Statement

The paper strengthens the review's concern that coded dementia outcomes are partly documentation artifacts. In a cardiology pre-encounter prediction project, a future dementia diagnosis code is not just a disease event; it is also a function of hospitalization, coding specificity, regional coding norms, and patient access to diagnostic workup.

## Evidence Most Relevant to This Review

- The study analyzes Medicare inpatient dementia diagnosis coding patterns among older fee-for-service beneficiaries.
- Non-specific dementia codes dominate inpatient dementia documentation, appearing in more than three quarters of dementia-coded hospitalizations.
- Temporal sequence mining identified movement from more specific codes, including Alzheimer disease codes, toward non-specific dementia codes in subsequent hospitalizations.
- State and county analyses suggest that local coding-pattern similarity varies geographically and is associated with rurality, Medicaid eligibility, and racial/ethnic composition.
- The paper frames this phenomenon as diagnostic signal decay: clinically meaningful information may be weakened or lost as diagnoses move through administrative documentation.

## Study Design Notes

The cohort is based on Medicare Part A MedPAR inpatient claims from 2016-2018 for beneficiaries aged 65 years or older with at least one hospitalization containing a dementia ICD-10 code. The analysis is not a prospective prediction study and not an EHR text study.

## Label and Outcome Implications

This paper is useful for arguing that dementia diagnosis codes have specificity problems in addition to sensitivity problems. A patient may move from specific to non-specific coding over time, and the absence of a specific Alzheimer disease code does not necessarily mean absence of Alzheimer disease.

## Downstream-Action and Diagnosis-Opportunity Implications

The paper supports treating coded dementia outcomes as products of clinical contact and coding practice. Hospitalization generates opportunities for coding, but inpatient claims may favor problem-list carry-forward, billing conventions, and non-specific dementia categories rather than etiologic precision.

## Limitations for This Review

- Preprint status means lower publication weight.
- Inpatient Medicare Part A claims are not outpatient EHR data.
- Hospitalized dementia patients are likely older, sicker, and later-stage than patients at a cardiology encounter.
- The methods cannot determine whether coding changes are clinically warranted or administrative artifacts.
- Geographic associations are ecological and need patient- and system-level validation.

## How to Use in the Literature Review

Cite as direct but lower-weight support for Section 5's argument that diagnosis-code outcomes are affected by coding specificity, geography, and documentation context. It should not be a primary anchor for prevalence, clinical diagnosis validity, or cardiology workflow.

## Claims to Carry Forward

- Dementia code specificity can degrade over time in inpatient claims.
- Non-specific dementia codes are common in Medicare hospitalizations.
- Regional coding-pattern variation is relevant to interpreting dementia-coded outcomes.

## Claims to Treat Cautiously

- Exact estimates of signal decay outside inpatient Medicare claims.
- Any claim that observed code transitions prove true clinical diagnostic deterioration or improvement.
- Any direct translation to outpatient cardiology EHRs without local validation.

## Recommended Follow-Up

Use this paper to motivate sensitivity analyses around diagnosis-code specificity and care-setting source of outcome ascertainment.
