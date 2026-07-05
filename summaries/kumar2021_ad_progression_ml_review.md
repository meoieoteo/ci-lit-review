---
citation_key: kumar2021_ad_progression_ml_review
summary_status: draft
source_status: full_text
paper_type: journal_article
ml_ai_methods:
  uses_ml_ai: true
  method_families: [svm, neural_network, random_forest, logistic_regression, other]
  specific_methods: []
  learning_setup: [supervised_learning]
  input_modalities: [structured_ehr, clinical_notes, imaging, labs, demographics, cognitive_tests]
  prediction_task: [risk_prediction, binary_classification]
  temporal_handling: [longitudinal_history, not_reported]
  interpretability: [none_reported]
created: 2026-07-05
updated: 2026-07-05
---

# kumar2021_ad_progression_ml_review

## Bibliographic Record
Kumar, Sayantan, Inez Oh, Suzanne Schindler, Albert M. Lai, Philip R. O. Payne, and Aditi Gupta. "Machine learning for modeling the progression of Alzheimer disease dementia using clinical data: a systematic literature review." JAMIA Open 4, no. 3 (2021). https://doi.org/10.1093/jamiaopen/ooab052.

## Plain-Language Summary
This systematic review summarizes machine-learning studies that use clinical data to model Alzheimer disease dementia progression. The reviewed literature grew substantially in the five years before publication and relied heavily on public datasets with neuroimaging, neurobehavioral scores, demographics, and laboratory values.

## Structured Summary

### Research Question
How have machine-learning methods been applied to clinical data from EHR-like or clinical datasets to model AD dementia progression?

### Study Type
Systematic literature review.

### Data Source
PubMed, Scopus, ScienceDirect, IEEE Xplore, ACM Digital Library, and arXiv searches for studies published from January 1, 2010 through May 31, 2020.

### Population
Populations varied across the 64 included articles.

### Index Date or Time Origin
Varied by included study.

### Observation Window
Varied by included study.

### Prediction Horizon or Follow-up
Varied by included study.

### Inputs or Predictors
Clinical data including neurobehavioral status exam scores, patient demographics, neuroimaging data, laboratory test values, and in principle structured EHR data and clinical notes.

### Outcome or Target
AD dementia progression or risk of progression.

### Methods
The authors used predefined selection criteria and summarized included papers by data characteristics, computational algorithms, and research focus.

### ML or AI Method Index
The review covers supervised ML methods used for AD progression modeling.

### Model Inputs and Representations
Most reviewed work used public datasets combining neuroimaging and clinical variables.

### Baselines or Comparators
The review compares broad classes of included studies rather than applying a common benchmark.

### Evaluation
Evaluation metrics vary across included studies.

### Main Findings
The review included 64 articles and found a rise in ML-based AD dementia progression modeling. Most studies focused on public datasets with both neuroimaging and clinical data.

### Author-Stated Limitations
The abstract emphasizes data sharing and reproducibility as needs for adaptation and generalizability.

### Funding, Conflicts, and Ethics
Not extracted in this draft.

### Notes on Missing or Ambiguous Information
The paper is a review rather than a single model-development study.
