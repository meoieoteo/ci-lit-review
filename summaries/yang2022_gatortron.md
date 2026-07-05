---
citation_key: yang2022_gatortron
summary_status: draft
source_status: full_text
paper_type: journal_article
ml_ai_methods:
  uses_ml_ai: true
  method_families: [llm, foundation_model, transformer, concept_extraction]
  specific_methods: [GatorTron, BERT]
  learning_setup: [self_supervised_learning, supervised_learning]
  input_modalities: [clinical_notes]
  prediction_task: [representation_learning, phenotyping]
  temporal_handling: [not_applicable]
  interpretability: [none_reported]
created: 2026-07-05
updated: 2026-07-05
---

# yang2022_gatortron

## Bibliographic Record
Yang, Xi, Aokun Chen, Nima PourNejatian, Hoo Chang Shin, Kaleb E. Smith, Christopher Parisien, Colin Compas, et al. "A Large Language Model for Electronic Health Records." npj Digital Medicine 5, no. 1 (2022). https://doi.org/10.1038/s41746-022-00742-2.

## Plain-Language Summary
GatorTron is a large clinical language model trained from scratch on a very large corpus of EHR clinical text and biomedical text. The study tests whether scaling model size and training data improves clinical NLP tasks.

## Structured Summary

### Research Question
Does scaling clinical language models to billions of parameters and very large EHR text corpora improve clinical NLP performance?

### Study Type
Large language model development and benchmark evaluation.

### Data Source
UF Health Integrated Data Repository clinical notes and additional text sources.

### Population
The corpus includes 290,482,002 clinical notes from 2,476,628 patients across UF Health encounters from 2011-2021.

### Index Date or Time Origin
Not applicable.

### Observation Window
Clinical notes from 2011-2021.

### Prediction Horizon or Follow-up
Not applicable.

### Inputs or Predictors
De-identified clinical narratives and biomedical text.

### Outcome or Target
Clinical NLP benchmark task labels for concept extraction, relation extraction, semantic textual similarity, natural language inference, and medical question answering.

### Methods
The authors train GatorTron models at base, medium, and large scales, up to 8.9 billion parameters, and compare effects of scaling both model size and training-data size.

### ML or AI Method Index
The core method is large transformer language-model pre-training for clinical text.

### Model Inputs and Representations
Clinical text is represented through large-scale contextual language-model embeddings.

### Baselines or Comparators
Existing biomedical and clinical transformer models.

### Evaluation
Five clinical NLP tasks: named entity recognition, medical relation extraction, semantic textual similarity, natural language inference, and medical question answering.

### Main Findings
GatorTron models outperformed prior biomedical and clinical transformer models across the five tasks. The abstract reports 9.6% and 9.5% accuracy improvements for NLI and medical question answering.

### Author-Stated Limitations
Not extracted in this draft.

### Funding, Conflicts, and Ethics
Not extracted in this draft.

### Notes on Missing or Ambiguous Information
This is a foundation-model paper rather than a clinical outcome prediction study.
