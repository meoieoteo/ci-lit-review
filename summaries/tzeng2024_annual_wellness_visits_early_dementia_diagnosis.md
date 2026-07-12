---
citation_key: tzeng2024_annual_wellness_visits_early_dementia_diagnosis
summary_status: draft
source_status: full_text
paper_type: journal_article
publication_status: peer_reviewed_version_of_record
ml_ai_methods:
  uses_ml_ai: false
  method_families: ["survival_model", "logistic_regression"]
  specific_methods: ["propensity score matching", "Fine-Gray competing risk model"]
  learning_setup: ["statistical_association"]
  input_modalities: ["claims", "diagnosis_codes", "demographics", "procedures", "other"]
  input_representation: ["engineered_features", "fixed_length_vector"]
  prediction_task: ["not_applicable"]
  temporal_handling: ["fixed_observation_window", "time_to_event"]
  interpretability: ["coefficients"]
created: 2026-07-12
updated: 2026-07-12
---

# tzeng2024_annual_wellness_visits_early_dementia_diagnosis

## Bibliographic Record

Tzeng, Huey-Ming, Mukaila A. Raji, Yong Shan, Peter Cram, and Yong-Fang Kuo. "Annual Wellness Visits and Early Dementia Diagnosis Among Medicare Beneficiaries." JAMA Network Open 7, no. 10 (2024): e2437247. https://doi.org/10.1001/jamanetworkopen.2024.37247.

## Publication and Source Status

Peer-reviewed JAMA Network Open article. The local source is full-text PMC HTML because the publisher PDF endpoint was blocked and the PMC article page did not expose a main PDF link during intake.

## Plain-Language Summary

This study evaluates whether Medicare annual wellness visits are associated with earlier first diagnosis of MCI or ADRD. In Texas fee-for-service Medicare beneficiaries, receipt of an incident annual wellness visit in 2018 was associated with a higher hazard of first MCI diagnosis during follow-up and a smaller association with first ADRD diagnosis. The authors interpret this as evidence that annual wellness visits may support earlier recognition of cognitive impairment.

## Structured Summary

### Research Question

What is the association between incident annual wellness visit receipt and first MCI or ADRD diagnosis among older adults with Medicare fee-for-service benefits?

### Study Type

Retrospective population-based cohort study.

### Data Source

100% Texas Medicare fee-for-service administrative data from 2015 to 2022, including beneficiary summary files, inpatient files, outpatient claims, and carrier files.

### Population

Community-dwelling Texas Medicare fee-for-service beneficiaries aged 68 or older in 2018 with complete Parts A and B and no Medicare Advantage enrollment for 2015-2018, excluding prior MCI/ADRD diagnosis and prior AWV in 2015-2017. Final cohort: 549,516 beneficiaries.

### Index Date or Time Origin

For AWV recipients, the first AWV date in 2018. For non-AWV recipients, a randomly assigned index month matched to the AWV cohort's month distribution, using the 15th day of that month.

### Observation Window

Baseline exclusions and covariates used 2015-2017 and the 12 months before index; outcomes were followed from index date in 2018 through December 31, 2022.

### Prediction Horizon or Follow-up

Follow-up from index date through the end of 2022, censored for end of study, loss of Parts A/B, Medicare Advantage switch, or competing death.

### Inputs or Predictors

Primary exposure was AWV receipt in 2018. Covariates included demographics, race/ethnicity, county/zip code characteristics, original Medicare entitlement, dual eligibility, Elixhauser comorbidity count, hospitalizations, neurologist visits, psychiatric visits, PCP presence, rural-urban classification, high-school graduation rate, physical inactivity, and social association rate.

### Outcome or Target

First MCI or ADRD diagnosis after index, reported as combined MCI/ADRD, MCI alone, and ADRD alone. ADRD was based on CMS Chronic Conditions Data Warehouse diagnosis-code algorithms; MCI used ICD-9-CM 331.83 and ICD-10-CM G31.84 as reported in the paper.

### Methods

The authors used 1:1 propensity score matching with exact matching on AWV month and conditional Fine-Gray competing risk models. Sensitivity analyses censored follow-up AWV changes and treated AWV as a time-dependent exposure.

### ML or AI Method Index

No ML/AI model was developed. The analysis used propensity score matching and competing-risk regression.

### Model Inputs and Representations

The analytic unit is beneficiary. Inputs are fixed tabular baseline features and time-to-event outcomes. No clinical text or variable-length EHR sequence modeling is used.

### Baselines or Comparators

AWV recipients were compared with propensity-score-matched beneficiaries who did not receive an AWV in 2018.

### Evaluation

The study reports standardized differences after matching, cumulative incidence functions, hazard ratios with 95% confidence intervals, and two sensitivity analyses.

### Main Findings

Among 549,516 beneficiaries, 66,433 had an incident AWV in 2018. After matching, AWV receipt was associated with higher first MCI diagnosis (HR 1.21, 95% CI 1.16-1.27) and slightly higher first ADRD diagnosis (HR 1.04, 95% CI 1.02-1.06). In sensitivity analyses, the association with MCI was larger, while the association with ADRD was small or nonsignificant.

### Author-Stated Limitations

The authors note possible patient self-selection into AWVs, limited generalizability outside Texas fee-for-service Medicare, reliance on billing data, lack of information on how AWVs were performed or referrals facilitated, and absence of patient-level education, marital status, living arrangement, physical activity, and social-life information.

### Funding, Conflicts, and Ethics

Funded by National Institute on Aging grant 1R01AG083102-01. No conflicts of interest were reported. The University of Texas Medical Branch IRB approved the study and waived consent because data were deidentified.

### Notes on Missing or Ambiguous Information

The summary is based on full-text HTML. The main PDF and supplements were not downloaded locally.
