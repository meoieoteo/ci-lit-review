---
citation_key: amini2024_speech_ad_progression
summary_status: draft
source_status: full_text
paper_type: journal_article
ml_ai_methods:
  uses_ml_ai: true
  method_families: [transformer, foundation_model, embedding_model, logistic_regression]
  specific_methods: [automatic speech recognition, speaker diarization, transformer sentence encoder, logistic regression]
  learning_setup: [supervised_learning]
  input_modalities: [speech, demographics, genetics, cognitive_tests, other]
  prediction_task: [binary_classification, risk_prediction]
  temporal_handling: [fixed_observation_window]
  interpretability: [coefficients, feature_importance]
created: 2026-07-05
updated: 2026-07-05
---

# amini2024_speech_ad_progression

## Bibliographic Record
Amini, Samad, Boran Hao, Jingmei Yang, Cody Karjadi, Vijaya B. Kolachalama, Rhoda Au, and Ioannis C. Paschalidis. "Prediction of Alzheimer's disease progression within 6 years using speech: A novel approach leveraging language models." Alzheimer's & Dementia 20, no. 8 (2024): 5262-5270. https://doi.org/10.1002/alz.13886.

## Plain-Language Summary
This study uses automatically transcribed speech from neuropsychological test interviews to predict which people with mild cognitive impairment will progress to Alzheimer disease within six years. The best models use text-derived features and simple demographic information, and they outperform models based on traditional neuropsychological test scores alone.

## Structured Summary

### Research Question
Can language-model features derived from speech recordings predict MCI-to-AD progression within six years?

### Study Type
Retrospective supervised prediction study.

### Data Source
Framingham Heart Study neuropsychological test interview recordings and related participant information.

### Population
166 participants with MCI, including 90 progressive MCI cases and 76 stable MCI cases.

### Index Date or Time Origin
The neuropsychological test interview associated with MCI status is the time origin.

### Observation Window
The model uses speech from neuropsychological testing at baseline. Follow-up identifies progression over a six-year window.

### Prediction Horizon or Follow-up
Progression to AD within six years.

### Inputs or Predictors
Automatically transcribed speech, age, sex, education, APOE, selected health factors, traditional neuropsychological test scores, and MMSE in different feature sets.

### Outcome or Target
Binary progression from MCI to AD within six years.

### Methods
The pipeline uses speech recognition, speaker diarization, subtest classification, text representation with language-model features, dimensionality reduction/feature selection, and logistic regression. Evaluation used stratified group 10-fold cross-validation with repeated runs.

### ML or AI Method Index
The core AI component is speech-to-text plus transformer-based language representation, followed by supervised logistic-regression classification.

### Model Inputs and Representations
The main representation is text automatically transcribed from neuropsychological interviews, split by subtests and encoded into language-model features.

### Baselines or Comparators
Comparators include demographics, APOE, health factors, traditional neuropsychological test scores, and MMSE.

### Evaluation
Metrics included AUC, accuracy, sensitivity, precision, specificity, and F1 score.

### Main Findings
The best model using text, demographics, APOE, and health factors achieved AUC 78.5 and F1 79.9. Text-only and text-plus-demographics models performed similarly. Traditional neuropsychological test scores had AUC 71.3, and MMSE had AUC 60.7.

### Author-Stated Limitations
The authors frame the work as an automated screening/prognosis approach requiring further development for remote and broad deployment.

### Funding, Conflicts, and Ethics
Funding included NSF and NIH support, as listed in the paper.

### Notes on Missing or Ambiguous Information
This is speech/NPT-based, not EHR-text-based. Acoustic features were not used; the analysis relied on automatically transcribed text.
