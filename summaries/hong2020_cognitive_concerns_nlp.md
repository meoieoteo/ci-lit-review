---
citation_key: hong2020_cognitive_concerns_nlp
title: "NLP to Detect Cognitive Concerns in Electronic Health Records"
summary_status: complete
source_status: full_text_pdf
publication_status: workshop_abstract_preprint
paper_type: machine_learning_healthcare_short_paper
---

# Summary: hong2020_cognitive_concerns_nlp

## Publication and Source Status

This is a short Machine Learning for Health 2020 extended abstract with an arXiv version. The available source is a full-text PDF, but the publication format is brief and should receive lower evidentiary weight than a full peer-reviewed clinical prediction or validation study.

## Research Question

The paper asks whether NLP applied to clinician progress notes can identify patients with cognitive concerns in the EHR better than structured diagnosis-code and medication features alone.

## Data and Cohort

The study used a gold-standard dataset of 1,000 randomly sampled patients from Mass General Brigham HealthCare. Expert clinicians reviewed each patient's 2018 EHR record and labeled the presence or absence of cognitive concerns. After filtering for patients with progress notes, the final dataset included 767 patients split into 690 train/validation patients and 77 test patients. The test set had 34 patients with cognitive concern labels.

Input data included diagnosis history, cognitive-related medications, and progress notes from January 1, 2018 through December 31, 2018.

## Label Definition

The outcome was presence of cognitive concerns, described as signs of dementia. The paper states that neurologists, psychiatrists, or geriatric psychiatrists reviewed EHR records to assign labels. The positive class appears to include subjective concern, mild cognitive impairment, and dementia, but the short paper does not provide a detailed annotation rubric, adjudication procedure, or inter-rater reliability.

## Methods

The authors compared four models:

1. Regularized logistic regression using cognitive-related medications and ICD codes.
2. Regularized logistic regression using counts from 15 regular-expression categories.
3. Regularized logistic regression using TF-IDF features selected by correlation with the cognitive concern label.
4. A Longformer sequence-classification model fine-tuned on notes using sliding windows of 4,096 tokens and patient-level aggregation.

Model thresholds were selected to maximize accuracy. The structured baseline used L1-regularized logistic regression with 10-fold cross-validation.

## Results

On the 77-patient test set, the structured-code/medication baseline achieved AUC 0.79, sensitivity 0.59, and specificity 1.00. The regular-expression model improved AUC to 0.88, sensitivity to 0.76, and specificity to 0.91. The TF-IDF model achieved AUC 0.90, sensitivity 0.85, and specificity 0.86. The Longformer model had the highest AUC at 0.93, with accuracy 0.90, sensitivity 0.79, specificity 0.98, PPV 0.96, and NPV 0.86.

The paper notes that the structured baseline missed patients with subjective concern, MCI, and dementia who lacked relevant codes or medications. The authors also observe that the deep-learning model was only marginally better than term-based NLP models in this dataset.

## Limitations

The study is small, single-system, and reported in short-paper format. The test set is only 77 patients. The paper does not describe external validation, calibration, subgroup performance, temporal validation, clinical workflow evaluation, or detailed label reproducibility. The cognitive concern label is broad and includes stages with different clinical meaning.

## Relevance to Review

This is directly relevant evidence that unstructured progress notes can add sensitivity for detecting cognitive concerns that are not captured by structured EHR features alone. It is especially relevant to the review's modeling-strategy question because it compares structured-only features, simple NLP, and a transformer model for cognitive concerns.

Its evidentiary role should be limited: it supports plausibility and model-design motivation, not definitive claims about deployment-ready dementia detection.
