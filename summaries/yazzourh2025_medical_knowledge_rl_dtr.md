---
citation_key: yazzourh2025_medical_knowledge_rl_dtr
summary_status: draft
source_status: full_text
paper_type: journal_article
ml_ai_methods:
  uses_ml_ai: true
  method_families: [reinforcement_learning]
  specific_methods: [dynamic treatment regimes, expert knowledge integration, reinforcement learning]
  learning_setup: [reinforcement_learning, not_applicable]
  input_modalities: [structured_ehr, other]
  prediction_task: [policy_learning]
  temporal_handling: [longitudinal_history, visit_sequence]
  interpretability: [rules, concept_features]
created: 2026-07-05
updated: 2026-07-05
---

# yazzourh2025_medical_knowledge_rl_dtr

## Bibliographic Record
Yazzourh, Sophia, Nicolas Savy, Philippe Saint-Pierre, and Michael R. Kosorok. "Medical Knowledge Integration Into Reinforcement Learning Algorithms for Dynamic Treatment Regimes." International Statistical Review, ahead of print, June 2025. https://doi.org/10.1111/insr.12617.

## Plain-Language Summary
This review explains how reinforcement learning can be used for dynamic treatment regimes and how medical expertise can be integrated into RL models. It emphasizes that expert knowledge may improve safety, interpretability, efficiency, and clinical adoption.

## Structured Summary

### Research Question
How can medical knowledge be integrated into reinforcement-learning algorithms for dynamic treatment regimes?

### Study Type
Methodological review.

### Data Source
Published methodological literature on reinforcement learning, precision medicine, and dynamic treatment regimes.

### Population
Not applicable.

### Index Date or Time Origin
Sequential treatment decision stages.

### Observation Window
Patient medical history across treatment stages, conceptually.

### Prediction Horizon or Follow-up
Long-term cumulative reward over treatment sequences.

### Inputs or Predictors
Patient states, histories, treatments/actions, rewards, and medical expert knowledge.

### Outcome or Target
Treatment policies that optimize long-term clinical outcomes while incorporating medical knowledge.

### Methods
The paper reviews RL foundations, DTR framing, and approaches for integrating expert knowledge into RL.

### ML or AI Method Index
The core method family is reinforcement learning for policy learning in precision medicine.

### Model Inputs and Representations
Decision processes model patient state, actions, transitions, and rewards.

### Baselines or Comparators
RL without expert knowledge and traditional DTR approaches are conceptual comparators.

### Evaluation
Review paper; no single empirical benchmark.

### Main Findings
The authors argue that medical expertise can increase confidence in RL recommendations, improve safety and interpretability, reduce learning time, and facilitate adoption by clinicians and patients.

### Author-Stated Limitations
The paper discusses barriers to clinical use of RL, including safety, interpretability, and practical deployment concerns.

### Funding, Conflicts, and Ethics
Supported by ANR LabEx CIMI according to the paper.

### Notes on Missing or Ambiguous Information
This is policy-learning background, not a risk-score paper.
