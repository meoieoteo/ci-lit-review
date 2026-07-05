---
citation_key: pellegrini2018_neuroimaging_ml_review
summary_status: draft
source_status: full_text
paper_type: preprint
ml_ai_methods:
  uses_ml_ai: true
  method_families: [svm, neural_network, random_forest, other]
  specific_methods: []
  learning_setup: [supervised_learning]
  input_modalities: [imaging, biomarkers, cognitive_tests, demographics]
  prediction_task: [binary_classification, multiclass_classification, phenotyping]
  temporal_handling: [cross_sectional, longitudinal_history]
  interpretability: [none_reported]
created: 2026-07-05
updated: 2026-07-05
---

# pellegrini2018_neuroimaging_ml_review

## Bibliographic Record
Pellegrini, Enrico, Lucia Ballerini, Maria del C. Valdes Hernandez, Francesca M. Chappell, Victor Gonzalez-Castro, Devasuda Anblagan, Samuel Danso, et al. "Machine learning of neuroimaging to diagnose cognitive impairment and dementia: A systematic review and comparative analysis." 2018. https://doi.org/10.48550/arXiv.1804.01961.

## Plain-Language Summary
This systematic review evaluates machine-learning studies using neuroimaging to distinguish healthy aging, MCI, and dementia. The field reported better performance for easier contrasts such as AD versus healthy controls, but poorer performance for clinically harder categories such as MCI converters versus non-converters.

## Structured Summary

### Research Question
How accurately do machine-learning neuroimaging studies diagnose cognitive impairment and dementia across clinically relevant boundaries?

### Study Type
Systematic review and comparative analysis.

### Data Source
Published studies from 2006 to late 2016.

### Population
Participants in included neuroimaging studies, commonly healthy controls, MCI participants, and people with AD or other dementia types.

### Index Date or Time Origin
Varied by included study.

### Observation Window
Varied by included study.

### Prediction Horizon or Follow-up
Varied; some studies considered MCI converter versus non-converter classification.

### Inputs or Predictors
Mostly neuroimaging, especially T1-weighted MRI, sometimes combined with other data types.

### Outcome or Target
Diagnostic categories spanning healthy aging, MCI, and dementia.

### Methods
The authors reviewed 111 studies, assessed study quality, and compared reported accuracy across disease boundaries, data sources, sample sizes, and ML methods.

### ML or AI Method Index
The paper reviews multiple machine-learning classifiers for neuroimaging-based diagnosis.

### Model Inputs and Representations
Neuroimaging-derived features are the main representation.

### Baselines or Comparators
Comparisons are across study designs, disease boundaries, data types, and ML methods.

### Evaluation
Reported accuracy across included studies.

### Main Findings
Most studies assessed AD versus healthy controls, used ADNI, support vector machines, and T1-weighted MRI. Accuracy was highest for AD versus healthy controls and poorer for healthy control versus MCI versus AD and MCI converter versus non-converter tasks. Combined data types improved accuracy more than sample size, data source, or ML method.

### Author-Stated Limitations
The authors conclude that machine learning did not yet differentiate clinically relevant disease categories sufficiently and called for more diverse datasets, multimodal data, and clinical integration.

### Funding, Conflicts, and Ethics
Not extracted in this draft.

### Notes on Missing or Ambiguous Information
This paper is neuroimaging-focused rather than EHR-text-focused.
