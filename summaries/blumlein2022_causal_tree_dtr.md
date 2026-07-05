---
citation_key: blumlein2022_causal_tree_dtr
summary_status: draft
source_status: full_text
paper_type: preprint
ml_ai_methods:
  uses_ml_ai: true
  method_families: [causal_model, tree_model, random_forest]
  specific_methods: [DTR-CT, DTR-CF, causal trees, causal forests]
  learning_setup: [supervised_learning, statistical_association]
  input_modalities: [structured_ehr]
  prediction_task: [policy_learning]
  temporal_handling: [longitudinal_history, visit_sequence]
  interpretability: [rules, feature_importance]
created: 2026-07-05
updated: 2026-07-05
---

# blumlein2022_causal_tree_dtr

## Bibliographic Record
Blumlein, Theresa, Joel Persson, and Stefan Feuerriegel. "Learning Optimal Dynamic Treatment Regimes Using Causal Tree Methods in Medicine." 2022. https://arxiv.org/abs/2204.07124.

## Plain-Language Summary
This paper proposes dynamic treatment regime methods based on causal trees and causal forests. The goal is to learn sequential treatment recommendations that are both flexible enough for EHR data and more explainable than black-box reinforcement-learning approaches.

## Structured Summary

### Research Question
Can causal tree and causal forest methods be adapted to learn optimal dynamic treatment regimes from complex medical data?

### Study Type
Method development with synthetic experiments and real-world ICU application.

### Data Source
Synthetic data and real-world intensive care unit data.

### Population
ICU patients in the applied evaluation; details are not extracted in this draft.

### Index Date or Time Origin
Sequential treatment decision stages.

### Observation Window
Longitudinal patient histories across treatment stages.

### Prediction Horizon or Follow-up
The task is policy learning over sequential decisions, not conventional prediction.

### Inputs or Predictors
Patient covariates, treatment histories, and outcomes.

### Outcome or Target
Optimal sequential treatment decisions and expected outcomes under learned dynamic treatment regimes.

### Methods
The authors introduce DTR-CT and DTR-CF by adapting causal trees and causal forests to sequential treatment-effect estimation. The methods aim to account for time-varying confounding and provide explainable decisions.

### ML or AI Method Index
The core methods are causal tree/forest estimators used for dynamic treatment-regime policy learning.

### Model Inputs and Representations
Structured patient covariates and treatment history are used to estimate heterogeneous treatment effects.

### Baselines or Comparators
State-of-the-art DTR baselines including Q-learning-style and other policy-learning methods.

### Evaluation
Synthetic data evaluation uses cumulative regret and percentage of optimal decisions; real-world ICU analysis compares expected outcomes under learned regimes.

### Main Findings
The proposed DTR-CT and DTR-CF methods reduce cumulative regret by more than 20% compared with the best baseline in synthetic experiments and recommend ICU treatment decisions with better expected outcomes than observed treatment regimes.

### Author-Stated Limitations
Not extracted in this draft.

### Funding, Conflicts, and Ethics
Not extracted in this draft.

### Notes on Missing or Ambiguous Information
This is about treatment policy, not pre-encounter risk scoring.
