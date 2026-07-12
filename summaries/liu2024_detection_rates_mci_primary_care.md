---
citation_key: liu2024_detection_rates_mci_primary_care
summary_status: draft
source_status: full_text
paper_type: journal_article
publication_status: peer_reviewed_version_of_record
ml_ai_methods:
  uses_ml_ai: false
  method_families: ["other"]
  specific_methods: ["probit model", "observed-to-expected ratio"]
  learning_setup: ["statistical_association"]
  input_modalities: ["claims", "diagnosis_codes", "demographics", "cognitive_tests"]
  input_representation: ["engineered_features", "fixed_length_vector"]
  prediction_task: ["not_applicable"]
  temporal_handling: ["fixed_observation_window"]
  interpretability: ["coefficients"]
created: 2026-07-12
updated: 2026-07-12
---

# liu2024_detection_rates_mci_primary_care

## Bibliographic Record

Liu, Ying, Hannah Jun, Aaron Becker, Christopher Wallick, and Soeren Mattke. "Detection Rates of Mild Cognitive Impairment in Primary Care for the United States Medicare Population." The Journal of Prevention of Alzheimer's Disease 11, no. 1 (2024): 7-12. https://doi.org/10.14283/jpad.2023.131.

## Publication and Source Status

Peer-reviewed open-access journal article. The local source is the publisher PDF.

## Plain-Language Summary

This study estimates how often U.S. primary care clinicians and practices diagnose expected MCI cases among attributed Medicare beneficiaries. It compares observed MCI diagnoses in Medicare claims with expected rates derived from Health and Retirement Study cognitive assessment data. Average clinician and practice detection rates were about 0.08, meaning only about 8% of expected MCI cases were diagnosed on average.

## Structured Summary

### Research Question

What are MCI detection rates among U.S. primary care clinicians and practices caring for Medicare beneficiaries?

### Study Type

Observational study using Medicare administrative data and expected-rate modeling.

### Data Source

100% Medicare enrollment, claims, and encounter data for 2017-2019, plus Health and Retirement Study data from 2000-2016 for expected-rate modeling.

### Population

Medicare beneficiaries age 65 or older with near-continuous fee-for-service or Medicare Advantage enrollment, office visits with primary care clinicians, and attribution to clinicians/practices. Final analytic samples were 226,756 primary care clinicians and 54,597 practices with at least 25 attributed older patients.

### Index Date or Time Origin

Three-year window from 2017 to 2019.

### Observation Window

Medicare claims/encounters from 2017-2019; HRS data through 2016 for expected-rate model development.

### Prediction Horizon or Follow-up

Not a deployment prediction study. The study estimates observed and expected MCI diagnoses over a 3-year period.

### Inputs or Predictors

Expected-rate models used demographic variables available in both HRS and Medicare: sex, age group, race/ethnicity, dual eligibility, and year trend. Attribution used office visits and clinician/practice identifiers.

### Outcome or Target

MCI diagnosis based on ICD-10-CM G31.84, requiring two claims on separate days in the 2017-2019 window.

### Methods

The authors attributed beneficiaries to primary care clinicians and practices, estimated expected MCI rates using HRS cognitive classifications and probit models, and calculated clinician/practice detection rates as observed MCI diagnosis rate divided by expected rate. They classified whether observed rates were lower than, no different from, or higher than expected using confidence intervals.

### ML or AI Method Index

No ML/AI model was developed. The study used regression-based expected-rate estimation and observed-to-expected ratios.

### Model Inputs and Representations

The analytic unit is clinician or practice panel. Inputs are fixed tabular summaries and claims-derived diagnosis indicators. No clinical text or sequence modeling is used.

### Baselines or Comparators

Expected MCI rates from HRS-based models, compared with observed claims diagnosis rates. Specialty groups were compared descriptively.

### Evaluation

Prediction accuracy of the HRS-derived expected-rate model was evaluated against HRS cognitive/proxy classifications. Clinician/practice observed rates were compared with expected rates using confidence intervals.

### Main Findings

Average detection rates were 0.08 for both clinicians and practices. Only 0.1% of clinicians and practices had diagnosis rates within the expected range. Geriatric clinicians had higher average detection than other primary care specialties, but nearly all still had observed rates significantly lower than expected.

### Author-Stated Limitations

The authors state that the expected-rate model based on demographics alone had moderate accuracy; expected prevalence was based on cognitive test scores rather than true clinical diagnosis; the administrative-data MCI algorithm was modeled after CCW dementia logic but needs its own validation; assignment rules for patients with both MCI and dementia claims may misattribute some cases; and diagnoses may be communicated but not documented in claims.

### Funding, Conflicts, and Ethics

Partially funded by Genentech/Roche through a contract with USC. The USC IRB approved the study. Soeren Mattke and Christopher Wallick reported industry relationships; other authors reported no conflicts.

### Notes on Missing or Ambiguous Information

Supplemental methods and tables were referenced but not separately downloaded in this intake. The study's MCI label depends on claims documentation and may undercount clinically recognized but undocumented impairment.
