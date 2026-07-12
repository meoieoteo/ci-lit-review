---
citation_key: spoto2025_diagnostic_signal_decay_dementia
summary_status: draft
source_status: full_text
paper_type: preprint
publication_status: preprint
ml_ai_methods:
  uses_ml_ai: true
  method_families: ["other"]
  specific_methods: ["transitive Sequential Pattern Mining", "random skewers matrix similarity", "multivariable linear regression"]
  learning_setup: ["statistical_association"]
  input_modalities: ["claims", "diagnosis_codes", "demographics", "other"]
  input_representation: ["event_sequence", "engineered_features"]
  prediction_task: ["not_applicable"]
  temporal_handling: ["longitudinal_history", "time_aware_sequence"]
  interpretability: ["coefficients"]
created: 2026-07-12
updated: 2026-07-12
---

# spoto2025_diagnostic_signal_decay_dementia

## Bibliographic Record

Spoto, Federica, Jiazi Tian, Jonas Huegel, Daniel T. Ortega, Christine S. Ritchie, Deborah Blacker, Francesca Dominici, Chirag J. Patel, Daniel Mork, and Hossein Estiri. "Quantifying Diagnostic Signal Decay in Dementia: A National Study of Medicare Hospitalization Data." arXiv:2506.14669, 2025. https://arxiv.org/abs/2506.14669.

## Publication and Source Status

Preprint on arXiv, version 1 dated June 17, 2025. The local source is the arXiv PDF.

## Plain-Language Summary

This preprint studies how dementia diagnosis codes vary across Medicare hospitalization data and argues that code patterns can lose clinical specificity as they pass through different health care and documentation systems. The authors call this "diagnostic signal decay." They find that non-specific dementia codes dominate nationally, that specific codes often transition to non-specific codes over time, and that coding-pattern divergence is associated with county-level rurality, Medicaid eligibility, and racial/ethnic composition.

## Structured Summary

### Research Question

How do dementia-related ICD-10 coding patterns vary geographically and demographically in Medicare hospitalization data, and what structural factors are associated with divergence from national coding patterns?

### Study Type

Preprint observational study of Medicare inpatient claims and diagnostic-code sequence patterns.

### Data Source

Medicare Part A MedPAR inpatient hospitalization claims for fee-for-service beneficiaries aged 65 or older from 2016-2018, plus county-level ACS/NHGIS and Census data.

### Population

1,827,468 Medicare fee-for-service beneficiaries aged 65 or older with at least one hospitalization containing a dementia-related ICD-10 diagnosis code between 2016 and 2018, totaling 3,045,819 hospitalizations.

### Index Date or Time Origin

Hospitalization sequence during 2016-2018.

### Observation Window

January 1, 2016 through December 31, 2018.

### Prediction Horizon or Follow-up

Not a prediction-horizon study. The paper analyzes diagnostic-code frequency and temporal transition structure.

### Inputs or Predictors

Dementia-related ICD-10 codes grouped into five categories; patient demographics; county-level education, unemployment, rurality, Medicaid eligibility, disability, racial/ethnic composition, and dementia prevalence.

### Outcome or Target

Diagnostic signal fidelity, operationalized as code frequency, temporal code-transition structure, and similarity between local and national diagnostic code patterns.

### Methods

The authors grouped 17 ICD-10 dementia codes into five diagnostic categories, used transitive Sequential Pattern Mining to characterize temporal associations among codes, compared local and national temporal-correlation matrices using random skewers matrix similarity, and fit multivariable linear regressions with state fixed effects to identify county-level correlates of lower similarity.

### ML or AI Method Index

The study uses sequence-mining and matrix-similarity methods, but it does not develop a clinical prediction model. It is indexed as computational/statistical analysis of claims code patterns.

### Model Inputs and Representations

The input unit is a beneficiary's sequence of hospitalization diagnosis codes. Code usage is represented as temporal associations and local/national similarity matrices, with county-level covariates used in regression.

### Baselines or Comparators

Local county or state code-use patterns were compared with national code-use patterns.

### Evaluation

The paper reports code frequencies, random-skewers similarity scores, regression coefficients, explained variance, and sensitivity analyses using alternative similarity metrics and individual ICD-10 codes.

### Main Findings

Non-specific dementia codes were dominant nationally and appeared in more than 75% of dementia hospitalizations. Alzheimer's disease and vascular dementia code use varied across states. Temporal analysis showed transitions from specific to non-specific codes. Lower county similarity to national patterns was associated with greater rural population share, Medicaid eligibility among dementia patients, and higher proportions of Black and Hispanic dementia patients. The regression model explained 38% of variation in local-to-national diagnostic alignment.

### Author-Stated Limitations

The authors state that the study is limited to Medicare Part A inpatient claims, excluding outpatient, long-term care, and community settings; hospitalized dementia patients are not representative of all dementia patients; hospital codes are often assigned by professional coders; county-level covariates may create ecological fallacy; tSPM+ cannot distinguish clinically warranted from administratively motivated transitions; and substantial variation remains unexplained.

### Funding, Conflicts, and Ethics

Funding, conflicts, and ethics statements were not identified in the extracted preprint text.

### Notes on Missing or Ambiguous Information

This is a preprint and should be checked for later peer-reviewed versions before manuscript use. Supplementary materials were referenced but not separately downloaded.
