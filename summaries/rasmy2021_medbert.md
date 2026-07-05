---
citation_key: rasmy2021_medbert
summary_status: draft
source_status: full_text
paper_type: journal_article
ml_ai_methods:
  uses_ml_ai: true
  method_families: [transformer, foundation_model, embedding_model]
  specific_methods: [Med-BERT, BERT, GRU, Bi-GRU, RETAIN]
  learning_setup: [self_supervised_learning, supervised_learning]
  input_modalities: [structured_ehr, diagnosis_codes]
  prediction_task: [risk_prediction, binary_classification, representation_learning]
  temporal_handling: [visit_sequence, longitudinal_history]
  interpretability: [attention]
created: 2026-07-05
updated: 2026-07-05
---

# rasmy2021_medbert

## Bibliographic Record
Rasmy, Laila, Yang Xiang, Ziqian Xie, Cui Tao, and Degui Zhi. "Med-BERT: pretrained contextualized embeddings on large-scale structured electronic health records for disease prediction." npj Digital Medicine 4, no. 1 (2021). https://doi.org/10.1038/s41746-021-00455-y.

## Plain-Language Summary
Med-BERT adapts BERT-style pre-training to structured EHR diagnosis-code sequences. It improves disease prediction, especially when downstream labeled training data are limited.

## Structured Summary

### Research Question
Can pre-trained contextual embeddings from large structured EHR data improve downstream disease prediction?

### Study Type
Model development and benchmark evaluation.

### Data Source
Large structured EHR datasets used for pre-training and downstream disease-prediction cohorts from two EHR databases.

### Population
Pre-training used 28,490,650 patient EHR records. Fine-tuning used three cohorts across two disease-prediction tasks.

### Index Date or Time Origin
Varied by downstream disease-prediction task.

### Observation Window
Longitudinal EHR diagnosis histories before prediction.

### Prediction Horizon or Follow-up
Varied by task; evaluated tasks included heart failure in patients with diabetes and pancreatic cancer prediction.

### Inputs or Predictors
Structured diagnosis-code sequences from EHR.

### Outcome or Target
Disease-prediction outcomes for heart failure and pancreatic cancer.

### Methods
The authors adapt BERT for structured EHR visits, modify layer representations for EHR structure, and add a domain-specific pre-training task before fine-tuning.

### ML or AI Method Index
The core method is transformer pre-training on structured EHR code sequences followed by supervised fine-tuning.

### Model Inputs and Representations
Diagnosis codes are represented as contextualized embeddings over patient visit sequences.

### Baselines or Comparators
GRU, Bi-GRU, and RETAIN predictive models.

### Evaluation
AUC improvement across three fine-tuning cohorts and experiments with small training sample sizes.

### Main Findings
Med-BERT improved AUC by 2.67-3.92%, 3.20-7.12%, and 2.02-4.71% across cohorts compared with GRU, Bi-GRU, and RETAIN. It was especially helpful with 300-500 fine-tuning samples.

### Author-Stated Limitations
Not extracted in this draft.

### Funding, Conflicts, and Ethics
Not extracted in this draft.

### Notes on Missing or Ambiguous Information
Med-BERT models structured EHR codes, not note text.
