---
citation_key: alsentzer2019_clinical_bert_embeddings
summary_status: draft
source_status: full_text
paper_type: conference_paper
ml_ai_methods:
  uses_ml_ai: true
  method_families: [transformer, foundation_model, embedding_model, concept_extraction]
  specific_methods: [BERT, BioBERT, Clinical BERT, Discharge Summary BERT]
  learning_setup: [self_supervised_learning, supervised_learning]
  input_modalities: [clinical_notes]
  input_representation: [raw_text, sequence_tokens, dense_embeddings]
  prediction_task: [representation_learning, phenotyping]
  temporal_handling: [not_applicable]
  interpretability: [none_reported]
created: 2026-07-05
updated: 2026-07-11
---

# alsentzer2019_clinical_bert_embeddings

## Bibliographic Record
Alsentzer, Emily, John R. Murphy, Willie Boag, Wei-Hung Weng, Di Jin, Tristan Naumann, and Matthew B. A. McDermott. "Publicly Available Clinical BERT Embeddings." Proceedings of the 2nd Clinical Natural Language Processing Workshop, 2019, 72-78. https://doi.org/10.18653/v1/W19-1909.

## Plain-Language Summary
This paper trains and releases BERT models specialized for clinical text. The authors pre-train models on MIMIC-III notes and evaluate them on clinical named entity recognition, medical natural language inference, and de-identification tasks. Clinical-domain pre-training improves several clinical NLP tasks compared with general BERT and BioBERT, but not all de-identification tasks.

## Structured Summary

### Research Question
Can BERT models pre-trained on clinical notes improve downstream clinical NLP performance?

### Study Type
Model development and benchmark evaluation.

### Data Source
Approximately 2 million notes from MIMIC-III v1.4 for pre-training, with downstream evaluations on MedNLI and i2b2 clinical NLP datasets.

### Population
No patient cohort is analyzed as a clinical population. The source text comes from ICU clinical notes in MIMIC-III.

### Index Date or Time Origin
Not applicable.

### Observation Window
Not applicable beyond the MIMIC-III note corpus and downstream task datasets.

### Prediction Horizon or Follow-up
Not applicable.

### Inputs or Predictors
Clinical text tokens from MIMIC-III notes and task-specific labeled text.

### Outcome or Target
Named entity labels, de-identification labels, and natural language inference labels depending on the benchmark.

### Methods
The authors trained Clinical BERT from BERT-Base and Clinical BioBERT from BioBERT using MIMIC clinical notes. They also trained all-note and discharge-summary variants and fine-tuned models for downstream tasks.

### ML or AI Method Index
The core method is transformer language-model pre-training followed by task-specific supervised fine-tuning.

### Model Inputs and Representations
The model represents tokenized clinical text with contextual token embeddings learned from clinical notes. The representation is text-sequence based for NLP tasks, not a patient-level fixed-length EHR feature vector and not a longitudinal EHR timing model.

### Baselines or Comparators
General-domain BERT and BioBERT are the main comparators.

### Evaluation
Performance is evaluated on two i2b2 named entity recognition tasks, two i2b2 de-identification tasks, and MedNLI.

### Main Findings
Clinical-domain BERT variants improve performance on clinical NER and MedNLI tasks. General BERT and BioBERT perform better on the de-identification tasks, which the authors attribute to differences between de-identified pre-training text and synthetic non-de-identified task text.

### Author-Stated Limitations
The paper emphasizes task dependence: clinical pre-training does not uniformly improve every clinical NLP task.

### Funding, Conflicts, and Ethics
Not extracted in this draft.

### Notes on Missing or Ambiguous Information
This summary does not extract every benchmark score. The paper is primarily a reusable model-resource paper, not a clinical outcome study.
