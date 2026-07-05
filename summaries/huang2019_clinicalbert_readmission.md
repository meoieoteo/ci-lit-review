---
citation_key: huang2019_clinicalbert_readmission
summary_status: draft
source_status: full_text
paper_type: preprint
ml_ai_methods:
  uses_ml_ai: true
  method_families: [transformer, foundation_model, embedding_model]
  specific_methods: [ClinicalBERT, BERT]
  learning_setup: [self_supervised_learning, supervised_learning]
  input_modalities: [clinical_notes]
  prediction_task: [binary_classification, risk_prediction, representation_learning]
  temporal_handling: [longitudinal_history, visit_sequence]
  interpretability: [attention]
created: 2026-07-05
updated: 2026-07-05
---

# huang2019_clinicalbert_readmission

## Bibliographic Record
Huang, Kexin, Jaan Altosaar, and Rajesh Ranganath. "ClinicalBERT: Modeling Clinical Notes and Predicting Hospital Readmission." 2019. https://arxiv.org/abs/1904.05342.

## Plain-Language Summary
This paper adapts BERT to clinical notes and evaluates whether note representations can predict 30-day hospital readmission. ClinicalBERT processes notes over a hospitalization and updates readmission risk as new notes become available.

## Structured Summary

### Research Question
Can BERT pre-trained on clinical notes represent patient narratives well enough to improve 30-day readmission prediction?

### Study Type
Model development and benchmark study.

### Data Source
Clinical notes from EHR data; the paper uses clinical note corpora for pre-training and readmission prediction.

### Population
Hospitalized patients represented through clinical notes.

### Index Date or Time Origin
Hospital admission and discharge timepoints are used for dynamic and discharge-summary readmission prediction.

### Observation Window
Clinical notes accumulated during an admission, including early-stage notes and discharge summaries.

### Prediction Horizon or Follow-up
Thirty-day hospital readmission.

### Inputs or Predictors
Unstructured clinical notes.

### Outcome or Target
Binary 30-day readmission.

### Methods
The authors pre-train BERT on clinical notes and fine-tune it for readmission prediction. They also evaluate clinical concept similarity and use attention weights as a possible interpretation signal.

### ML or AI Method Index
The core method is transformer-based clinical language-model pre-training plus supervised fine-tuning.

### Model Inputs and Representations
ClinicalBERT creates contextual representations of note text and aggregates note information across the patient timeline.

### Baselines or Comparators
Comparators include other clinical text representation methods such as Word2Vec and FastText, plus readmission-model baselines.

### Evaluation
The paper reports readmission prediction performance using clinically motivated metrics including recall at fixed positive predictive value.

### Main Findings
ClinicalBERT improves 30-day readmission prediction over competing clinical note representation methods and can support earlier risk scoring during admission.

### Author-Stated Limitations
The paper positions ClinicalBERT as a flexible framework, not a finished clinical deployment system.

### Funding, Conflicts, and Ethics
Not extracted in this draft.

### Notes on Missing or Ambiguous Information
This is a hospital readmission paper, not a dementia paper. It is relevant as a clinical-note representation method.
