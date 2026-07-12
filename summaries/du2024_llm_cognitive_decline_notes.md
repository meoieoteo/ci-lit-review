---
citation_key: du2024_llm_cognitive_decline_notes
title: "Enhancing early detection of cognitive decline in the elderly: a comparative study utilizing large language models in clinical notes"
summary_status: complete
source_status: full_text_html
publication_status: peer_reviewed
paper_type: comparative_nlp_model_study
---

# Summary: du2024_llm_cognitive_decline_notes

## Publication and Source Status

This is a 2024 peer-reviewed open-access article with full-text HTML downloaded from PubMed Central. The article notes a prior medRxiv version.

## Research Question

The study evaluates whether large language models can detect cognitive decline in real EHR clinical notes and how their error profiles compare with locally trained models.

## Data and Cohort

The study was conducted at Mass General Brigham using the same annotated note-section datasets as a prior cognitive-decline NLP study. Notes came from the four years before a 2019 MCI diagnosis among patients aged 50 or older.

The development dataset included 4,949 keyword-filtered note sections from 1,969 patients. The test dataset included 1,996 randomly sampled note sections from 1,161 patients without keyword filtering.

## Label Definition

Cognitive decline was defined as evidence of subjective cognitive decline, MCI, or dementia, including concerns, symptoms, diagnoses, cognitive assessments, or cognitive-related therapies. Transient, reversible, improved, or uncertain cognitive findings were labeled negative. Annotation involved trained annotators and subject matter experts, with Fleiss kappa 0.83 reported for an agreement set.

## Methods

The authors evaluated GPT-4 through Azure OpenAI Service and Llama 2 13B through Amazon EC2 in HIPAA-compliant environments. Prompt strategies included hard prompting, retrieval augmented generation, few-shot examples, and error-analysis-based instructions. Baselines included a hierarchical attention-based neural network and XGBoost. The authors also built a majority-vote ensemble of GPT-4, the attention-based DNN, and XGBoost.

## Results

GPT-4 outperformed Llama 2 and was more efficient, but did not outperform the locally trained traditional models. Error-analysis-based prompting was the strongest GPT-4 strategy. The ensemble model significantly outperformed individual models, achieving precision 90.2%, recall 94.2%, and F1 92.1%. Error analysis found 63 samples incorrectly predicted by at least one model, but only two were errors shared by all models, suggesting complementary error profiles.

## Limitations

The study uses a single health system and the same selected MCI-linked datasets as Wang 2021. It does not establish external generalizability, general-population risk prediction, or clinical utility. The specific LLM results may age quickly as model versions change. The ensemble was evaluated on a limited testing set and needs larger testing with patients outside the original dataset.

## Relevance to Review

This is direct evidence for LLM-based cognitive-decline note classification. It supports a nuanced modeling conclusion: general-domain LLMs may add complementary information and interpretability, but local task-trained models can outperform them, and ensembles may be more useful than standalone LLM deployment.
