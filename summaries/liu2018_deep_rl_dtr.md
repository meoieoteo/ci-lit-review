---
citation_key: liu2018_deep_rl_dtr
summary_status: draft
source_status: full_text
paper_type: preprint
ml_ai_methods:
  uses_ml_ai: true
  method_families: [reinforcement_learning, neural_network]
  specific_methods: [deep reinforcement learning, dynamic treatment regimes, deep neural network]
  learning_setup: [reinforcement_learning, supervised_learning]
  input_modalities: [structured_ehr, registry]
  prediction_task: [policy_learning]
  temporal_handling: [longitudinal_history, visit_sequence]
  interpretability: [none_reported]
created: 2026-07-05
updated: 2026-07-05
---

# liu2018_deep_rl_dtr

## Bibliographic Record
Liu, Ning, Ying Liu, Brent Logan, Zhiyuan Xu, Jian Tang, and Yanzhi Wang. "Deep Reinforcement Learning for Dynamic Treatment Regimes on Medical Registry Data." 2018. https://arxiv.org/abs/1801.09271.

## Plain-Language Summary
This paper proposes a deep reinforcement-learning framework for learning dynamic treatment regimes from observational medical registry data. The application is graft-versus-host disease prevention and treatment after hematopoietic cell transplantation.

## Structured Summary

### Research Question
Can deep reinforcement learning estimate dynamic treatment regimes from observational registry data with heterogeneous decision stages and high-dimensional actions?

### Study Type
Method development with medical registry application.

### Data Source
Center for International Blood and Marrow Transplant Research registry.

### Population
6,021 leukemia patients who underwent allogeneic hematopoietic cell transplantation.

### Index Date or Time Origin
Transplant and subsequent treatment decision stages.

### Observation Window
Treatment decisions from initial conditioning and prophylaxis through acute and chronic GVHD treatment stages up to four years.

### Prediction Horizon or Follow-up
Four-year treatment-regime horizon after transplantation.

### Inputs or Predictors
Patient clinical states, treatment histories, and high-dimensional treatment options.

### Outcome or Target
Dynamic treatment policies with high expected reward, including survival and relapse-related reward structure.

### Methods
The framework uses supervised learning to predict likely expert actions and deep reinforcement learning to estimate long-term value functions over candidate actions.

### ML or AI Method Index
The paper combines deep neural networks for expert-action prediction with DRL for policy/value estimation.

### Model Inputs and Representations
Registry-derived clinical variables are encoded as states; treatments are actions.

### Baselines or Comparators
Expert treatment decisions and DRL-recommended regimes.

### Evaluation
Top-N expert-action prediction accuracy and expected reward under learned dynamic treatment regimes.

### Main Findings
Top-N expert treatment prediction accuracy was generally between 75% and 90% for initial treatments, and DRL-based regimes showed high expected reward in experiments.

### Author-Stated Limitations
The paper notes limitations from available data size and uses separate models for different treatment stages.

### Funding, Conflicts, and Ethics
Not extracted in this draft.

### Notes on Missing or Ambiguous Information
This is treatment-policy work rather than risk-score development.
