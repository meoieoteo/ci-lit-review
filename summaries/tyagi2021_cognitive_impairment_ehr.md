---
citation_key: tyagi2021_cognitive_impairment_ehr
summary_status: complete
source_status: full_text
paper_type: conference_paper
publication_status: workshop_abstract_or_preprint
ml_ai_methods:
  uses_ml_ai: true
  method_families: [logistic_regression, transformer]
  specific_methods: [TF-IDF, ClinicalBERT]
  learning_setup: [supervised_learning]
  input_modalities: [clinical_notes, genetics]
  input_representation: [bag_of_words_or_terms, sequence_tokens, document_chunks]
  prediction_task: [binary_classification, phenotyping]
  temporal_handling: [not_reported]
  interpretability: [not_reported]
created: 2026-07-12
updated: 2026-07-12
---

# tyagi2021_cognitive_impairment_ehr

## Bibliographic Record

Tyagi et al., "Using Deep Learning to Identify Patients with Cognitive Impairment in Electronic Health Records," ML4H extended abstract/arXiv, 2021.

## Publication and Source Status

This summary is based on the full text saved as `papers/tyagi2021_cognitive_impairment_ehr.pdf`.

## Plain-Language Summary

The study trains NLP models to identify evidence of cognitive impairment in EHR note snippets among older patients. ClinicalBERT outperformed a TF-IDF logistic regression baseline on the annotated sequence-level task.

## Structured Summary

### Research Question

Can deep learning identify cognitive impairment evidence in EHR text?

### Study Type

Retrospective annotation and text-classification study reported as a short workshop/preprint paper.

### Data Source

Mass General Brigham BioBank-linked EHR notes.

### Population

Patients were older than 60, had APOE genotype data, and had at least one clinician note with a dementia-related keyword.

### Index Date or Time Origin

The source does not define a patient-level prediction index for risk scoring.

### Observation Window

The authors extracted 800-character sequences around dementia-related keywords.

### Prediction Horizon or Follow-up

The task is text evidence classification rather than future risk prediction.

### Inputs or Predictors

Annotated note sequences.

### Outcome or Target

Sequence-level evidence of cognitive impairment, labeled Yes/No/Neither. Family or patient concern alone was not considered cognitive impairment.

### Methods

The authors compared L1-regularized TF-IDF logistic regression with fine-tuned ClinicalBERT.

### ML or AI Method Index

ClinicalBERT and TF-IDF logistic regression.

### Model Inputs and Representations

Keyword-centered text snippets represented as TF-IDF features or transformer token sequences.

### Baselines or Comparators

TF-IDF logistic regression was the primary baseline.

### Evaluation

The final annotated dataset included 8,656 sequences from 2,487 patients, split 90% train and 10% holdout.

### Main Findings

ClinicalBERT reported AUC 0.98, accuracy 0.93, sensitivity 0.91, and specificity 0.96; TF-IDF logistic regression reported AUC 0.95 and accuracy 0.84.

### Author-Stated Limitations

The short paper provides limited detail on temporal deployment, patient-level validation, transportability, and downstream use.

### Funding, Conflicts, and Ethics

Funding, conflict, and ethics details should be checked in the source before citation.

### Notes on Missing or Ambiguous Information

The source is useful for NLP feasibility but does not provide a full risk-prediction study design.
