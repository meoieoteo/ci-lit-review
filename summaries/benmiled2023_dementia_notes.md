---
citation_key: benmiled2023_dementia_notes
summary_status: complete
source_status: full_text
paper_type: journal_article
publication_status: peer_reviewed_version_of_record
ml_ai_methods:
  uses_ml_ai: true
  method_families: [tree_model, gradient_boosting, neural_network, transformer, concept_extraction, embedding_model]
  specific_methods: [TF-ICF, BERT, ClinicalBERT, UMLS, gradient boosted trees]
  learning_setup: [supervised_learning]
  input_modalities: [clinical_notes, diagnosis_codes, demographics]
  input_representation: [bag_of_words_or_terms, concept_features, dense_embeddings, fixed_length_vector]
  prediction_task: [binary_classification, risk_prediction]
  temporal_handling: [lookback_window, prediction_horizon]
  interpretability: [UMLS_concepts, keywords]
created: 2026-07-12
updated: 2026-07-12
---

# benmiled2023_dementia_notes

## Bibliographic Record

Ben Miled et al., "Feature engineering from medical notes: A case study of dementia detection," Heliyon, 2023.

## Publication and Source Status

This summary is based on full-text HTML saved as `papers/benmiled2023_dementia_notes.html`.

## Plain-Language Summary

The paper evaluates whether routine medical notes can be transformed into features that predict dementia one year before diagnosis. It compares keyword, embedding, and UMLS concept representations and tests whether models developed at one institution generalize to held-out and external institutions.

## Structured Summary

### Research Question

Can engineered features from clinical notes predict one-year-ahead dementia, and do those features generalize across institutions?

### Study Type

Retrospective case-control prediction-model study.

### Data Source

Routine medical notes from multiple institutions.

### Population

The development institution included 7,222 patients, split evenly between incident dementia cases and matched controls. Patients with prior dementia or MCI were excluded.

### Index Date or Time Origin

The index date was the disease index date for cases and a matched index date for controls.

### Observation Window

Notes from the three years before the index date were used, excluding the year immediately before index.

### Prediction Horizon or Follow-up

The task was one-year-ahead dementia prediction.

### Inputs or Predictors

Predictors were selected keywords, average BERT or ClinicalBERT embeddings of keyword occurrences, and UMLS concept exposure variables derived from selected keywords.

### Outcome or Target

The target was incident dementia case status versus matched control status.

### Methods

The authors used TF-ICF for keyword selection, neural networks over embedding features, and gradient boosted trees over UMLS concept exposure variables.

### ML or AI Method Index

Transformer embeddings, UMLS concept mapping, neural networks, and gradient boosted trees.

### Model Inputs and Representations

Fixed-length note-derived feature vectors, including embeddings and 209 UMLS exposure variables.

### Baselines or Comparators

The study compares embedding-based and UMLS concept-based representations and evaluates internal and external institution performance.

### Evaluation

Models were developed at one institution, evaluated on held-out patients from that institution, and then evaluated at two other institutions.

### Main Findings

The UMLS concept exposure plus gradient boosted trees approach achieved an AUC of about 75% for one-year-ahead dementia prediction. Performance was not maintained with embedding-space features or across external institutions.

### Author-Stated Limitations

The authors report generalizability limitations and performance drops when models are moved across institutions.

### Funding, Conflicts, and Ethics

Funding, conflicts, and ethics details should be checked in the source before manuscript citation.

### Notes on Missing or Ambiguous Information

The full operational dementia code definition and institutional transport details should be source-checked before using exact claims.
