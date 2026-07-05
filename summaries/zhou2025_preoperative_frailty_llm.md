---
citation_key: zhou2025_preoperative_frailty_llm
summary_status: complete
source_status: full_text
paper_type: journal_article
ml_ai_methods:
  uses_ml_ai: true
  method_families:
    - transformer
    - foundation_model
    - llm
    - embedding_model
  specific_methods:
    - BERT
    - RoBERTa
    - BioBERT
    - PubMedBERT
    - VES-13
    - eFI
  learning_setup:
    - supervised_learning
  input_modalities:
    - clinical_notes
    - structured_ehr
    - diagnosis_codes
    - labs
    - cognitive_tests
  prediction_task:
    - binary_classification
    - phenotyping
  temporal_handling:
    - fixed_observation_window
  interpretability:
    - none_reported
created: 2026-07-05
updated: 2026-07-05
---

# zhou2025_preoperative_frailty_llm

## Bibliographic Record
Zhou, Ying Qiu, Onkar Litake, Minhthy N. Meineke, Jeffrey L. Tully, Nicole Xu, Waseem Abdou, and Rodney A. Gabriel. "A Large Language Model Approach to Identifying Preoperative Frailty Among Older Adults From Clinical Notes." Journal of the American Geriatrics Society 73, no. 8 (2025): 2422-2430. https://doi.org/10.1111/jgs.19545.

## Plain-Language Summary
This study trains transformer language models to identify preoperative frailty from anesthesia preoperative clinic notes. It compares labels based on a patient questionnaire, VES-13, with labels based on an electronic frailty index. The best-performing model depended strongly on which label source was used. Models trained on VES-13 labels performed very well on VES-13 validation and reasonably on eFI validation, while models trained on eFI labels did not generalize well to VES-13 validation. The paper is useful because it shows both the promise of clinical-note LLM classifiers and the importance of label choice.

## Structured Summary

### Research Question
Can large language model-based classifiers identify preoperative frailty from anesthesia preoperative clinical notes, and how does performance vary when frailty labels come from VES-13 versus eFI?

### Study Type
Retrospective observational model-development and validation study.

### Data Source
Preoperative anesthesia clinic notes from a single institution. The study used two separate spine-surgery datasets: one labeled with VES-13 questionnaire responses and one labeled with an electronic frailty index.

### Population
Patients undergoing major spine surgery. The VES-13 dataset included 479 older adults aged 65 or older. The eFI dataset included 998 patients undergoing complex spine surgery who were not included in the VES-13 dataset.

### Index Date or Time Origin
The preoperative anesthesia clinic note associated with the surgery was the model input. The classification target was preoperative frailty.

### Observation Window
The input text was taken from the preanesthesia clinic note, specifically medical history, history of present illness, and assessment/plan sections. Some inputs were truncated because models used a 512-token maximum sequence length.

### Prediction Horizon or Follow-up
Not a future-outcome prediction study. The task was binary classification of current preoperative frailty.

### Inputs or Predictors
Preoperative anesthesia clinic history and physical notes. Labels came from either VES-13 score or eFI score. The eFI incorporates comorbidities, functional status, labs, and physical exam findings from the EHR.

### Outcome or Target
Binary frailty classification. VES-13 frailty used score >= 3. eFI frailty used score >= 0.3.

### Methods
The VES-13 and eFI datasets were split 50/25/25 into training, validation, and test sets. The authors trained BERT, RoBERTa, BioBERT, and PubMedBERT classifiers. They froze base model weights and trained classification heads. Metrics included AUC, precision-recall curves, F1 score, accuracy, sensitivity, and specificity with bootstrapped confidence intervals.

### ML or AI Method Index
The core methods are supervised transformer-based text classifiers. The paper calls these large language models and evaluates general-domain, biomedical, and clinical variants.

### Model Inputs and Representations
The models used selected note sections from preoperative anesthesia notes. Text was tokenized and limited to 512 tokens.

### Baselines or Comparators
The paper compares four language model architectures and compares training/validation label sources: VES-13-trained models tested on VES-13 and eFI sets, and eFI-trained models tested on eFI and VES-13 sets.

### Evaluation
When trained and validated on VES-13 labels, AUCs were 0.99 for RoBERTa, 0.64 for BERT, 0.67 for BioBERT, and 0.73 for PubMedBERT. When VES-13-trained models were tested on eFI validation, AUCs were 0.63, 0.83, 0.87, and 0.87. When trained and validated on eFI, AUCs were around 0.88-0.91. When eFI-trained models were tested on VES-13 validation, AUCs were only about 0.60-0.62.

### Main Findings
Clinical notes can support automated frailty classification, but performance depends heavily on the label source. VES-13-trained models appeared to capture frailty more directly and transferred better to eFI validation than the reverse. The authors argue that eFI may be less granular or may capture a different construct than VES-13.

### Author-Stated Limitations
The study used spine surgical patients from one center rather than broader perioperative populations. Inputs were focused on anesthesia preoperative notes, and documentation heterogeneity across institutions could affect generalization. Unstructured clinical language includes abbreviations, misspellings, and provider variation. Some note inputs were truncated because of token limits.

### Funding, Conflicts, and Ethics
The study was IRB approved and exempt from informed consent because the dataset was de-identified. Dr. Gabriel reported institutional research funding and consulting relationships unrelated to the manuscript; other authors declared no conflicts.

### Notes on Missing or Ambiguous Information
The paper does not report calibration or clinical threshold selection for deployment. It is highly relevant to label-definition strategy because VES-13 and eFI labels did not transfer symmetrically.
