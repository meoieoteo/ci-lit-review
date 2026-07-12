---
citation_key: lyu2022_multimodal_mortality_notes
summary_status: complete
source_status: full_text
paper_type: conference_paper
publication_status: peer_reviewed_conference_or_preprint
ml_ai_methods:
  uses_ml_ai: true
  method_families: [transformer, embedding_model, neural_network]
  specific_methods: [ClinicalBERT, multimodal transformer, integrated gradients, Shapley values]
  learning_setup: [supervised_learning]
  input_modalities: [structured_ehr, clinical_notes, labs, vitals]
  input_representation: [time_aware_sequence, dense_embeddings, multimodal_features]
  prediction_task: [binary_classification, risk_prediction]
  temporal_handling: [first_48_hours, time_aware_sequence]
  interpretability: [integrated_gradients, Shapley_values]
created: 2026-07-12
updated: 2026-07-12
---

# lyu2022_multimodal_mortality_notes

## Bibliographic Record

Lyu et al., "A Multimodal Transformer: Fusing Clinical Notes with Structured EHR Data for Interpretable In-Hospital Mortality Prediction," AMIA Annual Symposium/arXiv, 2022.

## Publication and Source Status

This summary is based on the full text saved as `papers/lyu2022_multimodal_mortality_notes.pdf`.

## Plain-Language Summary

The paper proposes a multimodal transformer that combines structured ICU time-series data with clinical-note embeddings for in-hospital mortality prediction. It also presents interpretability outputs for text and structured variables.

## Structured Summary

### Research Question

Can a multimodal transformer fuse structured EHR data and clinical notes to improve interpretable in-hospital mortality prediction?

### Study Type

Retrospective ICU prediction-model study.

### Data Source

MIMIC-III ICU data, including structured variables and NOTEEVENTS clinical notes.

### Population

The analytic sample included ICU visits with notes available; reported splits were 14,068 training, 3,086 validation, and 3,107 test samples.

### Index Date or Time Origin

ICU admission.

### Observation Window

The first 48 hours of ICU stay.

### Prediction Horizon or Follow-up

In-hospital mortality during the admission.

### Inputs or Predictors

Structured clinical variables and clinical notes from the first 48 hours.

### Outcome or Target

In-hospital mortality.

### Methods

The model embeds structured time-series data and note representations, then fuses them with a multimodal transformer.

### ML or AI Method Index

ClinicalBERT, multimodal transformer, integrated gradients, and Shapley values.

### Model Inputs and Representations

Time-indexed structured variables and hourly note embeddings.

### Baselines or Comparators

The paper compares against structured-only, note-only, and other multimodal baselines.

### Evaluation

Performance is reported on a held-out MIMIC-III test set.

### Main Findings

The multimodal transformer reports AUCPR 0.538, AUROC 0.877, and F1 0.490.

### Author-Stated Limitations

Limitations include ICU-specific data, dependence on note availability, and retrospective evaluation.

### Funding, Conflicts, and Ethics

Funding, conflict, and ethics details should be checked in the source before citation.

### Notes on Missing or Ambiguous Information

The paper is a method analogy for multimodal fusion, not dementia prediction.
