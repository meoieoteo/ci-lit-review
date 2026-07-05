---
citation_key: osman2024_nlp_ageing_syndromes
summary_status: complete
source_status: full_text
paper_type: journal_article
ml_ai_methods:
  uses_ml_ai: true
  method_families:
    - rule_based_nlp
    - concept_extraction
    - neural_network
    - other
  specific_methods:
    - QUADAS-2
    - PRISMA
    - SWiM
  learning_setup:
    - supervised_learning
    - not_applicable
  input_modalities:
    - clinical_notes
    - structured_ehr
  prediction_task:
    - phenotyping
    - binary_classification
  temporal_handling:
    - cross_sectional
    - not_reported
  interpretability:
    - rules
    - concept_features
    - none_reported
created: 2026-07-05
updated: 2026-07-05
---

# osman2024_nlp_ageing_syndromes

## Bibliographic Record
Osman, Mo, Rachel Cooper, Avan A. Sayer, and Miles D. Witham. "The use of natural language processing for the identification of ageing syndromes including sarcopenia, frailty and falls in electronic healthcare records: a systematic review." Age and Ageing 53, no. 7 (2024). https://doi.org/10.1093/ageing/afae135.

## Plain-Language Summary
This systematic review evaluates whether NLP can identify ageing syndromes in EHR text. It finds that NLP has been used to identify falls, dementia, delirium, incontinence, frailty, and sarcopenia, and that reported diagnostic accuracy is often acceptable. However, the evidence base is uneven: only 22 studies were included, external validation was uncommon, quality varied, and many studies did not report enough diagnostic accuracy detail. The paper is useful as a cross-condition review of clinical-note phenotyping for geriatric syndromes.

## Structured Summary

### Research Question
What evidence exists on the feasibility and diagnostic accuracy of NLP algorithms for identifying ageing syndromes in EHRs?

### Study Type
Systematic review following PRISMA, registered in PROSPERO.

### Data Source
Searches covered PubMed, Embase, CINAHL, ACM Digital Library, IEEE Xplore, and Scopus from database inception through September 2023.

### Population
Included studies used adult EHR data from multiple care settings. Ageing syndromes of interest were sarcopenia, frailty, falls, delirium, dementia, incontinence, and multimorbidity/multiple long-term conditions.

### Index Date or Time Origin
Not standardized across included studies. Most included papers were diagnostic or phenotyping studies rather than future-risk prediction studies.

### Observation Window
Varied by included study and was often tied to clinical-note datasets or sampled records.

### Prediction Horizon or Follow-up
The review excluded studies using NLP to predict future onset of conditions or complications. The focus was identification of existing ageing syndromes.

### Inputs or Predictors
Clinical text from EHRs, including outpatient notes, discharge summaries, inpatient notes, emergency department notes, ambulance records, homecare notes, and other note types depending on the study.

### Outcome or Target
Identification of ageing syndromes in EHR text. Included targets were falls, dementia, delirium, incontinence, sarcopenia/frailty, and related geriatric conditions.

### Methods
Two reviewers screened studies. Data extraction captured computational method, text source, validation method, and performance metrics. QUADAS-2 was used for quality assessment. Because of heterogeneity, synthesis was narrative and used SWiM principles rather than meta-analysis.

### ML or AI Method Index
The review covers rule-based NLP, machine-learning text classification, deep-learning text classification, and named entity recognition. It does not identify one clearly superior NLP method.

### Model Inputs and Representations
The included studies used varied text representations. Some used rules or dictionaries; others used machine-learning or deep-learning classifiers. Named entity recognition was used in some studies to identify terms or concepts in clinical text.

### Baselines or Comparators
Gold standards commonly included manual text review by clinical experts or trained annotators. Some studies used administrative codes or validated administrative algorithms.

### Evaluation
Twenty-two studies were included. Sensitivity ranged from 57.1% to 100%, specificity from 84.0% to 100%, PPV from 47.0% to 100%, and F1 score from 0.57 to 0.95. Only four studies included external validation.

### Main Findings
NLP identification of ageing syndromes in EHRs appears feasible. Falls, dementia, and delirium were more frequently studied than sarcopenia, frailty, or multimorbidity. Study quality and reporting were variable. Only 8 of 22 studies had low concern across all QUADAS-2 domains.

### Author-Stated Limitations
The authors state that the search may have missed studies, heterogeneity prevented meta-analysis and publication-bias testing, interpretation was constrained by lack of a standard NLP taxonomy, and some included studies may not generalize to older populations because the inclusion criterion was adult age over 18.

### Funding, Conflicts, and Ethics
The authors reported no conflicts of interest. M.O. was funded by an NIHR Newcastle Biomedical Research Centre informatics fellowship. The work was conducted as part of the ADMISSION collaborative.

### Notes on Missing or Ambiguous Information
The review is broad across ageing syndromes, so dementia-specific conclusions require caution. It highlights the need for external validation, robust ground truth, and STARD-consistent diagnostic accuracy reporting.
