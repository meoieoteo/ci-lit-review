---
citation_key: shen2025_integrating_misclassified_ehr_outcomes
summary_status: draft
source_status: full_text
paper_type: preprint
publication_status: preprint
ml_ai_methods:
  uses_ml_ai: false
  method_families: ["causal_model", "other"]
  specific_methods: ["inverse probability weighting", "measurement error correction", "selection propensity model"]
  learning_setup: ["statistical_association"]
  input_modalities: ["structured_ehr", "demographics", "cognitive_tests", "other"]
  input_representation: ["engineered_features", "fixed_length_vector"]
  prediction_task: ["not_applicable"]
  temporal_handling: ["longitudinal_history"]
  interpretability: ["coefficients"]
created: 2026-07-12
updated: 2026-07-12
---

# shen2025_integrating_misclassified_ehr_outcomes

## Bibliographic Record

Shen, Jenny, Dane Isenberg, Kristin A. Linn, and Rebecca A. Hubbard. "Integrating Misclassified EHR Outcomes with Validated Outcomes from a Non-probability Sample." arXiv:2503.02071, 2025. https://arxiv.org/abs/2503.02071.

## Publication and Source Status

Preprint on arXiv, version 1 dated March 3, 2025. The local source is the arXiv PDF.

## Plain-Language Summary

This methods preprint addresses a common EHR research problem: a large EHR cohort may have outcome labels measured with error, while a smaller linked validation sample may have higher-quality outcomes but be selected non-randomly. The authors propose estimators for average treatment effects that correct both EHR outcome misclassification and selection bias in the validation sample. They illustrate the method using Adult Changes in Thought data, clinical Alzheimer disease outcomes, and autopsy-derived neuropathology.

## Structured Summary

### Research Question

How can investigators estimate average treatment effects when a large EHR-derived cohort has misclassified binary outcomes and a smaller validation sample contains gold-standard outcomes but is subject to selection bias?

### Study Type

Statistical methods preprint with simulations and an applied ACT study analysis.

### Data Source

Simulation studies and Adult Changes in Thought (ACT) study data, including linked clinical and autopsy information from Kaiser Permanente Washington members.

### Population

In the applied analysis, ACT participants were sampled from Kaiser Permanente Washington members aged at least 65, dementia-free, not living in nursing homes, and enrolled for at least two years. The analysis included 5,669 individuals from the full ACT cohort, including 837 in the autopsy subsample.

### Index Date or Time Origin

Not framed as a clinical prediction index. ACT includes baseline and biennial follow-up assessments; autopsy data are available for deceased participants who consented.

### Observation Window

Longitudinal ACT study follow-up; specific calendar years are not central in the extracted text.

### Prediction Horizon or Follow-up

Not a prediction study. The estimand is the average treatment effect of hypertension on AD neuropathology in the applied analysis.

### Inputs or Predictors

Treatment/exposure was hypertension, defined by maximum observed systolic blood pressure at least 140 mmHg across longitudinal clinical visits. Covariates included antihypertensive medication use, BMI, age, race, gender, clinical dementia status, ACT cohort, and hypertension for selection modeling.

### Outcome or Target

Silver-standard clinical AD diagnosis for the full ACT cohort and gold-standard AD neuropathology among autopsied participants. Neuropathology was defined using Braak stage and CERAD neuritic plaque ratings.

### Methods

The authors propose inverse-probability-weighted estimators that combine error-prone EHR outcomes with gold-standard validation outcomes while modeling selection into the non-probability validation sample. They compare estimators through simulations and ACT data analysis.

### ML or AI Method Index

No ML/AI prediction model is developed. The paper is a causal/statistical methods paper focused on measurement error, validation data, and sample selection.

### Model Inputs and Representations

The analytic unit is individual participant. Inputs are fixed tabular covariates, exposure, silver-standard outcome, and validation-sample gold-standard outcome.

### Baselines or Comparators

Comparators include naive estimators using silver-standard outcomes, validation-only estimators, estimators correcting misclassification without selection adjustment, and proposed estimators correcting both outcome misclassification and selection bias.

### Evaluation

Simulations assessed bias and efficiency under varied validation sampling mechanisms. The ACT application compared point estimates and confidence intervals for hypertension's effect on AD neuropathology.

### Main Findings

In simulations, estimators that failed to account for selection were biased when validation samples were non-probability samples. Proposed estimators reduced bias and improved efficiency. In ACT, the naive estimator using error-prone clinical outcomes was attenuated toward the null; estimators correcting outcome misclassification produced positive ATE estimates, and selection correction made less difference in this application.

### Author-Stated Limitations

The authors state that their estimators depend on correct treatment propensity and validation selection models; the selection model requires measured factors explaining validation inclusion; model misspecification can bias results; they focus on IPW estimation, binary outcomes, and ATE; predictor measurement error, CATE, continuous outcomes, multiply robust estimators, and missing covariate mechanisms remain future work.

### Funding, Conflicts, and Ethics

Funding, conflicts, and ethics statements were not identified in the extracted preprint text.

### Notes on Missing or Ambiguous Information

This is a preprint and should be checked for later peer-reviewed versions before manuscript use. The paper is methods-focused and is not specifically about pre-cardiology risk scoring or diagnosis opportunity, although the applied example concerns Alzheimer disease measurement.
