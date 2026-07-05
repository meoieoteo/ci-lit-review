---
citation_key: singhal2022_medpalm
summary_status: draft
source_status: full_text
paper_type: preprint
ml_ai_methods:
  uses_ml_ai: true
  method_families: [llm, foundation_model, transformer]
  specific_methods: [PaLM, Flan-PaLM, Med-PaLM, MultiMedQA, HealthSearchQA, chain-of-thought, self-consistency, instruction prompt tuning]
  learning_setup: [self_supervised_learning, supervised_learning]
  input_modalities: [other]
  prediction_task: [not_applicable]
  temporal_handling: [not_applicable]
  interpretability: [none_reported]
created: 2026-07-05
updated: 2026-07-05
---

# singhal2022_medpalm

## Bibliographic Record
Singhal, Karan, Shekoofeh Azizi, Tao Tu, S. Sara Mahdavi, Jason Wei, Hyung Won Chung, Nathan Scales, et al. "Large Language Models Encode Clinical Knowledge." 2022. https://arxiv.org/abs/2212.13138.

## Plain-Language Summary
This paper evaluates large language models on medical question answering and introduces Med-PaLM. It also proposes MultiMedQA, a benchmark combining medical exams, research questions, medication questions, consumer health search questions, and clinician/lay human evaluation of long-form answers.

## Structured Summary

### Research Question
How well do large language models encode and express clinical knowledge across medical question-answering tasks?

### Study Type
Benchmark and model-alignment study.

### Data Source
MultiMedQA, combining six existing datasets and the newly introduced HealthSearchQA.

### Population
Not a patient cohort.

### Index Date or Time Origin
Not applicable.

### Observation Window
Not applicable.

### Prediction Horizon or Follow-up
Not applicable.

### Inputs or Predictors
Medical natural-language questions, sometimes with answer choices or supporting PubMed abstracts.

### Outcome or Target
Multiple-choice accuracy and human-rated long-form answer quality.

### Methods
The authors evaluate PaLM and Flan-PaLM with prompting strategies including few-shot prompting, chain-of-thought, and self-consistency. They introduce instruction prompt tuning to create Med-PaLM.

### ML or AI Method Index
The core methods are large language models, instruction tuning, and prompting strategies.

### Model Inputs and Representations
Free-text medical questions and generated answers.

### Baselines or Comparators
Prior state of the art, PaLM, Flan-PaLM, Med-PaLM, and clinician-generated answers in human evaluation.

### Evaluation
Automated benchmark accuracy plus human evaluation across factuality, scientific consensus, harm, bias, precision, and helpfulness axes.

### Main Findings
Flan-PaLM achieved 67.6% accuracy on MedQA, more than 17 percentage points above prior state of the art. Med-PaLM improved long-form answer ratings: 92.6% of Med-PaLM answers aligned with scientific consensus versus 61.9% for Flan-PaLM and 92.9% for clinician answers; potential harm ratings were 5.8% for Med-PaLM versus 29.7% for Flan-PaLM and 6.5% for clinicians.

### Author-Stated Limitations
The authors emphasize remaining limitations in safety, fairness, bias, grounding, and clinical readiness.

### Funding, Conflicts, and Ethics
The work is from Google Research and DeepMind authors.

### Notes on Missing or Ambiguous Information
This is not an EHR prediction paper. It is relevant to LLM evaluation and clinical-language reasoning.
