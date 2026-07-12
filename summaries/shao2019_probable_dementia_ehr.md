---
citation_key: shao2019_probable_dementia_ehr
summary_status: complete
source_status: full_text
paper_type: journal_article
publication_status: peer_reviewed_version_of_record
ml_ai_methods:
  uses_ml_ai: true
  method_families: [logistic_regression, rule_based_nlp, concept_extraction, other]
  specific_methods: [latent Dirichlet allocation, stable topic extraction, MALLET, logistic regression]
  learning_setup: [weak_supervision, unsupervised_learning, supervised_learning]
  input_modalities: [structured_ehr, clinical_notes, medications, diagnosis_codes, procedures]
  input_representation: [fixed_length_vector, engineered_features, concept_features, bag_of_codes, bag_of_words_or_terms]
  prediction_task: [binary_classification, risk_prediction, phenotyping]
  temporal_handling: [fixed_observation_window, longitudinal_history]
  interpretability: [coefficients, concept_features]
created: 2026-07-11
updated: 2026-07-11
---

# shao2019_probable_dementia_ehr

## Bibliographic Record

Shao, Yijun, Qing T. Zeng, Kathryn K. Chen, Andrew Shutes-David, Stephen M. Thielke, and Debby W. Tsuang. "Detection of probable dementia cases in undiagnosed patients using structured and unstructured electronic health records." BMC Medical Informatics and Decision Making 19, no. 1 (2019): 128. https://doi.org/10.1186/s12911-019-0846-4.

## Publication and Source Status

Peer-reviewed open-access journal article. The summary is based on the full publisher PDF saved at `papers/shao2019_probable_dementia_ehr.pdf`.

## Plain-Language Summary

This study developed a weakly supervised EHR model to find Veterans who may have dementia despite lacking a dementia diagnosis code. The authors used known coded dementia cases as an imperfect "silver standard," built features from structured EHR data and clinical-note topics, trained a logistic regression risk score, and then manually reviewed a stratified sample of uncoded patients to estimate how well the score identified probable undiagnosed dementia.

## Structured Summary

### Research Question

Can structured and unstructured Veterans Health Administration EHR data be used to detect probable dementia among patients who do not have dementia ICD-9 codes?

### Study Type

Retrospective EHR phenotyping and risk-score development study with manual chart-review validation.

### Data Source

Veterans Health Administration EHR data from the VA Puget Sound setting, accessed through the VA Corporate Data Warehouse and VINCI.

### Population

Cases were Veterans aged 65 or older with a first dementia ICD-9 diagnosis from a specialty clinic between FY2009 and FY2014 and sufficient visits/notes in each of the three preceding years. Controls were Veterans aged 65 or older with inpatient or outpatient VA contact, no dementia-related diagnosis codes, and no anti-dementia medication prescriptions over the three-year analysis period. Controls were matched 5:1 to cases by sex, age within five years, and Charlson comorbidity category. The model-development cohort included 1,861 coded dementia cases and 9,305 controls.

### Index Date or Time Origin

For cases, the time origin was the first ICD-9 dementia diagnosis date. For controls, a random visit date was selected as an index date.

### Observation Window

Structured and unstructured clinical data were collected for the three years before, but not including, the first dementia diagnosis date for cases or the selected index date for controls.

### Prediction Horizon or Follow-up

The model was framed as detection of probable currently undiagnosed dementia among controls, not prospective prediction over a future horizon.

### Inputs or Predictors

Inputs included ICD codes other than dementia codes, CPT codes, medications, clinical document types, and topic features derived from clinical note text.

### Outcome or Target

For model development, the weak supervision target was coded dementia case versus non-coded control status. For validation of uncoded patients, dementia specialists manually reviewed clinical notes from sampled controls and classified subjects as dementia, non-dementia, or unclear using DSM-5 guidelines.

### Methods

The authors used latent Dirichlet allocation in MALLET to extract raw topics from sampled clinical notes, repeated LDA three times, then applied stable topic extraction. Topic presence was defined using inferred topic proportions. Structured and topic features were selected by case-control association. A logistic regression model generated prediction scores. A stratified validation sample of 120 controls across risk-score bins was manually reviewed by two dementia specialists, and a fitted relationship between risk score and chart-review dementia rate was used to estimate ROC performance and threshold behavior.

### ML or AI Method Index

The core strategy was weak supervision: coded dementia cases and matched uncoded controls were used to train a logistic regression score, while unsupervised topic modeling converted raw clinical notes into fixed topic features. The representation was a fixed-length engineered vector combining structured EHR features and text-derived topic features.

### Model Inputs and Representations

The model input unit was patient-level history over a three-year window. Longitudinal structured events and notes were collapsed into fixed-length features. The model did not consume a variable-length visit sequence or raw note sequence directly. Timing was handled through a fixed pre-index lookback window, not through explicit irregular-time sequence encoding.

### Baselines or Comparators

The paper compared feature distributions between coded dementia cases and controls. It did not present a formal structured-only versus text-only versus combined model performance table in the extracted full text, although both structured and unstructured features contributed to the combined model.

### Evaluation

Validation included manual record review by dementia specialists. An initial 20-subject review found high agreement with ICD-coded dementia status. A second stratified sample of 120 controls was reviewed to estimate undiagnosed dementia rates by score bin. When unclear cases were handled as dementia or non-dementia, AUCs were 0.912 and 0.908, respectively. A threshold of 0.061 had sensitivity about 0.825 and specificity about 0.832.

### Main Findings

The model selected 853 features, including 290 topics, 174 non-dementia ICD codes, 159 CPT codes, 59 medications, and 171 note types. Dementia-related topics occurred far more often among coded cases than controls. The authors concluded that structured and unstructured EHR data can identify probable undiagnosed dementia among patients without dementia codes and that ICD codes alone are insufficient as a gold standard.

### Author-Stated Limitations

The authors state that the algorithm was applied in geriatric specialty clinics rather than the broader primary-care VHA population, that the mostly male Veteran population limits generalizability to women, that dementia specialists could not definitively classify every subject from records alone, and that the study did not contact high-risk patients to determine willingness to undergo further workup.

### Funding, Conflicts, and Ethics

The study was supported by a VA VISN-20 Geriatric Research, Education, and Clinical Center Clinical Demonstration Project and NIA R56 AG059739. The authors reported no competing interests. The VA Puget Sound IRB approved the study with waiver of HIPAA authorization and consent.

### Notes on Missing or Ambiguous Information

The paper does not provide enough detail here to fully reconstruct all structured feature definitions, topic-term lists, or model coefficients. It also does not fully separate the contribution of structured features from note-derived features in model performance.
