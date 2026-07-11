---
citation_key: adejumo2024_hf_functional_status_nlp
summary_status: complete
source_status: full_text
paper_type: journal_article
ml_ai_methods:
  uses_ml_ai: true
  method_families:
    - transformer
    - foundation_model
    - concept_extraction
  specific_methods:
    - ClinicalBERT
    - MedSpaCy
    - SHAP
  learning_setup:
    - supervised_learning
  input_modalities:
    - clinical_notes
    - structured_ehr
    - diagnosis_codes
    - procedures
    - demographics
  input_representation:
    - raw_text
    - document_chunks
    - sequence_tokens
    - dense_embeddings
  prediction_task:
    - multiclass_classification
    - phenotyping
  temporal_handling:
    - longitudinal_history
    - fixed_observation_window
  interpretability:
    - saliency
    - feature_importance
created: 2026-07-05
updated: 2026-07-11
---

# adejumo2024_hf_functional_status_nlp

## Bibliographic Record
Adejumo, Philip, Phyllis M. Thangaraj, Lovedeep Singh Dhingra, Arya Aminorroaya, Xinyu Zhou, Cynthia Brandt, Hua Xu, Harlan M. Krumholz, and Rohan Khera. "Natural Language Processing of Clinical Documentation to Assess Functional Status in Patients With Heart Failure." JAMA Network Open 7, no. 11 (2024): e2443925. https://doi.org/10.1001/jamanetworkopen.2024.43925.

## Plain-Language Summary
This diagnostic study developed ClinicalBERT-based NLP models to extract heart-failure functional status from unstructured outpatient notes. The models identified explicit New York Heart Association (NYHA) class mentions and inferred activity- or rest-related heart-failure symptoms when NYHA class was not written directly. In 34,070 patients with heart failure across three Yale New Haven Health System outpatient networks, the models achieved high discrimination at the development site and two validation sites. Deployment across unannotated notes substantially increased capture of functional status information compared with explicit NYHA mentions alone.

## Structured Summary

### Research Question
Can transformer-based NLP extract NYHA class and activity- or rest-related heart-failure symptoms from unstructured clinical documentation?

### Study Type
Retrospective diagnostic study using EHR data and expert-annotated clinical notes.

### Data Source
Yale New Haven Health System EHR data from 2013-2022, extracted from Epic Clarity. Source data included structured fields and unstructured outpatient medical notes. Supplemental material describes note sectioning, sentence-level annotation, ClinicalBERT fine-tuning, and SHAP-based interpretability.

### Population
34,070 adult patients with heart failure and at least one outpatient encounter in Yale New Haven Hospital, Northeast Medical Group, or Greenwich Hospital cardiovascular outpatient practices.

### Index Date or Time Origin
Encounter-level outpatient notes were the unit of NLP classification. The broader source window was January 1, 2013 through June 30, 2022.

### Observation Window
The study used outpatient notes across the EHR period. Annotated development and validation notes came from site-specific samples; deployed models were applied to 182,308 outpatient notes not used in model development or validation.

### Prediction Horizon or Follow-up
Not a future-risk prediction study. The task was note-level extraction/classification of current documented functional status.

### Inputs or Predictors
Unstructured outpatient notes, sectioned to focus on history of present illness and assessment/plan. The cohort was identified using structured EHR elements such as diagnosis codes and encounter information.

### Outcome or Target
Expert-annotated labels for explicit NYHA class and activity- or rest-related heart-failure symptom descriptions. NYHA classes II and III were combined in some analyses because of treatment-guideline use and documentation variability.

### Methods
The authors fine-tuned a ClinicalBERT-based model for two document classification tasks: detecting NYHA class mentions and classifying symptoms with activity or rest. They used sentence-level annotation with note-level aggregation. The YNHH annotated set was split 80/10/10 for training, validation, and internal testing. NMG and GH samples were used as external validation sites. SHAP was adapted for transformer interpretability.

### ML or AI Method Index
The core method is supervised transformer-based clinical NLP using ClinicalBERT. The paper also uses MedSpaCy for sectioning and SHAP for token-level interpretability.

### Model Inputs and Representations
The model consumed selected sections of outpatient clinical notes as tokenized text for ClinicalBERT classification. The supplemental material states that MedSpaCy sectioning removed less relevant sections such as past medical history, labs, physical exam, medications, family history, imaging, and review of systems. The task is note-level/document-level extraction rather than a longitudinal EHR sequence model; timing is handled through note selection rather than explicit irregular-time modeling.

### Baselines or Comparators
The main comparator was expert EHR abstraction. The deployment analysis compared functional-status capture using explicit NYHA mentions alone versus explicit mentions plus NLP-based symptom recategorization.

### Evaluation
The NYHA model had micro-averaged AUROC 0.99 at YNHH, 0.98 at NMG, and 0.98 at GH. The activity/rest symptom model had AUROC 0.94 at YNHH, 0.94 at NMG, and 0.95 at GH. Subgroup analyses reported consistent AUROC values by race, sex, and ejection-fraction category.

### Main Findings
Only 13.1% of 182,308 outpatient notes had explicit NYHA mentions. NLP-based symptom classification added 10.8% more encounters, increasing functional-status classification to 23.9% of notes, an 83% increase over explicit mentions alone. The models also identified additional functional-status information in the year before ICD implantation.

### Author-Stated Limitations
The authors note possible dependence on annotation guidelines and local documentation style, reliance on a single primary annotator with quality-control review, difficulty distinguishing nuanced HF symptom limitations and class II versus III documentation, comorbidity-related ambiguity, and the choice of lightweight ClinicalBERT over larger newer LLMs.

### Funding, Conflicts, and Ethics
The Yale IRB approved the study and waived informed consent. Dr. Khera was supported by NIH funding. Dr. Thangaraj reported a pending patent unrelated to the work. Additional disclosures are listed in the article.

### Notes on Missing or Ambiguous Information
The paper reports strong discrimination but not calibration. It is an extraction/phenotyping study rather than a patient-outcome risk model. The approach is relevant to extracting functional state from notes, but the target is heart-failure NYHA status rather than cognitive impairment.
