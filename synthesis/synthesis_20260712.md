# Synthesis: Up-to-Date Literature Snapshot

## Synthesis Status

synthesis_complete

## Synthesis Question

What is the current cross-paper snapshot of the literature reviewed so far, and what does it imply for a pre-cardiology-encounter cognitive-risk score using longitudinal EHR text?

## Included Papers and Review Status

All 56 papers currently listed in `literature_review_state.md` have `consolidated_review_available`.

Direct dementia, MCI, cognitive impairment, cognitive-note, or dementia-phenotyping evidence:

- `benmiled2023_dementia_notes` - `consolidated_review_available`
- `du2024_llm_cognitive_decline_notes` - `consolidated_review_available`
- `gilmorebykovskyi2018_ci_ehr_phenotype` - `consolidated_review_available`
- `hong2020_cognitive_concerns_nlp` - `consolidated_review_available`
- `john2022_dementia_prediction_validation` - `consolidated_review_available`
- `kashyap2025_explainable_dementia_types` - `consolidated_review_available`
- `li2024_dementia_risk_notes` - `consolidated_review_available`
- `li2025_multimodal_dementia` - `consolidated_review_available`
- `lu2026_ehr_dementia_prediction_review` - `consolidated_review_available`
- `mccoy2020_dementia_ehr` - `consolidated_review_available`
- `penfold2022_mci_nlp` - `consolidated_review_available`
- `shao2019_probable_dementia_ehr` - `consolidated_review_available`
- `tyagi2021_cognitive_impairment_ehr` - `consolidated_review_available`
- `wang2021_cognitive_decline_notes` - `consolidated_review_available`
- `wei2025_mci_adrd_phenotyping_ehr` - `consolidated_review_available`

Diagnostic opportunity, detection gap, outcome validity, and bias evidence:

- `bynum2024_regional_variation_diagnostic_intensity_dementia` - `consolidated_review_available`
- `liang2025_target_trial_emulation` - `consolidated_review_available`
- `liu2024_detection_rates_mci_primary_care` - `consolidated_review_available`
- `mattke2023_expected_diagnosed_mci_dementia_medicare` - `consolidated_review_available`
- `shen2025_integrating_misclassified_ehr_outcomes` - `consolidated_review_available`
- `spoto2025_diagnostic_signal_decay_dementia` - `consolidated_review_available`
- `tzeng2024_annual_wellness_visits_early_dementia_diagnosis` - `consolidated_review_available`

Geriatric, frailty, cardiology-note, ageing-syndrome, and clinical analogue evidence:

- `adejumo2024_hf_functional_status_nlp` - `consolidated_review_available`
- `khan2026_next_generation_efi` - `consolidated_review_available`
- `osman2024_nlp_ageing_syndromes` - `consolidated_review_available`
- `song2022_home_health_notes` - `consolidated_review_available`
- `zhou2025_preoperative_frailty_llm` - `consolidated_review_available`

Structured EHR, clinical language model, and multimodal modeling background:

- `alsentzer2019_clinical_bert_embeddings` - `consolidated_review_available`
- `choi2016_retain` - `consolidated_review_available`
- `garriga2023_mental_health_crises_notes` - `consolidated_review_available`
- `huang2019_clinicalbert_readmission` - `consolidated_review_available`
- `lee2019_biobert` - `consolidated_review_available`
- `li2020_behrt` - `consolidated_review_available`
- `lyu2022_multimodal_mortality_notes` - `consolidated_review_available`
- `rasmy2021_medbert` - `consolidated_review_available`
- `ruan2025_icu_multimodal_notes` - `consolidated_review_available`
- `singhal2022_medpalm` - `consolidated_review_available`
- `steinberg2021_ehr_language_models` - `consolidated_review_available`
- `wornow2023_ehrshot` - `consolidated_review_available`
- `wornow2023_shaky_foundations_ehr_fm` - `consolidated_review_available`
- `yang2022_gatortron` - `consolidated_review_available`

AD/MCI progression, neuroimaging, speech, and broader ML review context:

- `amini2024_speech_ad_progression` - `consolidated_review_available`
- `grammenos2024_explainable_mci_ad` - `consolidated_review_available`
- `grueso2021_mci_ad_ml_review` - `consolidated_review_available`
- `kumar2021_ad_progression_ml_review` - `consolidated_review_available`
- `pellegrini2018_neuroimaging_ml_review` - `consolidated_review_available`

Sequential diagnosis, feature acquisition, value of information, and future policy context:

- `aronsson2025_active_feature_acquisition` - `consolidated_review_available`
- `blumlein2022_causal_tree_dtr` - `consolidated_review_available`
- `heckerman1991_probabilistic_similarity_networks` - `consolidated_review_available`
- `horvitz1987_beliefs_actions_resources` - `consolidated_review_available`
- `janisch2020_costly_features` - `consolidated_review_available`
- `kaelbling1998_pomdp_survey` - `consolidated_review_available`
- `liu2018_deep_rl_dtr` - `consolidated_review_available`
- `poh1996_information_value` - `consolidated_review_available`
- `vivar2020_peri_diagnostic_feature_acquisition` - `consolidated_review_available`
- `yazzourh2025_medical_knowledge_rl_dtr` - `consolidated_review_available`

## Executive Takeaway

The literature now supports the project's basic premise: longitudinal EHR text contains dementia-, cognition-, function-, frailty-, and care-navigation-relevant signal that is often missing from structured fields. The strongest contribution is still not a novel model architecture. The strongest contribution is a defensible encounter-level study design for pre-cardiology cognitive-risk scoring: target definition, label construction, timing, downstream-action bias, diagnosis opportunity, validation, calibration, and reproducible EHR-to-model-ready transformation.

The newest ten reviewed papers strengthen two conclusions. First, clinical notes are directly useful in dementia or cognitive-impairment tasks (`penfold2022_mci_nlp`, `benmiled2023_dementia_notes`, `mccoy2020_dementia_ehr`, `li2025_multimodal_dementia`, `tyagi2021_cognitive_impairment_ehr`, `kashyap2025_explainable_dementia_types`). Second, non-dementia multimodal EHR-text papers are useful as methods analogies but should not be cited as dementia evidence (`garriga2023_mental_health_crises_notes`, `lyu2022_multimodal_mortality_notes`, `song2022_home_health_notes`, `ruan2025_icu_multimodal_notes`).

## Major Ideas

### 1. "Dementia Prediction" Is Not a Single Target

Reviewed papers repeatedly use similar words for different constructs: current cognitive impairment, current undocumented impairment, future cognitive decline, future coded dementia diagnosis, dementia subtype, referral/testing, or care pathway. `lu2026_ehr_dementia_prediction_review`, `john2022_dementia_prediction_validation`, `li2024_dementia_risk_notes`, `penfold2022_mci_nlp`, `mccoy2020_dementia_ehr`, and `kashyap2025_explainable_dementia_types` all reinforce that target choice changes interpretation.

For this project, the first model should remain scoped to a single decision point: immediately before cardiology encounter start.

### 2. EHR Text Signal Is Real, But It Comes in Different Forms

The direct cognitive/dementia papers support multiple text strategies:

- note-section or snippet classification: `wang2021_cognitive_decline_notes`, `du2024_llm_cognitive_decline_notes`, `tyagi2021_cognitive_impairment_ehr`
- note-derived concepts or UMLS features: `penfold2022_mci_nlp`, `benmiled2023_dementia_notes`, `kashyap2025_explainable_dementia_types`
- free-text risk modeling from longer medical notes: `li2024_dementia_risk_notes`, `li2025_multimodal_dementia`
- chart-review phenotyping with note features: `wei2025_mci_adrd_phenotyping_ehr`
- symptom burden or informal cognitive/behavioral language: `mccoy2020_dementia_ehr`, `gilmorebykovskyi2018_ci_ehr_phenotype`

The synthesis implication is a staged comparison rather than a single text representation.

### 3. Interpretable Concepts Are the Most Defensible First Text Layer

The literature supports testing embeddings and transformer models, but interpretable note-derived concepts remain the clearest bridge to clinical review and study design. `penfold2022_mci_nlp`, `benmiled2023_dementia_notes`, `wei2025_mci_adrd_phenotyping_ehr`, `khan2026_next_generation_efi`, and `kashyap2025_explainable_dementia_types` support concept-based approaches. `du2024_llm_cognitive_decline_notes` and `wornow2023_shaky_foundations_ehr_fm` caution against assuming general-purpose LLMs beat local task-specific systems.

### 4. Diagnosis Opportunity Is a Core Label Problem

The reviewed diagnosis-opportunity papers now make the bias concern concrete. `bynum2024_regional_variation_diagnostic_intensity_dementia` supports geographic/diagnostic-intensity variation; `tzeng2024_annual_wellness_visits_early_dementia_diagnosis` supports annual wellness visits as an opportunity mechanism; `mattke2023_expected_diagnosed_mci_dementia_medicare` and `liu2024_detection_rates_mci_primary_care` show large expected-versus-diagnosed gaps; `spoto2025_diagnostic_signal_decay_dementia` cautions that dementia-code performance can vary.

Future coded diagnosis is therefore an observed care-pathway event, not a pure disease-state label.

### 5. Model Architecture Is Secondary to Design Validity

ClinicalBERT, BioBERT, GatorTron, BEHRT, Med-BERT, RETAIN, CLMBR-style representations, multimodal transformers, and evidential fusion methods are useful options. But none solve target, label, timing, transportability, or clinical utility by themselves. `steinberg2021_ehr_language_models`, `wornow2023_ehrshot`, and `wornow2023_shaky_foundations_ehr_fm` support strong baselines and careful benchmark interpretation. `lyu2022_multimodal_mortality_notes`, `garriga2023_mental_health_crises_notes`, `song2022_home_health_notes`, and `ruan2025_icu_multimodal_notes` are useful analogies for multimodal fusion and metrics, not dementia evidence.

### 6. Validation Must Be Designed Around Deployment

The strongest recurring validation lesson is negative: discrimination alone is insufficient. The study needs internal validation, temporal validation, possible site/practice validation, calibration, threshold operating points, and prevalence-aware PPV/NPV. `john2022_dementia_prediction_validation`, `lu2026_ehr_dementia_prediction_review`, `benmiled2023_dementia_notes`, `wei2025_mci_adrd_phenotyping_ehr`, and `wornow2023_shaky_foundations_ehr_fm` all support this.

## Major Gaps

### 1. Direct Cardiology Cognitive-Care Workflow Evidence Is Still Thin

`adejumo2024_hf_functional_status_nlp` supports cardiology-note NLP feasibility, but the review still lacks enough cardiology-specific cognitive screening, referral, documentation, and care-gap literature.

### 2. "Current Unmet Cognitive Care Need" Still Lacks a Ready Label

The most clinically attractive target may be current unmet cognitive care need, but reviewed papers do not provide an off-the-shelf operational label. Cognitive tests, chart review, note evidence, dementia codes, medications, referrals, and future diagnosis all measure different constructs.

### 3. Timing and Leakage Remain Underreported

Many studies define lookback windows or prediction horizons, but fewer provide enough note timestamps, signing times, note types, encounter links, or section handling to reproduce feature availability at a precise decision point.

### 4. External Transportability Is Weak

`benmiled2023_dementia_notes` is important because it directly demonstrates cross-institution performance degradation. Many other studies are single-system, internally validated, or benchmark-based.

### 5. EHR Schema and Reproducible Data Transformation Remain Underdeveloped

The review has many modeling papers but fewer practical references for Epic-to-model-ready transformation, OMOP/FHIR mapping, note metadata, source timestamps, vocabulary mapping, and local code-set governance.

## Areas of Agreement

- EHR text contains clinically useful signal not captured by structured fields.
- Diagnosis codes alone are weak labels for cognitive impairment and dementia.
- Absence of a dementia or MCI code should not be treated as absence of impairment.
- Target, label, index date, observation window, and horizon must be explicit.
- Structured baselines and simple NLP baselines are required before claiming advanced model value.
- Calibration, thresholding, and clinical utility need to be evaluated alongside AUROC/AUPRC.
- External or at least local temporal/site validation is necessary for any cardiology-facing model.

## Areas of Tension or Disagreement

- Future coded dementia is operationally convenient but biased by care opportunity.
- Current cognitive impairment is clinically meaningful but harder to label retrospectively.
- LLMs may help with concept extraction or adjudication, but direct LLM scoring is not yet supported as the first strategy.
- Raw embeddings can improve performance but are harder to audit than note-derived concepts.
- Diagnosis-opportunity variables may be confounders, mediators, ascertainment mechanisms, or care-pathway descriptors depending on the chosen target.

## Target and Label Lessons

The target decision should be made before model development. Candidate targets remain:

- current unmet cognitive care need
- current undocumented cognitive impairment
- future cognitive impairment
- future coded dementia/MCI diagnosis
- future referral, cognitive testing, or specialty evaluation

The label design should include positive, negative, and indeterminate categories. It should preserve label provenance: diagnosis code, cognitive test, chart-reviewed impairment, note evidence, referral/order, medication, specialist visit, or downstream diagnosis.

## EHR Text and Feature Lessons

The first note-feature inventory should prioritize:

- cognition and memory concerns
- executive function and attention
- confusion, disorientation, delirium language
- function and IADLs
- medication management and adherence
- appointment navigation and missed visits
- caregiver or collateral concern
- falls, mobility, frailty, sensory barriers
- social support, living situation, safety concerns
- cognitive testing, referrals, and diagnostic-workup mentions as separate care-process features

The strongest design is likely a staged comparison:

1. structured baseline
2. structured plus note-derived concepts
3. structured plus note embeddings
4. notes-only model
5. multimodal fusion
6. LLM-assisted extraction or adjudication if it adds measurable value

## Modeling Lessons

The current modeling ladder remains appropriate:

- Start with a transparent structured baseline.
- Add interpretable note concepts before opaque representations.
- Compare against TF-IDF/logistic regression or gradient boosting baselines.
- Add embeddings or sequence models only when they answer a defined design need.
- Treat LLMs as tools for extraction, weak labeling, adjudication, or ensembling before considering standalone scoring.
- Evaluate multimodal methods only after target/label/timing are stable.

The newest multimodal papers (`li2025_multimodal_dementia`, `garriga2023_mental_health_crises_notes`, `lyu2022_multimodal_mortality_notes`, `ruan2025_icu_multimodal_notes`) support methods exploration but do not change the main conclusion that architecture is secondary.

## Validation and Transportability Lessons

Minimum validation expectations for the first study should include:

- patient-level or encounter-level split discipline that avoids leakage
- temporal validation if calendar time permits
- site/practice/clinic validation if the data support it
- calibration plot, intercept, slope, and Brier score
- threshold-specific sensitivity, specificity, PPV, and NPV
- AUPRC for rare outcomes
- subgroup checks by age, sex, race/ethnicity, insurance, language, and utilization where feasible
- source-provenance analysis for labels
- sensitivity analysis for diagnosis opportunity and follow-up completeness

`benmiled2023_dementia_notes` should be used as a direct warning that note models can fail to transport even when the target is similar.

## Bias and Downstream-Action Lessons

The study should explicitly separate:

- pre-index patient state
- pre-index documentation
- post-index cognitive workup
- opportunity for diagnosis
- future diagnosis or cognitive-care event
- follow-up completeness and censoring

Potential diagnosis-opportunity variables include annual wellness visits, PCP follow-up, neurology/geriatrics/psychiatry/memory-clinic encounters, cognitive testing, neuroimaging, biomarker testing, hospitalization, death, insurance, geography, practice-level diagnostic intensity, and visit frequency.

## Implications for Our Study Design

- Anchor rows to `patient_id + cardiology_encounter_id + encounter_start_time`.
- Restrict predictors to data available before `encounter_start_time`.
- Store post-index referral, testing, diagnosis, and specialty contact as outcome/opportunity variables, not predictors.
- Choose one primary target and one primary horizon before modeling.
- Create a validation-label sample if feasible, because code-only labels are not enough.
- Preserve indeterminate labels rather than forcing every patient into case/control status.
- Compare structured-only, note-concept, note-embedding, and multimodal models.
- Report calibration and threshold performance before claiming clinical usefulness.
- Document the Epic-to-model-ready pipeline with source tables, timestamps, note classes, code lists, and feature provenance.

## Implications for the Review Workflow

- The paper-by-paper lifecycle rule added to `AGENTS.md` should remain the default.
- The state file should continue to separate processing inventory from interpretive outline sections.
- A specialist synthesis on label/target validity would now be useful.
- A specialist synthesis on EHR text concept inventory would now be useful.
- A specialist synthesis on Epic-to-model-ready schema requirements would now be useful.
- Central quantitative claims still need source checks before manuscript drafting.

## Claims Ready to Carry Forward

- EHR text contains cognitive, functional, and care-context signal relevant to dementia/cognitive-impairment detection and prediction.
- Diagnosis-code labels are not sufficient as pure disease-state labels.
- Absence of dementia/MCI codes is not a defensible negative label by itself.
- Future coded diagnosis is strongly shaped by diagnosis opportunity and care pathways.
- Interpretable note-derived concepts are a defensible first text representation.
- Strong structured and simple NLP baselines are required before claiming advanced model value.
- External transportability and calibration are common weaknesses in the field.

## Claims That Need More Evidence

- Cardiology notes specifically improve cognitive-risk prediction beyond structured EHR data.
- Current unmet cognitive care need can be labeled retrospectively with acceptable validity.
- Diagnosis opportunity can be measured well enough to adjust, stratify, or reweight future diagnosis labels.
- LLM-assisted extraction improves over local supervised NLP for this specific task.
- Any specific multimodal architecture is worth the added complexity for pre-cardiology deployment.

## Papers or Topics to Add

- Cognitive screening, recognition, and referral in cardiology clinics.
- Cognitive impairment in heart failure, atrial fibrillation, CAD, valvular disease, and other cardiology populations.
- Validated EHR phenotypes for MCI, ADRD, and cognitive impairment.
- Diagnostic-opportunity and outcome-ascertainment methods for dementia.
- Epic-to-OMOP, Epic-to-FHIR, or Epic-to-model-ready prediction pipelines.
- Clinical note sectioning, assertion, temporality, experiencer, and copied-forward text handling.
- Calibration and decision-curve analysis for clinical risk models.

## Recommended Next Actions

1. `update_study_design_template`: Define the first target, prediction horizon, index time, observation window, and eligible encounters.
2. `add_specialist_synthesizer`: Create label/target, EHR-text-concept, and EHR-schema synthesis passes.
3. `source_document_check`: Source-check central papers before manuscript drafting, especially direct dementia-note and diagnosis-opportunity papers.
4. `bibliography_expansion`: Search cardiology-specific cognitive screening/referral/care-gap literature.
5. `draft_manuscript_section`: Begin a rough Section 2-6 evidence map once target choice is made.
6. `update_agent_guidance`: Keep enforcing paper-by-paper lifecycle processing for future batches.
