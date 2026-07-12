---
citation_key: wei2025_mci_adrd_phenotyping_ehr
summary_status: complete
source_status: full_text
paper_type: journal_article
publication_status: peer_reviewed_version_of_record
ml_ai_methods:
  uses_ml_ai: true
  method_families:
    - logistic_regression
    - random_forest
    - neural_network
    - concept_extraction
    - other
  specific_methods:
    - LASSO
    - TF-IDF
    - Random Forest
    - Naive Bayes
    - Multilayer Perceptron
  learning_setup:
    - supervised_learning
  input_modalities:
    - clinical_notes
    - diagnosis_codes
    - medications
    - structured_ehr
  input_representation:
    - fixed_length_vector
    - bag_of_words_or_terms
    - engineered_features
    - concept_features
  prediction_task:
    - binary_classification
    - phenotyping
  temporal_handling:
    - site_split
    - cross_validation
  interpretability:
    - feature_importance
    - lasso_feature_selection
created: 2026-07-12
updated: 2026-07-12
---

# wei2025_mci_adrd_phenotyping_ehr

## Bibliographic Record

Wei, Ruoqi et al. "Automated phenotyping of mild cognitive impairment and Alzheimer's disease and related dementias using electronic health records." *International Journal of Medical Informatics* 200 (2025): 105917. DOI: `10.1016/j.ijmedinf.2025.105917`.

## Publication and Source Status

This summary is based on the full-text PDF saved as `papers/wei2025_mci_adrd_phenotyping_ehr.pdf`. The article is a peer-reviewed journal article, received August 7, 2024, revised January 31, 2025, accepted April 7, 2025, and available online April 11, 2025.

## Plain-Language Summary

The paper develops an automated EHR phenotyping model to identify patients with MCI or ADRD using chart-review labels. The model combines structured features, including diagnosis codes and dementia-related medications, with text features from clinical notes. Notes-only and combined note-plus-structured models performed much better than ICD-only or medication-only models. The best reported model achieved high discrimination in held-out tests, but the training sample was enriched for likely positive cases and uncertain chart reviews were excluded.

## Structured Summary

### Research Question

Can a machine-learning EHR phenotyping model accurately identify patients with MCI or ADRD by combining clinical notes, ICD codes, and dementia-related medications?

### Study Type

Retrospective supervised EHR phenotyping model study with manual chart-review reference labels.

### Data Source

Data came from Massachusetts General Hospital and Beth Israel Deaconess Medical Center. The paper states that outpatient visits were analyzed, with visits occurring between February 2015 and June 2022 in the abstract; the methods section also states that visits were collected between January 3, 2012 and November 3, 2017. This discrepancy should be source-checked before manuscript use.

### Population

Eligible patients were aged 50 years or older and had at least one clinical note. Patients were sampled using a stratified strategy based on medication and ICD-code evidence for MCI/ADRD to ensure adequate representation of low-, medium-, and high-likelihood patients. The final cohort included 3,626 patients and 5,612 visits after excluding 112 uncertain manual annotations.

The final cohort had mean age 67.6 years, 53% female, 70.5% White, 16.0% Black or African American, 1.5% Asian, and 11.94% other race category. Manual review identified 1,106 patients, or 30.5%, as MCI/ADRD positive.

### Index Date or Time Origin

The paper's unit is patient/visit phenotyping rather than prospective risk prediction. For patients with medication or ICD evidence, only notes after the first medication or ICD record were selected for analysis. ICD assignment allowed one day before and after the visit to account for prior or delayed entry.

### Observation Window

Clinical notes included office visit notes, admission notes, progress notes, discharge notes, and correspondence from all specialties in the MGH and BIDMC systems. Notes with fewer than 500 words were removed.

### Prediction Horizon or Follow-up

No future prediction horizon is defined. The model classifies whether the patient has an MCI/ADRD diagnosis according to manual chart review.

### Inputs or Predictors

Predictors include:

- clinical-note text features, including unigrams, bigrams, and trigrams weighted by TF-IDF;
- six ICD code categories for MCI/ADRD;
- nine predefined dementia-related medication groups.

ICD groupings were defined a priori by three neurologists and include Alzheimer's disease, vascular dementia, Lewy body dementia, frontotemporal dementia, unspecified dementias, and mild cognitive impairment. Medications include Aricept, donepezil, Exelon, rivastigmine, memantine, Namenda, Namzaric, Razadyne, and galantamine.

### Outcome or Target

The primary outcome was confirmed MCI or ADRD diagnosis determined by manual chart review. A neurologist manually reviewed notes in each medication/ICD stratum and assigned final yes/no MCI/ADRD labels. Cases marked uncertain were excluded.

### Methods

The authors trained logistic regression, random forest, Naive Bayes, and multilayer perceptron classifiers. Logistic regression used L1 regularization for feature selection. The authors compared input combinations: clinical notes plus ICDs plus medications, clinical notes only, ICDs only, and medications only. They used class weights inversely proportional to subsample size, grid-search hyperparameter tuning, and five-fold stratified nested cross-validation.

### ML or AI Method Index

The main model is regularized logistic regression over TF-IDF note features plus structured ICD and medication indicators. Alternative classifiers are random forest, Naive Bayes, and multilayer perceptron.

### Model Inputs and Representations

Text is represented as TF-IDF vectors over lowercased, lemmatized unigrams, bigrams, and trigrams after removing stop words and special characters. Structured data are represented through predefined ICD and medication groups. Features are assembled into a fixed-length vector for classification.

### Baselines or Comparators

Comparators include ICD-only, medication-only, note-only, and combined ICD-plus-medication-plus-note models. The paper also compares logistic regression, random forest, Naive Bayes, and multilayer perceptron classifiers. Site generalizability experiments train and test across MGH and BIDMC combinations.

### Evaluation

Metrics include accuracy, precision, recall, specificity, F1 score, AUROC, and AUPRC, with 95% confidence intervals from 1,000 bootstrap iterations. Generalizability experiments include MGH-to-BIDMC, BIDMC-to-MGH, combined training/testing, combined training to MGH, and combined training to BIDMC. The authors estimate expected performance in a random EHR sample using error rates within medication/ICD strata and stratum prevalence from 1,000 randomly sampled patients.

### Main Findings

For logistic regression in MGH+BIDMC train/test settings:

- ICD-only model: AUROC 0.54, AUPRC 0.69, accuracy 0.54.
- Medication-only model: AUROC 0.56, AUPRC 0.70, accuracy 0.56.
- Note-only model: AUROC 0.94, AUPRC 0.94, accuracy 0.88.
- ICD+medication+note model: AUROC 0.97, AUPRC 0.97, accuracy 0.91.

Across site experiments with all features, the highest reported performance was MGH+BIDMC training tested on MGH: AUROC 0.98, AUPRC 0.98, accuracy 0.93, specificity 0.96, recall 0.91, precision 0.96, and F1 0.93. Testing on BIDMC was lower but still high; for MGH+BIDMC training tested on BIDMC, AUROC was 0.92 and AUPRC 0.91.

Feature importance analysis identified terms and medications including "dementia," donepezil, Aricept, rivastigmine, memantine, "cognitive impairment," "Alzheimer," "MCI," "memory," "cognitive," and "decline." Error analysis found false positives often involved cognitive-like symptoms from alternative causes such as depression, anxiety, hypothyroidism, substance use, or sleep problems. False negatives often involved specialists outside cognitive care who sparsely mentioned MCI/ADRD.

### Author-Stated Limitations

The authors state that MGH and BIDMC are both in Boston and may not represent other U.S. or non-U.S. populations. They note that the model does not identify ADRD subtypes or MCI/ADRD severity. Excluding uncertain manual annotations may bias the model toward clearer cases and limit applicability to ambiguous real-world cases. They also state that LLMs such as GPT could improve feature extraction and interpretation, but were not used. Differences between MGH and BIDMC performance suggest possible institutional documentation pattern effects and the need for more generalizability testing.

### Funding, Conflicts, and Ethics

Funding came from NIH grants `R01NS102190`, `R01NS102574`, `R01NS107291`, `RF1AG064312`, `RF1NS120947`, `R01AG073410`, `R01HL161253`, `R01NS126282`, `R01AG073598`, and NSF grant `2014431`. EHR data extraction was approved by MGH and BIDMC Institutional Review Boards with waivers of informed consent; protocol numbers were `2013P001024`, `2023P000487`, and `2022P000417`. The authors declared no known competing financial interests or personal relationships.

Data and code are reported as available at `https://github.com/rockey1006/Automated_ADRD-MCI` and `https://bdsp.io/projects/jpCoV5N1MsB9a5QsgprQ/`.

### Notes on Missing or Ambiguous Information

- The abstract and methods section report different visit date ranges; this should be source-checked.
- The chart review appears to have been performed by one neurologist; inter-rater reliability is not reported.
- The model is a phenotyping/case-finding model, not future risk prediction.
- Sampling enriched likely MCI/ADRD positives; the authors estimate random-population accuracy separately, but PPV/NPV in routine deployment require careful interpretation.
