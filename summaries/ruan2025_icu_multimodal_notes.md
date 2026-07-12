---
citation_key: ruan2025_icu_multimodal_notes
summary_status: complete
source_status: full_text
paper_type: preprint
publication_status: preprint
ml_ai_methods:
  uses_ml_ai: true
  method_families: [transformer, neural_network, embedding_model, other]
  specific_methods: [BERT, BioBERT, ClinicalBERT, evidential neural network, Dempster-Shafer fusion]
  learning_setup: [supervised_learning]
  input_modalities: [structured_ehr, clinical_notes, labs, vitals, medications, demographics]
  input_representation: [dense_embeddings, engineered_features, multimodal_features, fixed_length_vector]
  prediction_task: [binary_classification, risk_prediction]
  temporal_handling: [first_24_hours]
  interpretability: [evidence_uncertainty]
created: 2026-07-12
updated: 2026-07-12
---

# ruan2025_icu_multimodal_notes

## Bibliographic Record

Ruan et al., "Towards accurate and reliable ICU outcome prediction: a multimodal learning framework based on belief function theory using structured EHRs and free-text notes," arXiv, 2025.

## Publication and Source Status

This summary is based on the full text saved as `papers/ruan2025_icu_multimodal_notes.pdf`.

## Plain-Language Summary

The preprint proposes a multimodal ICU outcome-prediction framework that combines structured EHR features and clinical notes using belief-function evidence fusion. It evaluates both accuracy and reliability metrics for mortality and prolonged length of stay.

## Structured Summary

### Research Question

Can belief-function multimodal fusion improve ICU outcome prediction and reliability when combining structured EHR data with clinical notes?

### Study Type

Retrospective ICU prediction-model preprint.

### Data Source

MIMIC-III ICU data.

### Population

ICU stays with structured data and selected note types available.

### Index Date or Time Origin

ICU admission.

### Observation Window

The first 24 hours of the ICU stay.

### Prediction Horizon or Follow-up

The outcomes are in-hospital mortality and prolonged length of stay.

### Inputs or Predictors

Structured demographics, vitals, labs, treatments, comorbidities, and notes from Nursing, Nursing/Other, Physician, and Radiology note types.

### Outcome or Target

Mortality and prolonged length of stay.

### Methods

The framework uses structured encoders, BERT-family text encoders, evidential neural networks, and Dempster-Shafer evidence fusion.

### ML or AI Method Index

MLP/ResNet/Transformer structured encoders, BERT/BioBERT/ClinicalBERT text encoders, evidential neural networks, and belief-function fusion.

### Model Inputs and Representations

Fixed-length structured features and 512-token note representations fused at the evidence level.

### Baselines or Comparators

The paper compares multiple structured/text encoder combinations and baseline multimodal models.

### Evaluation

The study uses 60/20/20 train/validation/test splits and five random seeds, reporting discrimination and reliability metrics.

### Main Findings

The abstract reports improvements over the best baseline for balanced accuracy, F1, AUROC, AUPRC, Brier score, and negative log likelihood. Detailed results include mortality AUROC around 0.853 and PLOS AUROC around 0.774 for best settings.

### Author-Stated Limitations

Limitations include retrospective MIMIC-III evaluation, preprint status, and need for external validation.

### Funding, Conflicts, and Ethics

Funding, conflict, and ethics details should be checked in the source before citation.

### Notes on Missing or Ambiguous Information

The paper is methodologically relevant for multimodal fusion and reliability metrics but not dementia- or cardiology-specific.
