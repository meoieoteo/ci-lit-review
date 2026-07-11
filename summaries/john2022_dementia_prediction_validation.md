---
citation_key: john2022_dementia_prediction_validation
summary_status: draft
source_status: full_text
paper_type: journal_article
ml_ai_methods:
  uses_ml_ai: true
  method_families: [logistic_regression, survival_model, random_forest, svm, other]
  specific_methods: [Walters Dementia Risk Score, Mehta RxDx-Dementia Risk Index, Nori ADRD prediction model, OMOP CDM, OHDSI PLP]
  learning_setup: [supervised_learning]
  input_modalities: [claims, structured_ehr, diagnosis_codes, medications, demographics]
  input_representation: [fixed_length_vector, engineered_features, bag_of_codes]
  prediction_task: [risk_prediction, binary_classification, survival_time_to_event]
  temporal_handling: [fixed_observation_window, time_to_event]
  interpretability: [coefficients, calibration]
created: 2026-07-05
updated: 2026-07-11
---

# john2022_dementia_prediction_validation

## Bibliographic Record
John, Luis H., Jan A. Kors, Egill A. Fridgeirsson, Jenna M. Reps, and Peter R. Rijnbeek. "External Validation of Existing Dementia Prediction Models on Observational Health Data." BMC Medical Research Methodology 22, no. 1 (2022). https://doi.org/10.1186/s12874-022-01793-5.

## Plain-Language Summary
This paper reviews existing dementia prediction models and tests whether they can be externally validated using observational health databases. Most published models lacked enough reporting detail for full validation, and only three selected models were externally validated.

## Structured Summary

### Research Question
Can published dementia prediction models be externally validated on observational health data, and is the published reporting sufficient to support validation?

### Study Type
Model-reporting review plus external validation study.

### Data Source
Published dementia prediction model studies from 2011-2020 and observational health databases mapped to the OMOP common data model.

### Population
Populations vary by model. The externally validated models include older adults or disease-specific groups such as people with diabetes and hypertension.

### Index Date or Time Origin
Varied by model. The paper specifically evaluates whether index date is reported.

### Observation Window
Varied by model and validation database.

### Prediction Horizon or Follow-up
Mostly three- to five-year time-at-risk windows where reported; some models lacked explicit time-at-risk.

### Inputs or Predictors
Routinely collected observational health data, including demographics, diagnosis codes, medication data, and other structured predictors depending on the model.

### Outcome or Target
Incident dementia or Alzheimer disease and related dementias.

### Methods
The authors defined reporting criteria required for external validation, reviewed published models, and externally validated Walters, Mehta, and Nori models using OHDSI patient-level prediction infrastructure.

### ML or AI Method Index
The reviewed literature includes Cox models, logistic regression, random forest, SVM, and other prediction methods. The external validation applies existing model specifications rather than training new models.

### Model Inputs and Representations
Structured observational health data are represented in OMOP CDM format and transformed into model-specific fixed-length predictor sets, such as demographic variables, diagnosis-code indicators, medication-derived predictors, and risk-score components. The externally validated models use fixed observation windows and time-at-risk definitions rather than variable-length EHR sequence modeling.

### Baselines or Comparators
Development performance from original papers and external validation performance across databases.

### Evaluation
Metrics include discrimination and calibration where possible, including c-statistic/AUROC and calibration measures.

### Main Findings
The review identified 59 dementia prediction models. All reported prediction method, development database, and target/outcome definitions, but only 22 reported index date, 21 reported predictor time window, and 9 reported full model specifications. Walters and Nori models transported reasonably to some databases; recalibration could not be assessed for the Mehta model because baseline hazard was not reported.

### Author-Stated Limitations
The authors conclude that reporting is often insufficient for full external validation and that uncertainty remains about how models work in other clinical settings.

### Funding, Conflicts, and Ethics
Not extracted in this draft.

### Notes on Missing or Ambiguous Information
This paper is directly relevant to model transportability and reporting rather than new model development.
