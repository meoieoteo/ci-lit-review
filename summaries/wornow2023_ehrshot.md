---
citation_key: wornow2023_ehrshot
title: "EHRSHOT: An EHR Benchmark for Few-Shot Evaluation of Foundation Models"
summary_status: complete
source_status: full_text_pdf
publication_status: preprint
paper_type: benchmark
---

# Summary: wornow2023_ehrshot

## Publication and Source Status

This is an arXiv/preprint benchmark paper submitted to the NeurIPS 2023 Datasets and Benchmarks track. The downloaded source is a full-text PDF. It should receive lower publication weight than peer-reviewed clinical validation studies.

## Purpose

EHRSHOT aims to improve reproducibility in EHR machine learning by releasing a longitudinal structured-EHR benchmark, task labels, code, and a pretrained structured-EHR foundation model.

## Data

EHRSHOT contains de-identified structured EHR data from 6,739 Stanford Medicine patients. Records include demographics, diagnoses, procedures, laboratory results, medications, and other structured events. The benchmark includes 41.6 million clinical events across 921,499 encounters.

The source database contains 3.67 million patients. The CLMBR-T-base model is pretrained on the structured EHR data of 2.57 million patients. EHRSHOT excludes clinical notes and images from the released benchmark.

## Tasks

The paper defines 15 classification tasks grouped into four categories:

1. Operational outcomes.
2. Anticipating lab test values.
3. Assignment of new diagnoses.
4. Anticipating chest X-ray findings.

The tasks include nine binary classification tasks, five five-way multiclass lab tasks, and one 14-way multilabel chest X-ray findings task. The authors provide canonical train/validation/test splits and few-shot samples.

## Models

The main comparison is between a count-based LightGBM model and CLMBR-T-base, a 141M-parameter autoregressive transformer model for structured medical-code sequences. CLMBR-T-base predicts the next medical code from prior codes, uses causally masked local attention, and does not process clinical text.

## Evaluation

The benchmark evaluates few-shot performance at k values from 1 to 128 positive and negative examples, plus full training data. Metrics include AUROC and AUPRC. For CLMBR-T-base, the pretrained model is frozen and a logistic-regression head is fine-tuned for each task.

## Results

CLMBR-T-base outperforms count-based GBM across all aggregated task categories for k <= 64. The advantage is most pronounced at intermediate k values and shrinks as more labeled data become available. Count-based GBM exceeds CLMBR-T-base on assignment-of-new-diagnosis tasks at k > 64, suggesting that pretraining is most useful in data-poor settings and not universally superior.

## Limitations

The benchmark releases only structured data, not clinical text or images. It evaluates one foundation model, uses a small selected cohort from the source database, and is limited to Stanford Medicine. The authors state that external performance at other institutions is unknown. Some tasks have very few positive cases, producing uncertain estimates.

## Relevance to Review

EHRSHOT is indirectly relevant to the dementia/cardiology problem. It supports discussion of few-shot evaluation, longitudinal structured-EHR modeling, benchmark design, and the need to compare foundation models against strong count-based baselines. It does not provide dementia-specific or note-based evidence.
