# Synthesis: Major Ideas and Gaps

## Synthesis Status
synthesis_complete

## Synthesis Question
What are the major ideas and gaps emerging from the reviewed papers, and how should they change the literature review and study design?

## Included Papers and Review Status
All 30 reviewed papers have consolidated reviews.

Core direct or high-value papers:
- `lu2026_ehr_dementia_prediction_review`
- `john2022_dementia_prediction_validation`
- `adejumo2024_hf_functional_status_nlp`
- `khan2026_next_generation_efi`
- `osman2024_nlp_ageing_syndromes`
- `zhou2025_preoperative_frailty_llm`

Supporting dementia, MCI, and AD prediction context:
- `grammenos2024_explainable_mci_ad`
- `grueso2021_mci_ad_ml_review`
- `kumar2021_ad_progression_ml_review`
- `pellegrini2018_neuroimaging_ml_review`
- `amini2024_speech_ad_progression`

Supporting clinical NLP, language model, and EHR representation context:
- `alsentzer2019_clinical_bert_embeddings`
- `huang2019_clinicalbert_readmission`
- `lee2019_biobert`
- `yang2022_gatortron`
- `singhal2022_medpalm`
- `choi2016_retain`
- `li2020_behrt`
- `rasmy2021_medbert`

Supporting causal, target-trial, sequential-diagnosis, and feature-acquisition context:
- `liang2025_target_trial_emulation`
- `aronsson2025_active_feature_acquisition`
- `janisch2020_costly_features`
- `vivar2020_peri_diagnostic_feature_acquisition`
- `poh1996_information_value`
- `horvitz1987_beliefs_actions_resources`
- `kaelbling1998_pomdp_survey`
- `heckerman1991_probabilistic_similarity_networks`
- `blumlein2022_causal_tree_dtr`
- `liu2018_deep_rl_dtr`
- `yazzourh2025_medical_knowledge_rl_dtr`

## Executive Takeaway
The literature supports the project intuition that longitudinal EHR data, especially free text, may contain useful cognitive and geriatric-risk signals before a cardiology encounter. But the main contribution should not be framed as applying a newer model. The stronger contribution is careful encounter-level target definition, label construction, timing, validation, and handling of downstream-action or diagnosis-opportunity bias.

## Major Ideas

### Target Definition Is the Central Design Choice
The reviewed literature repeatedly shows that "dementia prediction" is not a single task. It can mean known dementia, unrecognized current dementia, current unmet cognitive care need, future cognitive impairment, future coded diagnosis, referral, testing, or care pathway.

`lu2026_ehr_dementia_prediction_review` and `john2022_dementia_prediction_validation` support this directly. `zhou2025_preoperative_frailty_llm` supports the broader methodological point by showing that different frailty labels produce different learned constructs.

### Labels Are Care-Pathway Products, Not Pure Disease States
Diagnosis codes, referrals, cognitive tests, specialist visits, and documentation are partly produced by clinical attention and opportunity for diagnosis. This makes label construction a primary methodological problem.

The strongest direct warning comes from `lu2026_ehr_dementia_prediction_review`; the strongest analogy is `zhou2025_preoperative_frailty_llm`. `liang2025_target_trial_emulation` supports the need for clearer design logic, though it remains indirect for the first risk-score model.

### EHR Text Is Useful, But Interpretable Concepts Are the Most Defensible First Step
The evidence supports using notes, but not jumping straight to end-to-end LLM scoring. `adejumo2024_hf_functional_status_nlp` shows cardiology notes can reveal underdocumented clinical state. `khan2026_next_generation_efi` shows note-derived geriatric deficits can form interpretable risk features. `osman2024_nlp_ageing_syndromes` shows broader feasibility of NLP for geriatric syndrome identification while warning that external validation is limited.

### Validation and Calibration Are Field-Level Weaknesses
`lu2026_ehr_dementia_prediction_review` and `john2022_dementia_prediction_validation` jointly establish that external validation, calibration, thresholding, and full model reporting are weak points in dementia prediction. AUROC alone is not enough for a cardiology-facing score.

### Architecture Is Secondary
ClinicalBERT, BioBERT, GatorTron, Med-BERT, BEHRT, RETAIN, and related papers are useful background. They show plausible modeling tools, but they do not solve the project's target, label, timing, validation, or workflow problems.

### Sequential Diagnosis Belongs Later
Feature-acquisition, value-of-information, POMDP, and dynamic-treatment-regime papers help frame future action policy, but they should not drive the first model. The first model should remain a pre-encounter risk score.

## Major Gaps

### Direct Cardiology Cognitive-Care Evidence
The review still lacks direct literature on cognitive screening, recognition, referral, communication, and care gaps in cardiology settings.

### Operational Labels for Current Unmet Cognitive Care Need
The most clinically attractive target may be current unmet cognitive care need, but the reviewed literature does not yet provide a ready operational label.

### Diagnosis Opportunity and Follow-Up Completeness
The project needs papers and design work on measuring opportunity for diagnosis: PCP contact, neurology or geriatrics contact, cognitive testing, referral, follow-up completeness, competing death, and censoring.

### Source-Level Deepening of Key Papers
Several reviews were generated from neutral summaries. Before manuscript drafting, central papers need exact source checks for methods, labels, validation metrics, and limitations.

### EHR Schema and Reproducibility
The data transformation section remains thin. The review needs stronger evidence on Epic-to-OMOP or other common data model pathways, note preprocessing, code lists, and reproducible feature definitions.

## Areas of Agreement
- Target and label definition matter more than model novelty.
- EHR text can capture clinically useful information missing from structured data.
- Interpretable note-derived concepts are a strong first strategy.
- External validation, calibration, and thresholding should be designed from the beginning.
- Future diagnosis labels can reflect care pathways and diagnosis opportunity.

## Areas of Tension or Disagreement
- EHR text is promising, but the field does not yet prove it is sufficient for pre-cardiology cognitive-risk scoring.
- Foundation models are powerful, but most supporting evidence is methodological background rather than direct clinical deployment evidence.
- Sequential diagnosis methods are relevant to the long-term vision, but including them too early risks shifting the project away from the first risk-score target.
- Future coded diagnosis is easier to operationalize than unmet care need, but it is more vulnerable to downstream-action bias.

## Target and Label Lessons
The first study should explicitly choose among:
- Current unmet cognitive care need.
- Currently present but undocumented cognitive impairment.
- Future cognitive impairment.
- Future coded dementia diagnosis.
- Future referral, testing, or care pathway.

These should not be collapsed. The label strategy should include positive, negative, and indeterminate categories, and should not treat absence of a dementia code as proof of no impairment.

## EHR Text and Feature Lessons
The first text-enhanced model should likely use note-derived concepts before raw end-to-end LLM scoring. Candidate concepts include cognitive symptoms, function, IADLs, caregiver concern, medication management, appointment navigation, delirium/confusion, falls, mobility, frailty, sensory impairment, social isolation, and assistance needs.

`adejumo2024_hf_functional_status_nlp` supports cardiology-note extraction. `khan2026_next_generation_efi` supports interpretable deficit features. `osman2024_nlp_ageing_syndromes` supports feasibility with validation caution.

## Modeling Lessons
Recommended modeling ladder:
1. Structured baseline.
2. Structured data plus note-derived concepts.
3. Structured data plus note embeddings.
4. Longitudinal sequence model.
5. LLM-assisted extraction or augmentation.
6. End-to-end LLM scoring only if justified.

This ladder is consistent with the reviewed evidence and avoids making architecture the contribution before the target is defensible.

## Validation and Transportability Lessons
The study should pre-specify:
- Internal validation.
- Temporal validation.
- Site or practice validation if possible.
- Calibration plot, intercept, and slope.
- Threshold-specific sensitivity, specificity, PPV, and NPV.
- Decision-curve or net-benefit analysis if a threshold will inform action.
- Sufficient reporting for external validation or recalibration.

`john2022_dementia_prediction_validation` is especially important here because it shows that published models often omit details needed for validation.

## Bias and Downstream-Action Lessons
The key bias problem is not merely confounding. It is that labels may be created by downstream evaluation, referral, testing, documentation, and access. The study should separately track:
- Cognitive outcome evidence.
- Opportunity for diagnosis.
- Downstream action after cardiology.
- Follow-up completeness.
- Competing death or censoring.
- PCP, neurology, geriatrics, psychiatry, or memory-clinic contact.

## Implications for Our Study Design
- Anchor every row to `patient_id + cardiology_encounter_id + encounter_start_time`.
- Use only data strictly before `encounter_start_time`.
- Treat post-index referral, testing, diagnosis, and follow-up as outcome/opportunity variables, not predictors.
- Decide the primary target with MD input before modeling.
- Build a cognitive/frailty note-concept inventory before choosing final architectures.
- Include a structured baseline and calibration plan from the beginning.

## Implications for the Review Workflow
- Add an NLP/concept-extraction specialist reviewer.
- Add an EHR schema/common-data-model specialist reviewer.
- Use `searcher.md` to find direct cardiology cognitive-screening and referral literature.
- Source-check central papers before manuscript drafting.

## Claims Ready to Carry Forward
- EHR dementia prediction models often have weak target definitions, labels, calibration, validation, and reporting.
- EHR text can contain clinically useful information missing from structured fields.
- Interpretable note-derived concepts are a defensible first text strategy.
- Label source can change what a model learns.
- The first model should be scoped to pre-encounter risk scoring, not action recommendation.

## Claims That Need More Evidence
- That cardiology notes specifically contain cognitive-risk signals.
- That text-derived concepts improve cognitive-risk prediction beyond structured EHR data.
- That current unmet cognitive care need can be reliably labeled retrospectively.
- That diagnosis opportunity can be measured well enough to adjust or stratify labels.
- That any specific foundation model should be preferred for this project.

## Papers or Topics to Add
- Cardiology cognitive screening and referral workflows.
- Cognitive impairment recognition in cardiovascular clinics.
- Validated dementia or cognitive-impairment EHR phenotypes.
- Diagnostic opportunity, outcome ascertainment, and referral bias in dementia.
- Epic-to-OMOP or EHR-to-common-data-model transformation for prediction.
- Clinical-note concept extraction studies for cognition, function, caregiver concern, and navigation difficulty.

## Recommended Next Actions
1. Decide the first candidate target and outcome window with MD input.
2. Build the first cognitive/frailty note-concept inventory.
3. Source-check the central papers before manuscript drafting: `lu2026_ehr_dementia_prediction_review`, `john2022_dementia_prediction_validation`, `zhou2025_preoperative_frailty_llm`, `adejumo2024_hf_functional_status_nlp`, `khan2026_next_generation_efi`, and `liang2025_target_trial_emulation`.
4. Use `searcher.md` to find direct cardiology cognitive-care workflow papers.
5. Add NLP/concept-extraction and EHR schema/common-data-model specialist reviewers.
