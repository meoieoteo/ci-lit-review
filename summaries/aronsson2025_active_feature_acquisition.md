---
citation_key: aronsson2025_active_feature_acquisition
summary_status: draft
source_status: full_text
paper_type: preprint
ml_ai_methods:
  uses_ml_ai: true
  method_families: [pomdp, reinforcement_learning, value_of_information, tree_model, other]
  specific_methods: [active feature acquisition, dynamic feature selection, POMDP]
  learning_setup: [reinforcement_learning, simulation, not_applicable]
  input_modalities: [other]
  prediction_task: [feature_acquisition, binary_classification, multiclass_classification]
  temporal_handling: [not_applicable]
  interpretability: [rules, feature_importance]
created: 2026-07-05
updated: 2026-07-05
---

# aronsson2025_active_feature_acquisition

## Bibliographic Record
Aronsson, Linus, Arman Rahbar, and Morteza Haghir Chehreghani. "A Survey on Active Feature Acquisition Strategies." 2025. https://doi.org/10.48550/arXiv.2502.11067.

## Plain-Language Summary
This survey organizes active feature acquisition methods, where a model sequentially decides which costly feature to acquire next and when to stop and predict. It frames the problem as a POMDP and connects recent methods to older work in information acquisition, decision trees, and value-of-information reasoning.

## Structured Summary

### Research Question
How can active feature acquisition methods be unified, compared, and connected to structured POMDP planning?

### Study Type
Methodological survey.

### Data Source
Published literature on active feature acquisition, dynamic feature selection, cost-sensitive trees, POMDPs, and related information-acquisition methods.

### Population
Not applicable.

### Index Date or Time Origin
Not applicable.

### Observation Window
Not applicable.

### Prediction Horizon or Follow-up
Not applicable.

### Inputs or Predictors
Partially observed feature vectors with feature-specific acquisition costs.

### Outcome or Target
Prediction after sequential feature acquisition, with objective trading prediction quality against acquisition cost.

### Methods
The authors present a POMDP formulation and group methods into embedded cost-aware predictors, model-based planning methods, model-free policy-learning methods, and hybrid methods.

### ML or AI Method Index
The paper covers POMDP, reinforcement-learning, decision-tree, and value-of-information approaches to deciding which features to acquire.

### Model Inputs and Representations
Instances are represented by observed feature subsets that grow as the acquisition policy selects additional features.

### Baselines or Comparators
The survey compares method families rather than running a new benchmark.

### Evaluation
Not applicable as a primary empirical evaluation.

### Main Findings
The authors argue that a POMDP-centric view clarifies connections among active feature acquisition methods and exposes routes to stronger algorithmic guarantees.

### Author-Stated Limitations
The survey notes that much prior work is heuristic and lacks formal guarantees.

### Funding, Conflicts, and Ethics
Not extracted in this draft.

### Notes on Missing or Ambiguous Information
This is not a medical paper, but it is relevant to sequential test or information acquisition.
