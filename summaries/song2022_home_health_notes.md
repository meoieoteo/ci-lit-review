---
citation_key: song2022_home_health_notes
summary_status: complete
source_status: full_text
paper_type: journal_article
publication_status: peer_reviewed_version_of_record
ml_ai_methods:
  uses_ml_ai: true
  method_families: [logistic_regression, random_forest, svm, bayesian_network, rule_based_nlp, neural_network]
  specific_methods: [LASSO, Random Forest, SVM, Bayesian network, CNN]
  learning_setup: [supervised_learning]
  input_modalities: [structured_ehr, clinical_notes]
  input_representation: [engineered_features, concept_features, fixed_length_vector]
  prediction_task: [binary_classification, risk_prediction]
  temporal_handling: [episode_window]
  interpretability: [Omaha_System_problems, concerning_notes]
created: 2026-07-12
updated: 2026-07-12
---

# song2022_home_health_notes

## Bibliographic Record

Song et al., "Clinical notes: An untapped opportunity for improving risk prediction for hospitalization and emergency department visit during home health care," Journal of Biomedical Informatics, 2022.

## Publication and Source Status

This summary is based on full-text HTML saved as `papers/song2022_home_health_notes.html`.

## Plain-Language Summary

The study tests whether information extracted from home-health clinical notes improves prediction of hospitalization or emergency department visits. Adding note-derived information to structured assessment and EHR variables improved F-score and precision-recall performance.

## Structured Summary

### Research Question

Do clinical-note features improve risk prediction for hospitalization or ED visits during home health care?

### Study Type

Retrospective prediction-model study.

### Data Source

Structured OASIS/EHR data and approximately 2.3 million home-health clinical notes from a large New York nonprofit home-health organization.

### Population

The study included 86,823 home-health episodes from 2015 to 2017.

### Index Date or Time Origin

Home-health episode.

### Observation Window

Variables were derived from structured assessment/EHR data and notes during the home-health episode.

### Prediction Horizon or Follow-up

The target was hospitalization or ED visit during home-health care.

### Inputs or Predictors

Four feature sets were compared: structured data only; structured plus proportion of concerning notes; structured plus Omaha System problems from notes; and structured plus both note-derived feature families.

### Outcome or Target

Hospitalization or ED visit, extracted from OASIS.

### Methods

The authors used LASSO feature selection and compared logistic regression, Random Forest, Bayesian network, SVM, and Naive Bayes classifiers. Note features came from an ML-based concerning-note classifier and an NLP system for Omaha System risk factors.

### ML or AI Method Index

LASSO, Random Forest, SVM, Bayesian network, Naive Bayes, and note-feature extraction.

### Model Inputs and Representations

Fixed-length episode-level structured and note-derived feature vectors.

### Baselines or Comparators

The structured-only risk model was compared with three structured-plus-notes models.

### Evaluation

The dataset was split 90% training and 10% testing, with SMOTE for class imbalance and tenfold cross-validation.

### Main Findings

8373 of 86,823 episodes had hospitalization or ED visits. SVM had the highest F-score (0.82), Random Forest had the highest PRC area (0.864), and adding clinical-note information improved F-score by up to 16.6% and PRC area by up to 17.8%.

### Author-Stated Limitations

The authors call for validation in other settings and note the need for further investigation of note-derived risk factors.

### Funding, Conflicts, and Ethics

Funding, conflict, and ethics details should be checked in the source before citation.

### Notes on Missing or Ambiguous Information

This is not a dementia study, but it provides an EHR-text risk-prediction analogy.
