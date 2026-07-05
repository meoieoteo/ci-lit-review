---
citation_key: lee2019_biobert
summary_status: draft
source_status: full_text
paper_type: journal_article
ml_ai_methods:
  uses_ml_ai: true
  method_families: [transformer, foundation_model, embedding_model, concept_extraction]
  specific_methods: [BioBERT, BERT]
  learning_setup: [self_supervised_learning, supervised_learning]
  input_modalities: [other]
  prediction_task: [representation_learning, phenotyping]
  temporal_handling: [not_applicable]
  interpretability: [none_reported]
created: 2026-07-05
updated: 2026-07-05
---

# lee2019_biobert

## Bibliographic Record
Lee, Jinhyuk, Wonjin Yoon, Sungdong Kim, Donghyeon Kim, Sunkyu Kim, Chan Ho So, and Jaewoo Kang. "BioBERT: a pre-trained biomedical language representation model for biomedical text mining." Bioinformatics 36, no. 4 (2019): 1234-1240. https://doi.org/10.1093/bioinformatics/btz682.

## Plain-Language Summary
BioBERT adapts BERT to biomedical literature by additional pre-training on large biomedical corpora. It improves performance across biomedical named entity recognition, relation extraction, and question answering tasks.

## Structured Summary

### Research Question
Does pre-training BERT on biomedical corpora improve biomedical text-mining performance?

### Study Type
Model development and benchmark evaluation.

### Data Source
Large biomedical corpora including PubMed abstracts and PubMed Central full-text articles.

### Population
Not applicable.

### Index Date or Time Origin
Not applicable.

### Observation Window
Not applicable.

### Prediction Horizon or Follow-up
Not applicable.

### Inputs or Predictors
Biomedical text.

### Outcome or Target
Named entity recognition, relation extraction, and biomedical question answering benchmark labels.

### Methods
The authors continue BERT pre-training on biomedical text and fine-tune the resulting model for multiple biomedical NLP tasks.

### ML or AI Method Index
BioBERT is a transformer foundation model specialized through domain-adaptive pre-training.

### Model Inputs and Representations
Biomedical text is represented with contextual token embeddings.

### Baselines or Comparators
General BERT and prior state-of-the-art biomedical text-mining models.

### Evaluation
NER F1, relation-extraction F1, and question-answering mean reciprocal rank are reported.

### Main Findings
BioBERT improved biomedical NER by 0.62 F1 points, relation extraction by 2.80 F1 points, and question answering by 12.24 MRR points compared with prior state of the art.

### Author-Stated Limitations
Not extracted in this draft.

### Funding, Conflicts, and Ethics
Not extracted in this draft.

### Notes on Missing or Ambiguous Information
BioBERT is trained on biomedical literature, not clinical notes or EHR data.
