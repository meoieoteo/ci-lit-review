---
citation_key: garriga2023_mental_health_crises_notes
summary_status: complete
source_status: full_text
paper_type: journal_article
publication_status: peer_reviewed_version_of_record
ml_ai_methods:
  uses_ml_ai: true
  method_families: [gradient_boosting, neural_network, transformer, embedding_model]
  specific_methods: [BERT, XGBoost, SHAP]
  learning_setup: [supervised_learning]
  input_modalities: [structured_ehr, clinical_notes, diagnosis_codes, medications, demographics]
  input_representation: [engineered_features, dense_embeddings, multimodal_features, fixed_length_vector]
  prediction_task: [binary_classification, risk_prediction]
  temporal_handling: [rolling_prediction_window]
  interpretability: [SHAP]
created: 2026-07-12
updated: 2026-07-12
---

# garriga2023_mental_health_crises_notes

## Bibliographic Record

Garriga et al., "Combining clinical notes with structured electronic health records enhances prediction of mental health crises," Cell Reports Medicine, 2023.

## Publication and Source Status

This summary is based on full-text HTML saved as `papers/garriga2023_mental_health_crises_notes.html`.

## Plain-Language Summary

The study predicts mental health crisis relapse using structured EHR data and clinical notes. Adding BERT-derived note representations to structured data improved short-horizon prediction compared with structured-only baselines.

## Structured Summary

### Research Question

Can clinical notes improve prediction of mental health crisis relapse beyond structured EHR data?

### Study Type

Retrospective multimodal EHR prediction study.

### Data Source

Eight years of de-identified EHR data for mental health patients.

### Population

The cohort included 59,750 patients and 2,709,626 crisis events or weekly prediction records as reported by the paper.

### Index Date or Time Origin

The prediction unit was a weekly time point.

### Observation Window

Structured and note data before each weekly prediction point were used.

### Prediction Horizon or Follow-up

The target was mental health crisis relapse in the next 28 days.

### Inputs or Predictors

Structured EHR features and 768-dimensional BERT semantic features from clinical notes.

### Outcome or Target

Mental health crisis event or relapse within 28 days.

### Methods

The study compared structured XGBoost/deep neural networks, unstructured-note neural networks, hybrid deep neural networks, and an ensemble approach.

### ML or AI Method Index

BERT embeddings, XGBoost, deep neural networks, ensemble modeling, and SHAP interpretation.

### Model Inputs and Representations

Fixed-length structured features and BERT note embeddings.

### Baselines or Comparators

Baselines included logistic regression using recent crisis history and structured-only models.

### Evaluation

The authors evaluated AUROC and AUPRC for weekly predictions in a low-prevalence outcome setting.

### Main Findings

The ensemble DNN achieved mean AUPRC 0.133 and AUROC 0.865, outperforming reported structured and simple history baselines.

### Author-Stated Limitations

Limitations include domain specificity to mental health crisis prediction and dependence on available notes.

### Funding, Conflicts, and Ethics

Funding, conflict, and ethics details should be checked in the source before citation.

### Notes on Missing or Ambiguous Information

The study is an analogy for multimodal prediction and does not address dementia labels or cardiology workflows.
