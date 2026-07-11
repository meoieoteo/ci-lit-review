---
citation_key: lu2026_ehr_dementia_prediction_review
summary_status: complete
source_status: full_text
paper_type: journal_article
ml_ai_methods:
  uses_ml_ai: true
  method_families:
    - logistic_regression
    - tree_model
    - random_forest
    - gradient_boosting
    - neural_network
    - transformer
    - concept_extraction
    - embedding_model
    - other
  specific_methods: []
  learning_setup:
    - supervised_learning
    - statistical_association
  input_modalities:
    - structured_ehr
    - clinical_notes
    - medications
    - diagnosis_codes
    - labs
    - procedures
    - demographics
    - other
  input_representation:
    - fixed_length_vector
    - engineered_features
    - concept_features
    - dense_embeddings
    - raw_text
    - not_reported
  prediction_task:
    - binary_classification
    - risk_prediction
    - phenotyping
  temporal_handling:
    - fixed_observation_window
    - longitudinal_history
    - time_to_event
    - not_reported
  interpretability:
    - coefficients
    - feature_importance
    - calibration
    - none_reported
created: 2026-07-05
updated: 2026-07-11
---

# lu2026_ehr_dementia_prediction_review

## Bibliographic Record
Lu, Alicia, Velandai Srikanth, Sarah Westworth, Yue-Guang Baey, Chris Moran, Richard Beare, Kristy Siostrom, Nadine Andrew, and Taya Collyer. "Electronic health record-based prediction models for dementia detection: a systematic review of model performance and quality." Journal of the American Medical Informatics Association 33, no. 6 (2026): 1210-1224. https://doi.org/10.1093/jamia/ocag048.

## Plain-Language Summary
This systematic review asks whether existing electronic health record-based dementia prediction models are good enough, well reported enough, and clinically clear enough to support real-world use. The authors find a rapidly growing literature, but also substantial methodological weakness. Most models rely on structured EHR data, many use unclear or weak outcome definitions based on diagnosis codes, calibration is rarely reported, and external validation is uncommon. The authors conclude that EHR-based dementia prediction is not yet clinically mature and needs clearer use cases, better reference standards, stronger validation, better reporting, and interdisciplinary development.

## Structured Summary

### Research Question
What is the performance, methodological quality, and risk of bias of prediction models that use routine EHR data to detect existing dementia or predict future dementia?

### Study Type
Systematic review of multivariable prediction model studies. The review followed TRIPOD-SRMA and was prospectively registered in PROSPERO.

### Data Source
The authors searched Medline, EMBASE, Scopus, IEEE Xplore, ACM, Google Scholar, arXiv, medRxiv, and bioRxiv. Database searches ran from inception through July 15, 2024, and grey literature searches ran through September 24, 2024.

### Population
The included studies used EHR-derived data from clinical populations. Most studies used single-country datasets, especially from the United States and United Kingdom. The included models covered diagnostic and prognostic dementia prediction settings.

### Index Date or Time Origin
Index date definitions varied across included studies and were often not clearly reported. The review highlights ambiguity in whether models aimed to identify recorded dementia, unrecognized current dementia, or future dementia risk.

### Observation Window
Observation windows varied across included studies and were inconsistently reported. Some models used longitudinal EHR histories; others used less clearly specified EHR snapshots or feature windows.

### Prediction Horizon or Follow-up
Among prognostic models, prediction horizons ranged from 1 day to 10 years, with most under 5 years.

### Inputs or Predictors
Predictors came from routine EHR data. Structured predictors commonly included demographics, medical conditions, procedures, medications, labs, vital signs, and utilization. Unstructured predictors came from clinical text such as clinic letters and progress notes, using approaches ranging from keyword lists to embeddings and engineered text features.

### Outcome or Target
Included models targeted diagnostic detection of dementia or prognostic prediction of future dementia. Operational outcomes were heterogeneous. Many studies used recorded dementia diagnosis codes, medication codes, rule-based definitions, specialist clinic codes, manual chart review, or machine-learning-derived labels as reference standards. Only 4 studies, covering 17 models, used established clinical diagnostic criteria.

### Methods
The review included 56 studies, 434 developed prediction models, and 155 external validations. Data extraction was guided by CHARMS and TRIPOD+AI. Risk of bias was assessed with PROBAST. Because of heterogeneity in model designs and performance reporting, the authors did not perform a formal meta-analysis; they synthesized results narratively and summarized AUROC values descriptively.

### ML or AI Method Index
The paper is itself a systematic review, not a new model-development study. It indexes and compares statistical, machine-learning, deep-learning, and hybrid EHR prediction models. Across included models, 129 used statistical methods, 193 used machine learning, 96 used deep learning, and 10 used combined methods. The authors report no major internal-validation AUROC advantage for AI methods over traditional statistical methods.

### Model Inputs and Representations
Most models used structured EHR data only: 347 of 434 models. Forty-six models used unstructured data only, and 41 used both structured and unstructured EHR data. Across included studies, input representations were heterogeneous and often incompletely reported. Many models appear to have used fixed-length engineered feature sets from structured EHR history, while unstructured data representations included simple keyword approaches, text-derived concept or topic features, embeddings, and other engineered NLP features. The review does not support a single classification of all included models as either fixed-vector or variable-length time-aware EHR sequence models.

### Baselines or Comparators
The review compared models descriptively by data type, model type, validation level, and modeling method. It compared apparent, internal, and external validation AUROC; structured versus unstructured versus combined EHR data; diagnostic versus prognostic models; and statistical versus AI-based methods.

### Evaluation
Discrimination was the most commonly reported performance domain. AUROC was reported for 352 models. Calibration was reported for 69 models across 9 studies. External validation was performed for 47 models, representing 11% of developed models. Mean AUROC was 0.76 for apparent performance, 0.79 for internal validation, and 0.74 for external validation.

### Main Findings
Fifty-six studies met inclusion criteria. Most models were prognostic, used US data, and relied solely on structured EHR data. Outcome definitions were often unclear or weakly connected to the intended clinical task. Only 4% of models used established clinical criteria as the dementia reference standard. Calibration and threshold reporting were sparse. All 434 developed models were rated high risk of bias, mostly because of analysis and outcome-domain problems. Among 155 external validations, 134 were high risk of bias and the remainder were unclear.

### Author-Stated Limitations
The authors state that heterogeneity in model design and reporting prevented formal meta-analysis. Their synthesis relied on published information, which was often incomplete. Some PROBAST judgments may be subjective because reporting quality was poor.

### Funding, Conflicts, and Ethics
The paper reports no specific grant funding. Alicia Lu was supported by an Australian Government Research Training Program scholarship through Monash University. The authors declared no conflicts of interest.

### Notes on Missing or Ambiguous Information
The review depends heavily on the quality of included studies. Many included models did not clearly specify prediction task, index date, outcome timing, missing-data handling, threshold choice, or calibration. Supplementary files contain detailed extraction and PROBAST ratings, but they were not part of this summary pass.
