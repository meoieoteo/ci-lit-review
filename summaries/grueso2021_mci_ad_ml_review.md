---
citation_key: grueso2021_mci_ad_ml_review
summary_status: draft
source_status: full_text
paper_type: journal_article
ml_ai_methods:
  uses_ml_ai: true
  method_families: [svm, neural_network, random_forest, other]
  specific_methods: [support vector machine, convolutional neural network, random forest]
  learning_setup: [supervised_learning]
  input_modalities: [imaging, biomarkers, genetics, cognitive_tests, demographics]
  prediction_task: [binary_classification, risk_prediction]
  temporal_handling: [longitudinal_history, fixed_observation_window]
  interpretability: [none_reported]
created: 2026-07-05
updated: 2026-07-05
---

# grueso2021_mci_ad_ml_review

## Bibliographic Record
Grueso, Sergio, and Raquel Viejo-Sobera. "Machine learning methods for predicting progression from mild cognitive impairment to Alzheimer's disease dementia: a systematic review." Alzheimer's Research & Therapy 13, no. 1 (2021). https://doi.org/10.1186/s13195-021-00900-w.

## Plain-Language Summary
This systematic review examines machine-learning studies predicting progression from MCI to Alzheimer disease dementia. Most studies used ADNI neuroimaging data, especially MRI, and support vector machines were the most common algorithm. Reported accuracy varied, and multimodal MRI plus PET studies tended to perform better than single-modality studies.

## Structured Summary

### Research Question
What machine-learning methods and data sources have been used to predict MCI progression to AD dementia, and how accurate are they?

### Study Type
Systematic review.

### Data Source
Published studies identified through database searches; most included studies used ADNI.

### Population
Participants in included studies generally included stable MCI, progressive MCI, AD, and healthy control groups.

### Index Date or Time Origin
Varied by included study, usually baseline MCI assessment.

### Observation Window
Varied by included study; the review notes follow-up definitions such as three years for ADNI and one year for AddNeuroMed in some contexts.

### Prediction Horizon or Follow-up
Progression from MCI to AD dementia during study-specific follow-up periods.

### Inputs or Predictors
Mainly neuroimaging features from MRI and PET, sometimes combined with genetic, cognitive, or other clinical variables.

### Outcome or Target
Stable MCI versus progressive MCI / conversion to AD dementia.

### Methods
The authors followed PRISMA-style review methods and extracted study design, data source, neuroimaging modality, features, classifier, validation method, accuracy, and AUC.

### ML or AI Method Index
The review covers multiple supervised ML methods, with SVM most common and CNNs reporting higher average accuracy in the included literature.

### Model Inputs and Representations
Most included models used imaging-derived features; some used multimodal feature sets.

### Baselines or Comparators
The review compares methods and modalities across studies rather than reanalyzing data directly.

### Evaluation
The review reports accuracy and AUC where available.

### Main Findings
Of 116 reviewed studies, most used ADNI data, MRI, and SVM. SVM had mean accuracy around 75.4%, while convolutional neural networks had mean accuracy around 78.5%. MRI plus PET studies generally performed better than single-modality studies.

### Author-Stated Limitations
The review highlights concerns about generalizability, heavy reliance on ADNI, and clinically relevant prediction remaining difficult.

### Funding, Conflicts, and Ethics
Not extracted in this draft.

### Notes on Missing or Ambiguous Information
This review is focused largely on neuroimaging, not EHR text.
