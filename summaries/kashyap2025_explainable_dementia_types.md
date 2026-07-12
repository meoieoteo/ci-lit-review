---
citation_key: kashyap2025_explainable_dementia_types
summary_status: complete
source_status: full_text
paper_type: journal_article
publication_status: peer_reviewed_version_of_record
ml_ai_methods:
  uses_ml_ai: true
  method_families: [llm, transformer, logistic_regression, concept_extraction]
  specific_methods: [GPT-4, text embeddings, linear classifier]
  learning_setup: [supervised_learning]
  input_modalities: [clinical_notes]
  input_representation: [concept_features, dense_embeddings, fixed_length_vector]
  prediction_task: [multiclass_classification, phenotyping]
  temporal_handling: [not_reported]
  interpretability: [LLM_aided_concepts]
created: 2026-07-12
updated: 2026-07-12
---

# kashyap2025_explainable_dementia_types

## Bibliographic Record

Kashyap et al., "Predicting explainable dementia types with LLM-aided feature engineering," Bioinformatics, 2025.

## Publication and Source Status

This summary is based on full-text HTML saved as `papers/kashyap2025_explainable_dementia_types.html`.

## Plain-Language Summary

The paper uses GPT-4 and a medical textbook to build interpretable clinical concept features for classifying dementia types from clinical notes. The concept-based model outperformed n-gram logistic regression and a direct GPT-4 baseline.

## Structured Summary

### Research Question

Can LLM-aided feature engineering produce interpretable features for dementia-type classification from clinical notes?

### Study Type

Retrospective NLP/modeling study.

### Data Source

Clinical notes from a single hospital system, plus the Oxford Textbook of Medicine for feature engineering.

### Population

Patients with dementia-type labels in the study data; exact population details should be source-checked before citation.

### Index Date or Time Origin

The paper is framed as note-based dementia-type classification rather than a pre-index risk model.

### Observation Window

Temporal windows are not central to the reported task.

### Prediction Horizon or Follow-up

No future prediction horizon is reported for the main dementia-type classification task.

### Inputs or Predictors

Clinical notes converted into concept-vector representations.

### Outcome or Target

Dementia type classification.

### Methods

The authors used GPT-4 to extract 254 clinically interpretable concepts, estimated concept agreement/presence in notes, and trained a linear classifier.

### ML or AI Method Index

LLM-aided concept engineering, text embeddings, and linear classification.

### Model Inputs and Representations

Concept features indicating whether a patient exhibits clinical concepts, plus embedding-based methods for efficient concept matching.

### Baselines or Comparators

The paper compares the concept model with n-gram logistic regression and direct GPT-4 classification.

### Evaluation

The paper reports classification accuracy and compares baseline approaches.

### Main Findings

The concept-based model reports accuracy 0.72, compared with 0.64 for n-gram logistic regression and 0.48 for a GPT-4 baseline. Text embeddings reduced time and cost relative to direct LLM use.

### Author-Stated Limitations

Limitations include missed clinical details by GPT-4, omission of demographic/lifestyle features, limited temporal modeling, a constrained concept set, and single-hospital data.

### Funding, Conflicts, and Ethics

Funding, conflict, and ethics details should be checked in the source before citation.

### Notes on Missing or Ambiguous Information

The study is about dementia-type classification, not early dementia risk before a cardiology encounter.
