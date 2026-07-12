---
citation_key: li2024_dementia_risk_notes
summary_status: complete
source_status: full_text
paper_type: journal_article
publication_status: peer_reviewed_version_of_record
ml_ai_methods:
  uses_ml_ai: true
  method_families:
    - transformer
    - neural_network
    - embedding_model
    - other
  specific_methods:
    - Longformer
    - Sentence-BERT
    - pPSO
    - LED_BookSum
    - LED_PubMed
    - AdamW
  learning_setup:
    - supervised_learning
    - unsupervised_learning
  input_modalities:
    - clinical_notes
  input_representation:
    - raw_text
    - document_chunks
    - sequence_tokens
    - dense_embeddings
  prediction_task:
    - binary_classification
    - risk_prediction
  temporal_handling:
    - observation_window
    - prediction_horizon
    - chronological_concatenation
  interpretability:
    - sentence_selection
    - decision_focused_summaries
created: 2026-07-12
updated: 2026-07-12
---

# li2024_dementia_risk_notes

## Bibliographic Record

Li, Shengyang; Dexter, Paul; Ben-Miled, Zina; Boustani, Malaz. "Dementia risk prediction using decision-focused content selection from medical notes." *Computers in Biology and Medicine* 182 (2024): 109144. DOI: `10.1016/j.compbiomed.2024.109144`.

## Publication and Source Status

This summary is based on the full-text PDF saved as `papers/li2024_dementia_risk_notes.pdf`. The PDF is the final Elsevier version of record, received January 28, 2024, revised August 19, 2024, accepted September 8, 2024, and available online September 18, 2024. A PubMed Central HTML version also exists locally, but it is an NIH author manuscript; the PDF is the source used for this redo.

## Plain-Language Summary

The paper develops a dementia risk prediction model that uses only medical notes from routine EHR data. Because a patient's longitudinal notes can exceed transformer input limits, the authors propose a decision-focused content selection method that chooses sentences likely to help classify future dementia risk. The selected sentences are fed into a Longformer classifier. In internal three-fold cross-validation on a balanced retrospective case-control dataset, this method outperformed truncation, particle-swarm sentence selection, and generic LED summarization baselines.

## Structured Summary

### Research Question

Can a transformer-based dementia risk prediction model use decision-focused sentence selection to predict future dementia from longitudinal medical notes while avoiding arbitrary truncation or generic summarization?

### Study Type

Non-interventional retrospective EHR prediction model study.

### Data Source

The study used data from the Indiana Network for Patient Care through the Regenstrief Data Core. INPC is described as a centralized community-wide electronic medical record collecting data from 19 hospitals in seven health systems, the Marion County Health Department, regional laboratories, radiology centers, and physician practices.

The EHR source includes demographics, laboratory results, emergency department, inpatient and outpatient encounter data, free-text chief complaints, coded diagnoses and procedures, vital signs, and other clinical data. This paper uses medical notes represented as text.

### Population

The initial cohort contained 26,236 patients: 4,796 incident dementia cases and 21,440 controls. Controls were randomly downsampled to 4,796 to avoid class imbalance, producing 9,592 patients equally split between cases and controls.

Table 2 reports mean age 74.43 years for cases and 72.80 years for controls; 63% of cases and 64% of controls were female; 67% of cases and 70% of controls were White.

### Index Date or Time Origin

For cases, controls were matched within five years of the disease index date of the matching case. The paper does not provide a detailed operational definition of the disease index date beyond this description.

### Observation Window

The paper evaluates one-year and two-year observation periods. All medical notes within the observation period are collected into a single patient document ordered chronologically from oldest to newest.

### Prediction Horizon or Follow-up

The paper evaluates prediction horizons of 0.5 years, meaning six months, and one year.

### Inputs or Predictors

The model uses medical notes only. Notes are combined chronologically, cleaned by replacing numerals with spaces and removing text formatting tags and report titles, split into sentences using the NLTK sentence tokenizer, and deduplicated.

### Outcome or Target

The outcome is binary incident dementia case status versus matched control status. Cases are patients with incident dementia. Patients with mild cognitive impairment or previous dementia are excluded from the case cohort. Controls have no dementia or MCI diagnosis and are matched to cases by sex, race, and age within five years of the case disease index date.

### Methods

The paper proposes a decision-focused content selection meta-algorithm. During training, the method iteratively selects nonredundant sentences from each patient's note document, trains a Longformer classifier, updates sentence relevance based on whether the classifier predicts the disease outcome correctly, and recalculates sentence-selection thresholds. The method uses an exploration/exploitation scheme inspired by multi-armed bandits and a simulated-annealing update for thresholds.

For inference on held-out patients, the true outcome is unavailable, so the authors use an unsupervised sentence-selection process. Sentence-BERT embeddings and pPSO are used to build representative centroids from training-set case and control sentences selected by the supervised process; new-patient summaries are built by selecting nonredundant sentences similar to these centroids.

### ML or AI Method Index

The main classifier is Longformer with a classification head. Sentence-BERT is used to compute sentence embeddings and cosine similarities. pPSO is used for centroid selection. LED_BookSum and LED_PubMed summarization models are used as baselines. Classifiers are trained with AdamW on Nvidia A100 GPUs, half precision, five epochs, batch size four, and linear warmup.

### Model Inputs and Representations

Each patient's longitudinal notes are represented as a chronologically ordered text document. The proposed method turns that document into a selected sentence sequence constrained by token limit. The classifier consumes token sequences rather than fixed tabular features.

The authors report that for a one-year observation period, average patient documents exceeded 5,000 tokens and 200 sentences, and nearly 40% exceeded the 4,096-token Longformer input limit.

### Baselines or Comparators

The content-selection comparators are:

- late truncation;
- early truncation;
- random truncation;
- pPSO sentence sampling;
- LED_BookSum summarization;
- LED_PubMed summarization.

All compared content-selection methods feed into the same Longformer classification architecture.

### Evaluation

The paper reports three-fold cross-validation. Metrics include AUC, precision, sensitivity, specificity, F1 score, and accuracy. Results are reported for summary lengths of 1,024 and 4,096 tokens, one- and two-year observation periods, and six-month and one-year prediction horizons.

### Main Findings

For one-year observation and one-year prediction horizon, the proposed method achieved:

- 1,024-token limit: AUC 78.43, precision 73.78, sensitivity 70.64, specificity 70.64, F1 70.21, accuracy 70.64.
- 4,096-token limit: AUC 77.15, precision 72.38, sensitivity 69.89, specificity 69.89, F1 69.57, accuracy 69.89.

For the proposed method across alternate timing settings:

- one-year observation, six-month horizon, 1,024 tokens: AUC 80.63;
- two-year observation, six-month horizon, 1,024 tokens: AUC 81.26;
- two-year observation, one-year horizon, 1,024 tokens: AUC 79.90;
- one-year observation, six-month horizon, 4,096 tokens: AUC 80.34;
- two-year observation, six-month horizon, 4,096 tokens: AUC 81.64;
- two-year observation, one-year horizon, 4,096 tokens: AUC 80.07.

The authors report that shorter prediction horizons and longer observation periods improved performance. They also report that the proposed content-selection method outperformed truncation, pPSO, and LED summarization baselines for the one-year observation and one-year horizon setting.

### Author-Stated Limitations

The authors state that the static summary length used in the study, 1,024 or 4,096 tokens, may not be optimal for all patients or observation periods. They suggest that a patient- and observation-period-specific dynamic limit may be more suitable. They also state that future work includes fusing medical notes with other EHR modalities and environmental data.

### Funding, Conflicts, and Ethics

The study was approved by the Indiana University Review Board, IRB number `2008372812`.

The authors state that the research was supported by the National Institute on Aging, USA, award `076071-00010C`. High-performance computing services were supported in part by Lilly Endowment support for the Indiana University Pervasive Technology Institute.

The data are available from the Regenstrief Institute with restrictions and permission; the code for model training and inferencing is reported as available under the PDMlaboratory.

Conflict disclosures: Dr. Ben-Miled has a financial interest in DigiCare Realized. Dr. Boustani serves as Chief Scientific Officer and co-founder of Blue Agilis and Chief Health Officer of DigiCare Realized, has equity interests in Blue Agilis and DigiCare Realized, sold equity in Preferred Population Health Management and MyShift/RestUp, and serves as an advisory board member for Eli Lilly, Eisai, Merck, Biogen, and Genentech. The paper states these conflicts were reviewed and managed by Indiana University. The remaining authors declared no competing interests.

### Notes on Missing or Ambiguous Information

- The paper does not provide a detailed code list or diagnostic algorithm for incident dementia, MCI exclusion, previous dementia exclusion, or control definition in the main text.
- The paper does not report chart-adjudicated dementia labels, cognitive test validation, external validation, calibration, decision-curve analysis, subgroup performance, or real-world PPV under natural dementia prevalence.
- The case-control downsampling creates a 50% case fraction, so precision and accuracy are not prevalence-calibrated for routine clinical deployment.
- The paper does not specify note types in enough detail to determine which notes would be available before a cardiology encounter in a local Epic implementation.
