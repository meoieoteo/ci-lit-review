---
citation_key: choi2016_retain
summary_status: draft
source_status: full_text
paper_type: conference_paper
ml_ai_methods:
  uses_ml_ai: true
  method_families: [rnn, neural_network]
  specific_methods: [RETAIN, reverse-time attention, GRU]
  learning_setup: [supervised_learning]
  input_modalities: [structured_ehr, diagnosis_codes, medications, procedures]
  input_representation: [visit_sequence, sequence_tokens, time_aware_sequence]
  prediction_task: [binary_classification, risk_prediction]
  temporal_handling: [visit_sequence, longitudinal_history]
  interpretability: [attention]
created: 2026-07-05
updated: 2026-07-11
---

# choi2016_retain

## Bibliographic Record
Choi, Edward, Mohammad Taha Bahadori, Joshua A. Kulas, Andy Schuetz, Walter F. Stewart, and Jimeng Sun. "RETAIN: An Interpretable Predictive Model for Healthcare Using Reverse Time Attention Mechanism." Advances in Neural Information Processing Systems 29, 2016.

## Plain-Language Summary
RETAIN is a neural model for longitudinal EHR prediction that tries to preserve interpretability. It reads patient visits in reverse chronological order and uses attention to identify influential visits and clinical variables for a prediction.

## Structured Summary

### Research Question
Can an EHR sequence model achieve neural-network-level predictive performance while producing clinically interpretable visit- and variable-level explanations?

### Study Type
Model development and benchmark evaluation.

### Data Source
Large health-system EHR dataset from Sutter Health.

### Population
263,000 patients with 14 million visits over eight years.

### Index Date or Time Origin
Prediction is based on longitudinal visit sequences before a target prediction point.

### Observation Window
Historical EHR visits before prediction.

### Prediction Horizon or Follow-up
The paper evaluates future clinical prediction tasks, including future heart failure diagnosis.

### Inputs or Predictors
Sequential EHR visit codes such as diagnoses, medications, and procedures.

### Outcome or Target
Future diagnosis prediction, including heart failure in the main case-control example.

### Methods
RETAIN uses a two-level attention architecture over visits and variables, processed in reverse time. The model is trained end to end for supervised prediction.

### ML or AI Method Index
The core method is a recurrent neural network with reverse-time attention designed for interpretability.

### Model Inputs and Representations
Each patient is represented as a variable-length sequence of visits containing high-dimensional clinical variables. RETAIN does not collapse the entire EHR history into a single fixed-length tabular vector before modeling; it consumes ordered visit sequences and uses reverse-time recurrent processing with visit-level and variable-level attention.

### Baselines or Comparators
Comparators include traditional models and RNN variants.

### Evaluation
The paper compares predictive accuracy, scalability, and interpretability against baselines.

### Main Findings
RETAIN achieved accuracy and scalability comparable to RNN methods while providing attention-based explanations closer to traditional interpretable models.

### Author-Stated Limitations
Not extracted in detail in this draft.

### Funding, Conflicts, and Ethics
Not extracted in this draft.

### Notes on Missing or Ambiguous Information
The paper uses structured EHR sequences, not clinical notes.
