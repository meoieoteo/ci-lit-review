---
citation_key: penfold2022_mci_nlp
summary_status: complete
source_status: full_text
paper_type: journal_article
publication_status: peer_reviewed_version_of_record
ml_ai_methods:
  uses_ml_ai: true
  method_families: [logistic_regression, rule_based_nlp, concept_extraction]
  specific_methods: [LASSO]
  learning_setup: [supervised_learning]
  input_modalities: [clinical_notes, cognitive_tests, demographics]
  input_representation: [concept_features, engineered_features, fixed_length_vector]
  prediction_task: [binary_classification, phenotyping]
  temporal_handling: [lookback_window]
  interpretability: [clinical_concepts]
created: 2026-07-12
updated: 2026-07-12
---

# penfold2022_mci_nlp

## Bibliographic Record

Penfold et al., "Natural language processing for prediction of mild cognitive impairment in primary care: a pilot study," BMC Medical Informatics and Decision Making, 2022.

## Publication and Source Status

This summary is based on the full-text peer-reviewed journal article saved as `papers/penfold2022_mci_nlp.pdf`.

## Plain-Language Summary

The study tested whether phrases in routine clinical notes could identify patients with mild cognitive impairment when structured cognitive screening or diagnostic information is not routinely available. The authors annotated notes, mapped text to cognitive-function concepts, and trained a LASSO logistic regression model. The resulting model had modest discrimination and very high specificity at one reported operating point, but very low sensitivity.

## Structured Summary

### Research Question

Can cognitive-function concepts extracted from primary-care clinical notes identify mild cognitive impairment in routine-care patients?

### Study Type

Retrospective NLP and prediction-model pilot study.

### Data Source

Kaiser Permanente Washington Epic Clarity notes linked to standardized cognitive assessments from the Adult Changes in Thought study and a general primary-care population.

### Population

The paper used 1,794 ACT participants and 2,391 general-population patients. Exclusions included prior Alzheimer disease/dementia and donepezil use; additional general-population exclusions included prior MCI, Parkinson disease, and psychotic disorder.

### Index Date or Time Origin

The index was anchored to standardized cognitive assessment dates.

### Observation Window

The study covered clinical notes and assessments from January 1, 2004 through September 30, 2015.

### Prediction Horizon or Follow-up

The task was identifying MCI status around cognitive assessment rather than long-horizon future dementia prediction.

### Inputs or Predictors

The model used note-derived cognitive-function concepts. The authors annotated 10,391 clinic notes and mapped phrases to 42 concepts.

### Outcome or Target

MCI-positive status was defined using cognitive assessment scores; ACT CASI scores were converted to MMSE, and MMSE/MoCA scores at or below 26 were treated as positive.

### Methods

The authors extracted cognitive phrases from notes, mapped them to concepts, and trained a LASSO logistic regression model.

### ML or AI Method Index

Rule-based/concept extraction plus supervised LASSO logistic regression.

### Model Inputs and Representations

Patient-level engineered concept features derived from clinical text.

### Baselines or Comparators

A demographics-only comparator is reported.

### Evaluation

The model was trained using ACT plus 60% of the general-population sample and validated on the remaining 40% of the general-population sample, with tenfold cross-validation in development.

### Main Findings

The validation AUC was 0.670 (95% CI 0.638 to 0.702), compared with 0.598 for demographics alone. At a cutoff of 0.60, reported specificity was 99.7% and PPV was 70%, but sensitivity was about 1.7%.

### Author-Stated Limitations

The authors emphasize the pilot nature of the study, modest discrimination, low sensitivity at the high-specificity operating point, and measurement issues because cognitive tests were not routinely administered.

### Funding, Conflicts, and Ethics

Funding, ethics, and conflict details should be checked in the source before manuscript use.

### Notes on Missing or Ambiguous Information

The degree to which note concepts transport to other EHRs, specialties, and note types is not established by this pilot.
