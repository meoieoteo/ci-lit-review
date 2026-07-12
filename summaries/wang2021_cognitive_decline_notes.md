---
citation_key: wang2021_cognitive_decline_notes
title: "Automated Detection of Cognitive Impairment in Electronic Health Records"
summary_status: complete
source_status: full_text_html
publication_status: peer_reviewed
paper_type: diagnostic_model_study
---

# Summary: wang2021_cognitive_decline_notes

## Publication and Source Status

This is a peer-reviewed JAMA Network Open diagnostic study published in 2021. The downloaded source is full-text HTML from PubMed Central.

## Research Question

The study asks whether a deep learning algorithm applied to clinical notes can detect evidence of cognitive decline before a documented mild cognitive impairment diagnosis.

## Data and Cohort

The authors used Mass General Brigham EHR data. They identified patients aged 50 years or older with an initial ICD-10 MCI diagnosis in 2019 and extracted clinical notes from the four years preceding that diagnosis. The unique population across labeled datasets was 2,166 patients.

Two manually labeled section-level reference datasets were created. Dataset I included 4,950 note sections filtered by cognitive keywords and represented 1,969 patients. Dataset II included 2,000 randomly selected note sections without keyword filtering and represented 1,161 patients.

## Label Definition

Cognitive decline was defined broadly, spanning subjective cognitive decline, MCI, and dementia. Positive evidence could include cognitive concern, symptoms such as memory loss, diagnoses, cognitive assessments, or cognitive-related therapy. Transient, reversible, improved, or uncertain cognitive findings were labeled negative.

Three annotators were trained with subject matter experts. Initial conflicts were resolved with experts, and a second 50-section agreement set achieved Fleiss kappa 0.83. Uncertain cases in the larger labeling set were resolved by subject matter experts.

## Methods

Clinical notes were segmented into sections using the Medical Text Extraction, Reasoning and Mapping System. The main model was a hierarchical attention-based deep learning model using convolutional, recurrent, and attention layers with word2vec embeddings trained on 3,729,838 notes from 10,837 patients with MCI diagnoses.

The authors compared the deep learning model with logistic regression, random forest, support vector machine, and XGBoost baselines using TF-IDF unigram features. Models were evaluated with AUROC and AUPRC. Confidence intervals were estimated with bootstrap resampling.

## Results

Dataset I had 1,453 positive sections (29.4%). Dataset II had 69 positive sections (3.45%). The deep learning model performed best in both datasets. In dataset I, it achieved AUROC 0.971 and AUPRC 0.933. In dataset II, it achieved AUROC 0.997 and AUPRC 0.929. With a 0.5 cutoff, PPV was 0.848 and sensitivity 0.925 in dataset I, and PPV was 0.771 and sensitivity 0.928 in dataset II.

The best conventional baseline was XGBoost, with AUROC/AUPRC 0.953/0.882 in dataset I and 0.988/0.898 in dataset II. The authors report that keyword search had low PPV despite identifying all positive cases in dataset II.

## Limitations

The study is single-system and externally unvalidated. The cohort is selected on later MCI diagnosis, so the model detects textual evidence before a recorded MCI code among already-identified MCI patients rather than predicting incident cognitive decline in an unselected population. MCI diagnoses in EHR data may be heterogeneous and may not always reflect AD-related early disease. The model may need retraining for other documentation environments.

## Relevance to Review

This is strong direct evidence that clinical notes can contain cognitive-decline evidence before structured MCI diagnosis and that note-section classifiers can outperform keyword search and TF-IDF baselines. It is highly relevant to note-based phenotyping and early detection. It should not be overinterpreted as an externally validated pre-cardiology risk model.
