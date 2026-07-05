---
citation_key: kaelbling1998_pomdp_survey
summary_status: draft
source_status: full_text
paper_type: journal_article
ml_ai_methods:
  uses_ml_ai: true
  method_families: [pomdp, reinforcement_learning, value_of_information]
  specific_methods: [MDP, POMDP, finite-memory controller]
  learning_setup: [not_applicable]
  input_modalities: [other]
  prediction_task: [policy_learning]
  temporal_handling: [visit_sequence]
  interpretability: [not_applicable]
created: 2026-07-05
updated: 2026-07-05
---

# kaelbling1998_pomdp_survey

## Bibliographic Record
Kaelbling, Leslie Pack, Michael L. Littman, and Anthony R. Cassandra. "Planning and Acting in Partially Observable Stochastic Domains." Artificial Intelligence 101, nos. 1-2 (1998): 99-134. https://doi.org/10.1016/S0004-3702(98)00023-X.

## Plain-Language Summary
This foundational paper introduces MDPs and POMDPs for planning under uncertainty. It explains how agents can choose actions when the true state is only partially observed and actions may both gather information and change the world.

## Structured Summary

### Research Question
How can optimal action policies be computed for stochastic domains where the agent cannot directly observe the true state?

### Study Type
Foundational methods paper / survey with algorithmic contribution.

### Data Source
Not applicable.

### Population
Not applicable.

### Index Date or Time Origin
Sequential decision steps.

### Observation Window
The agent's action-observation history is summarized through belief states.

### Prediction Horizon or Follow-up
Planning horizon depends on the POMDP specification.

### Inputs or Predictors
States, actions, observations, transition probabilities, observation probabilities, rewards, and beliefs.

### Outcome or Target
An optimal or approximately optimal policy for action under partial observability.

### Methods
The paper introduces MDP/POMDP theory, describes offline solution methods, and discusses extracting finite-memory controllers.

### ML or AI Method Index
The core framework is POMDP planning, which is closely related to reinforcement learning and value-of-information reasoning.

### Model Inputs and Representations
Uncertainty over state is represented as a belief distribution.

### Baselines or Comparators
The paper contrasts POMDPs with fully observable MDPs and deterministic planning.

### Evaluation
Primarily theoretical and algorithmic discussion.

### Main Findings
POMDPs offer a unified framework in which actions that gather information and actions that change the world are optimized together.

### Author-Stated Limitations
The authors note computational complexity and limitations of enumerative state representations.

### Funding, Conflicts, and Ethics
Not extracted in this draft.

### Notes on Missing or Ambiguous Information
This is not a clinical paper; it supports sequential diagnosis and information-acquisition theory.
