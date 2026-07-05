---
citation_key: grammenos2024_explainable_mci_ad
summary_status: draft
source_status: full_text
paper_type: journal_article
ml_ai_methods:
  uses_ml_ai: true
  method_families: [gradient_boosting, tree_model]
  specific_methods: [XGBoost, Recursive Feature Elimination, SHAP]
  learning_setup: [supervised_learning]
  input_modalities: [structured_ehr, imaging, biomarkers, genetics, cognitive_tests, demographics]
  prediction_task: [binary_classification, risk_prediction]
  temporal_handling: [longitudinal_history, fixed_observation_window]
  interpretability: [feature_importance, saliency]
created: 2026-07-05
updated: 2026-07-05
---

# grammenos2024_explainable_mci_ad

## Bibliographic Record
Grammenos, Gerasimos, Aristidis G. Vrahatis, Panagiotis Vlamos, Dean Palejev, and Themis Exarchos. "Predicting the Conversion from Mild Cognitive Impairment to Alzheimer's Disease Using an Explainable AI Approach." Information 15, no. 5 (2024): 249. https://doi.org/10.3390/info15050249.

## Plain-Language Summary
This paper predicts conversion from MCI to Alzheimer disease using ADNI data, gradient boosting, feature selection, and SHAP explanations. The model uses longitudinal data from baseline through follow-up and reports 85% accuracy for predicting transition versus stability.

## Structured Summary

### Research Question
Can an explainable machine-learning model predict which MCI patients will convert to AD?

### Study Type
Supervised model development study using ADNI data.

### Data Source
ADNIMERGE data from ADNI phases ADNI1, ADNI2, ADNI3, and ADNI-GO.

### Population
The paper describes an initial ADNI dataset of 2378 participants and a modeled MCI cohort with stable and transition groups after preprocessing.

### Index Date or Time Origin
Baseline ADNI visit.

### Observation Window
Longitudinal data from baseline through follow-up visits, including a 48-month observation framing in the methods.

### Prediction Horizon or Follow-up
The abstract describes a 36-month prediction period; the introduction and methods also discuss 48-month transition framing.

### Inputs or Predictors
ADNI clinical, cognitive, imaging, genetic, biomarker, and demographic variables available in ADNIMERGE.

### Outcome or Target
Stable MCI versus MCI transition to Alzheimer disease.

### Methods
The authors compare multiple classifiers, select XGBoost, tune hyperparameters, use Recursive Feature Elimination, and apply SHAP values for explanation.

### ML or AI Method Index
The main model is XGBoost with feature selection and post hoc SHAP explanation.

### Model Inputs and Representations
Tabular ADNI features are used directly after preprocessing and feature selection.

### Baselines or Comparators
The paper compares XGBoost with other machine-learning classifiers including CatBoost, LightGBM, logistic regression, SVM, random forest, decision tree, and naive Bayes.

### Evaluation
Five-fold cross-validation is reported with precision, recall, F1, accuracy, and ROC AUC.

### Main Findings
The reported average accuracy is 0.85 and ROC AUC is 0.86. Stable class precision/recall/F1 were 0.94/0.84/0.90, and transition class precision/recall/F1 were 0.71/0.88/0.79.

### Author-Stated Limitations
Not extracted in detail in this draft.

### Funding, Conflicts, and Ethics
The study uses ADNI data; ADNI investigators contributed data infrastructure but not the analysis.

### Notes on Missing or Ambiguous Information
The paper uses both 36-month and 48-month language. A later review should reconcile the exact target horizon from the methods and cohort construction.
