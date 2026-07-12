---
citation_key: mccoy2020_dementia_ehr
summary_status: complete
source_status: full_text
paper_type: journal_article
publication_status: peer_reviewed_version_of_record
ml_ai_methods:
  uses_ml_ai: true
  method_families: [survival_model, rule_based_nlp]
  specific_methods: [Fine-Gray competing risk regression]
  learning_setup: [statistical_association]
  input_modalities: [clinical_notes, diagnosis_codes, demographics]
  input_representation: [engineered_features, bag_of_words_or_terms, fixed_length_vector]
  prediction_task: [survival_time_to_event, risk_prediction]
  temporal_handling: [follow_up_time, censoring]
  interpretability: [cognitive_symptom_terms]
created: 2026-07-12
updated: 2026-07-12
---

# mccoy2020_dementia_ehr

## Bibliographic Record

McCoy et al., "Stratifying risk for dementia onset using large-scale electronic health record data: a retrospective cohort study," Alzheimer's & Dementia, 2020.

## Publication and Source Status

This summary is based on full-text HTML saved as `papers/mccoy2020_dementia_ehr.html`.

## Plain-Language Summary

This retrospective cohort study asked whether a cognitive-symptom score extracted from hospital discharge notes was associated with later dementia diagnosis. The score was associated with earlier incident dementia diagnosis over up to eight years of follow-up.

## Structured Summary

### Research Question

Does cognitive symptomatology estimated from discharge notes stratify future dementia diagnosis risk?

### Study Type

Retrospective cohort with time-to-event modeling.

### Data Source

Longitudinal EHR data from two large academic medical centers.

### Population

The cohort included 267,855 hospitalized adults without prior/current dementia diagnosis at index.

### Index Date or Time Origin

Index was an inpatient hospitalization discharge; one hospitalization was randomly selected when patients had multiple eligible discharges.

### Observation Window

Hospital discharges from 2005 through 2017 were used.

### Prediction Horizon or Follow-up

Patients were followed for up to eight years for incident dementia diagnosis.

### Inputs or Predictors

The main exposure was a cognitive symptom score derived from discharge-note terms. Models adjusted for age, sex, white race, and Charlson comorbidity.

### Outcome or Target

Incident dementia diagnosis code during inpatient or outpatient follow-up.

### Methods

The authors used a validated NLP-derived cognitive symptom score and Fine-Gray competing-risk regression.

### ML or AI Method Index

Rule-based/term-list NLP exposure plus survival modeling.

### Model Inputs and Representations

Discharge-note cognitive symptom score and structured covariates.

### Baselines or Comparators

The study reports adjusted associations and replication in a second hospital system and age subgroup.

### Evaluation

The main estimate used competing-risk regression over 1,251,858 patient-years of follow-up.

### Main Findings

There were 6,516 new dementia diagnoses. The cognitive symptom score was associated with earlier dementia diagnosis, with adjusted hazard ratio 1.63 (95% CI 1.54 to 1.72).

### Author-Stated Limitations

The study relies on EHR documentation and diagnosis codes and uses hospitalized populations and discharge-note text.

### Funding, Conflicts, and Ethics

Funding, conflicts, and ethics details should be checked in the source before citation.

### Notes on Missing or Ambiguous Information

The cognitive score is not an outpatient cardiology pre-encounter feature as implemented; adaptation would require outpatient note sources and timing controls.
