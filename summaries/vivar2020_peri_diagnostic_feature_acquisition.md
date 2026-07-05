---
citation_key: vivar2020_peri_diagnostic_feature_acquisition
summary_status: draft
source_status: full_text
paper_type: conference_paper
ml_ai_methods:
  uses_ml_ai: true
  method_families: [neural_network, value_of_information, other]
  specific_methods: [integrated gradients, accumulated integrated gradients, input dropout]
  learning_setup: [supervised_learning]
  input_modalities: [structured_ehr, imaging, labs, other]
  prediction_task: [feature_acquisition, binary_classification, multiclass_classification]
  temporal_handling: [not_applicable]
  interpretability: [saliency, feature_importance]
created: 2026-07-05
updated: 2026-07-05
---

# vivar2020_peri_diagnostic_feature_acquisition

## Bibliographic Record
Vivar, Gerome, Kamilia Mullakaeva, Andreas Zwergal, Nassir Navab, and Seyed-Ahmad Ahmadi. "Peri-Diagnostic Decision Support Through Cost-Efficient Feature Acquisition at Test-Time." In Medical Image Computing and Computer Assisted Intervention - MICCAI 2020. Springer International Publishing, 2020. https://doi.org/10.1007/978-3-030-59713-9_55.

## Plain-Language Summary
This paper proposes a feature-acquisition method for diagnostic decision support. Given already collected evidence, the model recommends which examination or feature to acquire next, balancing expected diagnostic value and cost.

## Structured Summary

### Research Question
Can integrated gradients guide cost-efficient test-time feature acquisition for diagnostic decision support?

### Study Type
Method development and benchmark evaluation.

### Data Source
Two public medical datasets and two synthetic datasets.

### Population
Not a single clinical cohort; public medical datasets are used for evaluation.

### Index Date or Time Origin
The decision point is the current diagnostic state with partial features observed.

### Observation Window
Sequential acquisition during a diagnostic workflow.

### Prediction Horizon or Follow-up
Not a future prediction task; the target is diagnosis after feature acquisition.

### Inputs or Predictors
Partially observed feature vectors and feature costs.

### Outcome or Target
Accurate diagnosis with fewer or lower-cost acquired features.

### Methods
The authors train neural networks with input dropout and use integrated gradients at test time to estimate which missing feature is most valuable. They introduce accumulated integrated gradients for dynamic acquisition.

### ML or AI Method Index
The core method combines neural classification with feature-attribution-guided acquisition.

### Model Inputs and Representations
Structured feature vectors with missing/acquired feature masks.

### Baselines or Comparators
Prior RL and non-RL cost-sensitive feature acquisition methods.

### Evaluation
Accuracy and feature/cost efficiency on medical and synthetic datasets.

### Main Findings
The proposed approach is reported to be more cost- and feature-efficient than prior approaches while achieving higher overall accuracy.

### Author-Stated Limitations
The paper discusses limitations of prior RL and attribution approaches; detailed limitations of the proposed method are not extracted in this draft.

### Funding, Conflicts, and Ethics
Not extracted in this draft.

### Notes on Missing or Ambiguous Information
This paper is about within-diagnostic feature acquisition, not pre-encounter risk scoring.
