---
citation_key: li2020_behrt
summary_status: draft
source_status: full_text
paper_type: journal_article
ml_ai_methods:
  uses_ml_ai: true
  method_families: [transformer, foundation_model, embedding_model]
  specific_methods: [BEHRT, BERT]
  learning_setup: [self_supervised_learning, supervised_learning]
  input_modalities: [structured_ehr, diagnosis_codes, medications, procedures, demographics]
  prediction_task: [risk_prediction, multiclass_classification, representation_learning]
  temporal_handling: [visit_sequence, longitudinal_history, irregular_time_intervals]
  interpretability: [attention]
created: 2026-07-05
updated: 2026-07-05
---

# li2020_behrt

## Bibliographic Record
Li, Yikuan, Shishir Rao, Jose Roberto Ayala Solares, Abdelaali Hassaine, Dexter Canoy, Yajie Zhu, Kazem Rahimi, and Gholamreza Salimi-Khorshidi. "BEHRT: Transformer for Electronic Health Records." Scientific Reports 10, no. 1 (2020). https://doi.org/10.1038/s41598-020-62922-y.

## Plain-Language Summary
BEHRT applies a BERT-like transformer architecture to longitudinal EHR event sequences. It predicts future diagnoses across many conditions and learns patient and disease representations from large-scale UK health records.

## Structured Summary

### Research Question
Can a transformer model improve longitudinal EHR disease prediction and representation learning?

### Study Type
Model development and benchmark evaluation.

### Data Source
Clinical Practice Research Datalink linked with hospital and administrative datasets in the UK.

### Population
Nearly 1.6 million individuals in the model evaluation described in the abstract.

### Index Date or Time Origin
Prediction points are based on patient EHR timelines and prior events.

### Observation Window
Longitudinal primary care and linked secondary care histories.

### Prediction Horizon or Follow-up
Future onset of 301 conditions.

### Inputs or Predictors
Structured EHR concepts such as diagnoses, medications, measurements, age, segment, and positional/time information.

### Outcome or Target
Onset prediction for 301 medical conditions.

### Methods
The authors adapt transformer self-attention to EHR sequences and use BERT-style pre-training/fine-tuning ideas for disease trajectory modeling.

### ML or AI Method Index
BEHRT is a transformer model for structured longitudinal EHR data.

### Model Inputs and Representations
Patients are represented as sequences of coded clinical concepts with time and demographic embeddings.

### Baselines or Comparators
Existing deep EHR models.

### Evaluation
Average precision score for future disease prediction.

### Main Findings
BEHRT achieved absolute average-precision improvements of 8.0-10.8 percentage points compared with prior deep EHR models when predicting onset of 301 conditions.

### Author-Stated Limitations
Not extracted in this draft.

### Funding, Conflicts, and Ethics
Not extracted in this draft.

### Notes on Missing or Ambiguous Information
This is structured longitudinal EHR modeling, not clinical-note modeling.
