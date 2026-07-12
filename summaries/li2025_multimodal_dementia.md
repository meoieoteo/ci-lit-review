---
citation_key: li2025_multimodal_dementia
summary_status: complete
source_status: full_text
paper_type: dissertation
publication_status: dissertation
ml_ai_methods:
  uses_ml_ai: true
  method_families: [transformer, neural_network, random_forest, embedding_model]
  specific_methods: [Longformer, Random Forest, hybrid fusion, decision-focused content selection]
  learning_setup: [supervised_learning]
  input_modalities: [structured_ehr, clinical_notes, demographics, diagnosis_codes]
  input_representation: [dense_embeddings, multimodal_features, document_chunks, fixed_length_vector]
  prediction_task: [binary_classification, risk_prediction]
  temporal_handling: [lookback_window, prediction_horizon]
  interpretability: [content_selection]
created: 2026-07-12
updated: 2026-07-12
---

# li2025_multimodal_dementia

## Bibliographic Record

Li, "Multimodal Fusion for Early Detection of Dementia Using Electronic Health Records," Purdue University dissertation, 2025.

## Publication and Source Status

This summary is based on the full dissertation PDF saved as `papers/li2025_multimodal_dementia.pdf`.

## Plain-Language Summary

The dissertation studies dementia detection from structured EHR data and lengthy clinical notes. It includes decision-focused content selection for long notes and a hybrid fusion architecture combining structured-data predictions with note embeddings.

## Structured Summary

### Research Question

Can multimodal EHR models combining structured data and medical notes improve early dementia detection?

### Study Type

Dissertation containing retrospective EHR modeling studies.

### Data Source

Indiana Network for Patient Care data.

### Population

Matched case-control cohorts for dementia detection were constructed from EHR data.

### Index Date or Time Origin

The dissertation uses dementia case/control index dates tied to observation and prediction windows.

### Observation Window

Reported experiments use observation periods from one to three years.

### Prediction Horizon or Follow-up

Reported horizons include approximately 0.5 to 1 year before the index.

### Inputs or Predictors

Structured demographics and diagnoses plus unstructured medical notes.

### Outcome or Target

Dementia case/control status.

### Methods

The dissertation includes decision-focused note content selection, Longformer-based note modeling, Random Forest structured-data modeling, and hybrid fusion of structured probability embeddings with note embeddings.

### ML or AI Method Index

Longformer, Random Forest, neural fusion, and decision-focused content selection.

### Model Inputs and Representations

Structured features are converted to model scores or embeddings and concatenated with Longformer note representations.

### Baselines or Comparators

Unimodal structured, unimodal notes, and baseline fusion models are compared with the hybrid fusion model.

### Evaluation

The dissertation reports nested cross-validation across observation-window and prediction-horizon settings.

### Main Findings

The dissertation reports that multimodal fusion improves over structured-only and note-only baselines, with strongest results in longer observation and shorter horizon settings.

### Author-Stated Limitations

Limitations include retrospective design, dependence on one health-information exchange context, and the need for broader validation.

### Funding, Conflicts, and Ethics

Dissertation administrative and ethics details should be checked in the PDF before citation.

### Notes on Missing or Ambiguous Information

Exact table values should be source-checked before manuscript use because this is a long dissertation with multiple experiments.
