---
citation_key: janisch2020_costly_features
summary_status: draft
source_status: full_text
paper_type: journal_article
ml_ai_methods:
  uses_ml_ai: true
  method_families: [reinforcement_learning, neural_network]
  specific_methods: [classification with costly features, MDP, deep reinforcement learning]
  learning_setup: [reinforcement_learning, simulation]
  input_modalities: [other]
  prediction_task: [feature_acquisition, binary_classification, multiclass_classification]
  temporal_handling: [not_applicable]
  interpretability: [none_reported]
created: 2026-07-05
updated: 2026-07-05
---

# janisch2020_costly_features

## Bibliographic Record
Janisch, Jaromir, Tomas Pevny, and Viliam Lisy. "Classification with Costly Features as a Sequential Decision-Making Problem." Machine Learning 109, no. 8 (2020): 1587-1615. https://doi.org/10.1007/s10994-020-05874-8.

## Plain-Language Summary
This paper treats classification with costly features as a sequential decision problem. A model decides whether to buy another feature or stop and classify, under average or hard per-sample budgets.

## Structured Summary

### Research Question
Can classification with costly features be formulated as an MDP and solved flexibly with deep reinforcement learning under different budget constraints?

### Study Type
Method development and benchmark evaluation.

### Data Source
Several benchmark datasets and real-world-inspired settings with missing features.

### Population
Not a clinical population.

### Index Date or Time Origin
Not applicable.

### Observation Window
Not applicable.

### Prediction Horizon or Follow-up
Not applicable.

### Inputs or Predictors
Partially acquired feature vectors with feature costs.

### Outcome or Target
Correct class prediction while respecting feature acquisition cost/budget.

### Methods
The authors formulate average-budget and hard-budget costly-feature classification problems, convert them into MDPs, and solve them with deep reinforcement learning.

### ML or AI Method Index
The core method is reinforcement learning for adaptive feature acquisition and classification.

### Model Inputs and Representations
The state consists of observed feature values and unobserved feature indicators.

### Baselines or Comparators
Prior algorithms for costly feature classification.

### Evaluation
Performance is evaluated across datasets and budget settings.

### Main Findings
The proposed method performs robustly across average budget, hard budget, and sparse/missing-feature settings, outperforming prior algorithms in the authors' experiments.

### Author-Stated Limitations
The authors note that theoretical guarantees are lost when using neural function approximation.

### Funding, Conflicts, and Ethics
Not extracted in this draft.

### Notes on Missing or Ambiguous Information
The paper is not medical, but its motivating examples include diagnosis with costly tests.
