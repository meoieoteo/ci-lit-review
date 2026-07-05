---
citation_key: khan2026_next_generation_efi
summary_status: complete
source_status: full_text
paper_type: preprint
ml_ai_methods:
  uses_ml_ai: true
  method_families:
    - neural_network
    - concept_extraction
    - survival_model
    - other
  specific_methods:
    - NLP-NER
    - Cox proportional hazards
    - Harrell C-index
    - generalized additive mixed models
  learning_setup:
    - supervised_learning
    - statistical_association
  input_modalities:
    - structured_ehr
    - clinical_notes
    - diagnosis_codes
    - labs
    - medications
    - procedures
  prediction_task:
    - risk_prediction
    - survival_time_to_event
    - phenotyping
  temporal_handling:
    - longitudinal_history
    - time_to_event
    - fixed_observation_window
  interpretability:
    - concept_features
    - calibration
created: 2026-07-05
updated: 2026-07-05
---

# khan2026_next_generation_efi

## Bibliographic Record
Khan, Esha, Silvia Ottaviani, Juho Kaijansinkko, Markus J. Haapanen, Anna Tirkkonen, Jonathan K. L. Mak, Hanna Pajulammi, Mikaela B. von Bonsdorff, Jake Lin, and Juulia Jylhava. "A next-generation electronic frailty index leveraging deep learning on unstructured health records extends risk prediction across the full frailty spectrum." medRxiv, 2026. https://doi.org/10.64898/2026.06.23.26356323.

## Plain-Language Summary
This preprint builds an electronic frailty index that combines structured EHR data with information extracted from free-text clinical notes. Using a large Finnish EHR dataset across primary, secondary, tertiary, long-term, and home-care services, the authors construct a 53-item eFI and show that it is associated with mortality, severe infections, fractures, and healthcare utilization. The study argues that unstructured notes can improve frailty measurement by capturing functional, sensory, cognitive, and psychosocial deficits that structured ICD-coded data may miss.

## Structured Summary

### Research Question
Can a multidimensional electronic frailty index built from structured and unstructured EHR data improve risk stratification across adulthood and across the frailty spectrum?

### Study Type
Population-based retrospective EHR study. The source is a medRxiv preprint and had not been peer reviewed at the time of the local PDF.

### Data Source
Longitudinal EHR data from the Wellbeing Services County of Central Finland from January 1, 2010 through December 31, 2023. Data included diagnoses, labs, procedures, prescribed medications, and free-text notes from multiple care settings.

### Population
193,629 individuals aged 35-103 after exclusions, drawn from public healthcare records in Central Finland. The original dataset included all inpatient and outpatient EHRs from public primary, secondary, tertiary, long-term, and home-care services.

### Index Date or Time Origin
Entry year was the first calendar year in which a person appeared in the data. Baseline eFI was used for outcome models.

### Observation Window
Annual eFI values were calculated across available calendar years. Baseline eFI was used for outcome analyses, with longitudinal trajectories modeled over age.

### Prediction Horizon or Follow-up
All-cause mortality follow-up continued until death or last available EHR. Severe infections and fractures were assessed within two years after baseline eFI. Healthcare utilization was assessed during the first year after baseline eFI.

### Inputs or Predictors
The eFI included 53 binary deficit items: 34 ICD-10-coded diagnoses, 9 laboratory-test items, and 10 free-text-derived deficits. Free-text deficits included falls, incontinence, loneliness, mobility limitations, hearing and visual impairment, age-related neurocognitive problems, and assistance needs with bathing, dressing, eating, or meal preparation.

### Outcome or Target
Outcomes were all-cause mortality, severe infections requiring hospital treatment, fractures, and healthcare utilization.

### Methods
The authors constructed a deficit-accumulation eFI with equally weighted binary items. Free-text deficits were identified using deep-learning AI-driven NLP-NER models. Frailty trajectories were modeled with generalized additive mixed models. Associations with mortality, severe infections, and fractures used Cox proportional hazards models. Count/utilization models are described in supplementary methods. Predictive discrimination was assessed using Harrell's C-index and compared against HFRS and CCI.

### ML or AI Method Index
The AI component is concept extraction from clinical notes using deep-learning NLP-NER. The risk models themselves are statistical survival/count models using the constructed eFI as a predictor.

### Model Inputs and Representations
The eFI is a concept-feature representation of frailty. It combines structured diagnosis/lab items and note-derived deficits. This is more interpretable than a black-box note embedding because each extracted item corresponds to a deficit category.

### Baselines or Comparators
The authors compare eFI performance with Hospital Frailty Risk Score and Charlson Comorbidity Index, each added to base models containing age and sex.

### Evaluation
The NLP-NER models had F1 scores from 0.74 to 0.92 across free-text deficit items. Cox model generalizability was assessed with a 70/30 train-test split and C-index in the held-out test set. The eFI improved discrimination over HFRS and CCI across time-to-event outcomes and improved model fit in count models.

### Main Findings
Frailty accelerated after age 65. Severe frailty was associated with higher risk of mortality, severe infections, fractures, and healthcare utilization compared with non-frail status. Associations persisted even among individuals classified as non-frail. The eFI showed stronger discrimination than HFRS and CCI across outcomes.

### Author-Stated Limitations
The authors note incomplete data capture inherent to EHR research, absence of direct lifestyle and socioeconomic measures because of collection and privacy limitations, and observational design that precludes causal inference.

### Funding, Conflicts, and Ethics
Funding came from the Research Council of Finland, Instrumentarium Science Foundation, Sigrid Juselius Foundation, and Samfundet Folkhalsan. Ethics review and consent were not required under Finnish secondary-use legislation; the relevant ethics committee certified that review was not required.

### Notes on Missing or Ambiguous Information
This is a preprint and should be treated as not yet peer reviewed. Supplementary methods contain additional details on NLP-NER models and count-model analyses that should be extracted before using this as a methods template.
