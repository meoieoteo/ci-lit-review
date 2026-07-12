---
citation_key: mattke2023_expected_diagnosed_mci_dementia_medicare
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

# mattke2023_expected_diagnosed_mci_dementia_medicare

## Bibliographic Record

Mattke, Soeren, Hannah Jun, Esther Chen, Ying Liu, Aaron Becker, and Christopher Wallick. "Expected and diagnosed rates of mild cognitive impairment and dementia in the U.S. Medicare population: observational analysis." Alzheimer's Research & Therapy 15, no. 1 (2023): 128. https://doi.org/10.1186/s13195-023-01272-z.

## Publication and Source Status

Peer-reviewed open-access journal article. The local source is the publisher PDF.

## Plain-Language Summary

This study compares how often MCI and dementia are documented in Medicare claims with expected rates estimated from Health and Retirement Study cognitive assessment data. It finds that documented MCI diagnoses capture only a small fraction of expected MCI cases, while dementia diagnoses are closer to or above expected rates overall. Detection differs by race/ethnicity, dual eligibility, and Medicare coverage type.

## Structured Summary

### Research Question

How do documented Medicare diagnosis rates for MCI and dementia compare with expected rates estimated from cognitive assessment data?

### Study Type

Observational analysis of Medicare claims and survey-derived expected prevalence.

### Data Source

100% Medicare fee-for-service and Medicare Advantage claims/encounter and enrollment data from 2015 to 2019, linked conceptually to Health and Retirement Study data from 2000 to 2016 for expected-rate modeling.

### Population

Medicare beneficiaries aged 65 or older with nearly continuous enrollment over rolling 3-year windows or until death. The 2017-2019 window included 41,205,474 beneficiaries.

### Index Date or Time Origin

Rolling 3-year observation windows: 2015-2017, 2016-2018, and 2017-2019.

### Observation Window

Three-year Medicare claims windows; HRS waves from 2000-2016 for expected-rate model development.

### Prediction Horizon or Follow-up

Not a prediction study in the clinical deployment sense. The study estimates expected prevalence/detection rates within observation windows.

### Inputs or Predictors

HRS expected-rate models used sex, age group, race/ethnicity, dual eligibility, and secular year trend. Medicare observed rates used diagnosis codes in claims/encounters.

### Outcome or Target

Observed MCI and dementia diagnoses in Medicare claims. MCI used ICD-10 G31.84 and ICD-9 331.83 with two claims on separate days. Dementia used a modified Chronic Conditions Data Warehouse algorithm.

### Methods

The authors used HRS cognitive classifications to estimate expected MCI/CIND and dementia rates, then applied model weights to Medicare data. Detection rate was defined as observed claims diagnosis rate divided by expected rate.

### ML or AI Method Index

No ML/AI model was developed. The study used probit models and observed-to-expected ratios.

### Model Inputs and Representations

The analytic unit is beneficiary in a 3-year window. Inputs are fixed demographic features and claims diagnosis indicators. No clinical text, longitudinal sequence modeling, or embeddings are used.

### Baselines or Comparators

Observed Medicare diagnosis rates were compared with expected rates from HRS-based cognitive assessment models. Subgroup comparisons included age, sex, race/ethnicity, dual eligibility, fee-for-service, and Medicare Advantage.

### Evaluation

The HRS model was calibrated using 2000-2014 data and assessed against 2016 HRS participants. Reported AUROC was 0.670 for MCI/CIND versus normal and 0.772 for dementia versus normal.

### Main Findings

MCI detection rates increased from 0.062 to 0.079 across rolling windows, implying that most expected MCI cases were undiagnosed. In 2017-2019, MCI detection was 0.098 among non-Hispanic White beneficiaries, 0.039 among Black beneficiaries, and 0.048 among Hispanic beneficiaries. Dementia was diagnosed more frequently than expected overall, but detection was lower for Black and Hispanic beneficiaries than for non-Hispanic White beneficiaries.

### Author-Stated Limitations

The authors state that the predictive model used limited demographic information and had only adequate accuracy; expected MCI was based on cognitive test scores rather than clinical diagnosis; dementia expected rates may be underpredicted; HRS cognitive classification may overclassify dementia in minority populations; claims algorithms may misclassify cases; plan switching was not modeled; and some diagnoses may be communicated but not documented in claims.

### Funding, Conflicts, and Ethics

Funded by a contract from Genentech to the University of Southern California. Medical writing support was funded by Genentech. The USC IRB approved the study with waiver of consent and HIPAA authorization. Soeren Mattke and Christopher Wallick reported industry relationships, including Genentech/Roche-related interests; other authors reported no conflicts.

### Notes on Missing or Ambiguous Information

Supplemental material was referenced but not separately downloaded in this intake. The study uses CIND from HRS as the analogue for MCI.
