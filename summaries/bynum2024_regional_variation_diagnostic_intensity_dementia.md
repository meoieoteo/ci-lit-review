---
citation_key: bynum2024_regional_variation_diagnostic_intensity_dementia
summary_status: draft
source_status: full_text
paper_type: journal_article
publication_status: peer_reviewed_version_of_record
ml_ai_methods:
  uses_ml_ai: false
  method_families: ["other"]
  specific_methods: ["Poisson regression", "mixed-effects model", "observed-to-expected diagnostic intensity"]
  learning_setup: ["statistical_association"]
  input_modalities: ["claims", "diagnosis_codes", "demographics", "other"]
  input_representation: ["engineered_features", "fixed_length_vector"]
  prediction_task: ["not_applicable"]
  temporal_handling: ["fixed_observation_window"]
  interpretability: ["coefficients"]
created: 2026-07-12
updated: 2026-07-12
---

# bynum2024_regional_variation_diagnostic_intensity_dementia

## Bibliographic Record

Bynum, Julie P. W., Slim Benloucif, Jonathan Martindale, A. James O'Malley, and Matthew A. Davis. "Regional variation in diagnostic intensity of dementia among older U.S. adults: An observational study." Alzheimer's & Dementia 20, no. 10 (2024): 6755-6764. https://doi.org/10.1002/alz.14092.

## Publication and Source Status

Peer-reviewed journal article. The local source is the PMC full-text HTML because direct PDF download was blocked or unavailable during intake. The article is open access under a CC BY-NC-ND license according to the source page.

## Plain-Language Summary

This study asks whether older adults' likelihood of receiving a new Alzheimer's disease and related dementias (ADRD) diagnosis differs by where they live after accounting for regional population risk. Using Medicare fee-for-service claims and hospital referral regions, the authors estimate expected new ADRD diagnoses and compare them with observed diagnoses. They find that diagnosis intensity varies substantially across regions and that the variation is largest for adults aged 66-74 and for Black and Hispanic groups.

## Structured Summary

### Research Question

Do new ADRD diagnosis rates vary across U.S. health care markets after adjusting for demographics, education, health risk factors, and general diagnostic intensity?

### Study Type

Observational study of regional variation using Medicare claims.

### Data Source

2018-2019 Medicare fee-for-service claims from a 20% Master Beneficiary Summary File sample, plus regional measures from U.S. Census/ACS, BRFSS, U.S. Diabetes Surveillance System, and a published general diagnostic-intensity measure.

### Population

Adults age 66 or older in fee-for-service Medicare, enrolled in Parts A and B in 2018 and 2019 or until death, residing in a U.S. hospital referral region. The final sample contained 4,842,034 beneficiaries.

### Index Date or Time Origin

Calendar year 2019 for new ADRD diagnosis, with 2018 used as a lookback year to distinguish new from existing diagnosis.

### Observation Window

Claims from January 1, 2018 through December 31, 2019.

### Prediction Horizon or Follow-up

Not a prediction study. The outcome was new ADRD diagnosis in 2019.

### Inputs or Predictors

Hospital referral region population composition, including age, sex, race/ethnicity, education, smoking, obesity, diabetes, and a general diagnostic-intensity measure.

### Outcome or Target

New ADRD diagnosis in 2019 based on a validated ICD-10-CM claims algorithm applied to inpatient, outpatient/professional, home health, and hospice claims.

### Methods

The authors calculated regional new ADRD diagnosis rates, used Poisson regression to estimate expected new ADRD cases by hospital referral region, and defined ADRD-specific diagnosis intensity as observed divided by expected new ADRD cases. Mixed-effect models estimated the individual probability of new ADRD diagnosis by regional diagnostic intensity.

### ML or AI Method Index

No ML/AI model was developed. The study uses regression-based observed-to-expected modeling for epidemiologic and health services analysis.

### Model Inputs and Representations

The analytic unit is hospital referral region for diagnostic-intensity estimation and beneficiary for individual probability models. Inputs are fixed regional or individual tabular variables. The study does not use variable-length EHR sequences or clinical text.

### Baselines or Comparators

Expected new ADRD diagnosis rates adjusted for demographic, socioeconomic, health-risk, and general diagnostic-intensity characteristics.

### Evaluation

The study reports ranges, coefficients of variation, Moran's I for spatial clustering, explained variation from progressive adjustment, and modeled diagnosis probabilities by regional diagnostic intensity.

### Main Findings

Among fee-for-service beneficiaries, 3.0% received a new ADRD diagnosis in 2019. Unadjusted new diagnosis rates across HRRs ranged from 1.7 to 5.4 per 100. ADRD-specific diagnosis intensity ranged from 0.69 to 1.47. Variation was greatest among adults aged 66-74 and among Black and Hispanic groups. Across groups, living in a region with higher ADRD diagnostic intensity was associated with roughly a two-fold difference in the probability of receiving an ADRD diagnosis.

### Author-Stated Limitations

The authors state that results may not generalize to Medicare Advantage enrollees; residual confounding may remain; regional risk measures are coarse; administrative and large survey data have limitations; some clinical factors were unavailable; subgroup analyses were limited by data constraints; and the study was not designed to determine whether regional diagnosis differences affect health outcomes.

### Funding, Conflicts, and Ethics

The study received expedited IRB review from Dartmouth College. The source states no conflicts of interest. Funding details are in the article and supporting information.

### Notes on Missing or Ambiguous Information

The PDF and supplements were not downloaded locally, so this summary is based on the full-text HTML. The study estimates diagnostic intensity relative to expected claims diagnoses, not a direct epidemiologic gold standard for true ADRD incidence.
