# Literature Review State

This file tracks where the literature review stands relative to [literature_review_outline.md](literature_review_outline.md). It is a working state document, not manuscript prose.

## Current Evidence Base

### Reviewed Papers

Core reviewed papers with earlier hand-written reviews:

- `lu2026_ehr_dementia_prediction_review`: Core methodological anchor for EHR dementia prediction quality, target ambiguity, label weakness, calibration gaps, and sparse external validation.
- `adejumo2024_hf_functional_status_nlp`: Cardiology-note NLP analogue showing clinical state can be extracted from outpatient cardiovascular notes.
- `khan2026_next_generation_efi`: Frailty/NLP analogue showing interpretable note-derived deficits can improve geriatric-risk representation.
- `osman2024_nlp_ageing_syndromes`: Systematic review of NLP for ageing syndromes, including dementia, with validation-quality cautions.
- `zhou2025_preoperative_frailty_llm`: Label-definition analogue showing different frailty labels can produce different learned constructs.

Newly reviewed papers with primary review, specialist reviews, and consolidated review generated from neutral summaries:

- Dementia, MCI, and AD prediction/review: `john2022_dementia_prediction_validation`, `grammenos2024_explainable_mci_ad`, `grueso2021_mci_ad_ml_review`, `kumar2021_ad_progression_ml_review`, `pellegrini2018_neuroimaging_ml_review`, `amini2024_speech_ad_progression`.
- EHR and clinical language models: `alsentzer2019_clinical_bert_embeddings`, `huang2019_clinicalbert_readmission`, `lee2019_biobert`, `yang2022_gatortron`, `singhal2022_medpalm`.
- Longitudinal EHR representation: `choi2016_retain`, `li2020_behrt`, `rasmy2021_medbert`.
- Causal design and target-trial framing: `liang2025_target_trial_emulation`.
- Sequential diagnosis, feature acquisition, and decision policy: `aronsson2025_active_feature_acquisition`, `janisch2020_costly_features`, `vivar2020_peri_diagnostic_feature_acquisition`, `poh1996_information_value`, `horvitz1987_beliefs_actions_resources`, `kaelbling1998_pomdp_survey`, `heckerman1991_probabilistic_similarity_networks`, `blumlein2022_causal_tree_dtr`, `liu2018_deep_rl_dtr`, `yazzourh2025_medical_knowledge_rl_dtr`.

### Review Depth Note

All papers currently in the review inventory now have primary reviews, current specialist reviews, and consolidated reviews. Many reviews were generated from neutral summaries rather than deep source re-extraction. Source-document checks are still needed before relying on a paper for a central manuscript claim, exact methods claim, or quantitative performance claim.

### Cross-Paper Synthesis

- `synthesis/synthesis_20260709_major_ideas_and_gaps.md`: Current cross-paper synthesis of major ideas, gaps, tensions, and study-design implications.

## 1. Introduction and Clinical Motivation

### Current State

The core motivation is coherent but still needs more direct clinical evidence. The reviewed literature supports the idea that routine EHR data and clinical text contain signals relevant to cognitive or geriatric status, but we have not yet reviewed much cardiology-specific cognitive-care literature.

### Supporting Evidence

- `lu2026_ehr_dementia_prediction_review` supports the broad relevance of EHR data for dementia detection and prediction, while warning that the field is not clinically mature.
- `adejumo2024_hf_functional_status_nlp` supports the cardiology-note premise: outpatient cardiovascular notes contain underused clinical-state information.
- `osman2024_nlp_ageing_syndromes` supports feasibility of NLP for geriatric syndromes, including dementia, across EHR text sources.

### Gaps

- Need clinical literature on cognitive screening, recognition, referral, or care gaps in cardiology settings.
- Need stronger evidence on cardiologist-facing workflow needs and acceptable model outputs.

## 2. Clinical Target and Prediction Setting

### Current State

This is one of the strongest emerging lessons: the target definition is central. "Dementia prediction" is too broad and can mean current impairment, undocumented impairment, future impairment, future coded diagnosis, referral, testing, or care pathway.

The current project focus is pre-cardiology-encounter risk scoring. The working unit is:

```text
patient_id + cardiology_encounter_id + encounter_start_time
```

### Supporting Evidence

- `lu2026_ehr_dementia_prediction_review` shows that published EHR dementia models often blur diagnostic and prognostic targets.
- `zhou2025_preoperative_frailty_llm` shows that different operational labels can make models learn different constructs.
- `john2022_dementia_prediction_validation` directly supports reporting and external-validatability concerns for dementia prediction models.

### Gaps

- Need to decide the first primary target: current unmet cognitive care need versus future cognitive impairment versus future coded diagnosis.
- Need MD input on which target is clinically meaningful before a cardiology encounter.
- Need more papers on operational definitions of unmet cognitive care need and undiagnosed cognitive impairment.

## 3. Cohort Construction and Timing

### Current State

The index time should be the start of the cardiology encounter. Inputs should be limited to EHR data strictly before that time. This is clear in our design but often unclear in the broader literature.

### Supporting Evidence

- `lu2026_ehr_dementia_prediction_review` identifies unclear prediction tasks, unclear time origins, and weak model reporting as common limitations.
- The 20260706 synthesis concluded that index date, observation window, and prediction horizon need to be tracked explicitly for every reviewed paper.

### Gaps

- Need more reviewed evidence on encounter-level prediction designs.
- Need a concrete study-design decision on repeated cardiology encounters per patient.
- Need rules for prior-history requirements and follow-up requirements.

## 4. Label Definition and Outcome Validity

### Current State

This is a core methodological problem. Diagnosis codes, cognitive tests, chart review, referrals, and NLP-derived labels measure different things. Absence of a dementia code is not a defensible negative label by itself.

### Supporting Evidence

- `lu2026_ehr_dementia_prediction_review` is the main anchor: many EHR dementia models use weak or ambiguous outcome definitions, and only a small minority use established diagnostic criteria.
- `zhou2025_preoperative_frailty_llm` provides a strong analogue: VES-13 and eFI labels produced different frailty constructs.
- `osman2024_nlp_ageing_syndromes` shows that NLP phenotyping studies often rely on manual text review but vary in validation quality.
- `khan2026_next_generation_efi` supports interpretable deficit extraction but does not validate a dementia label.

### Gaps

- Need deeper source checks for label details in the papers that become central to the label-definition section.
- Need papers on validated dementia and cognitive-impairment EHR phenotypes.
- Need a plan for indeterminate cases rather than forcing all patients into positive or negative labels.

## 5. Downstream-Action and Diagnosis-Opportunity Bias

### Current State

This may be the project's most important methodological contribution. Future diagnosis, testing, and referral labels are partly caused by downstream clinical action and opportunity for diagnosis.

### Supporting Evidence

- `lu2026_ehr_dementia_prediction_review` supports the concern indirectly through diagnosis-code and documentation limitations.
- The problem statement gives the central example: two equivalent patients may diverge because one is referred and one is not.
- `liang2025_target_trial_emulation` is relevant for formalizing cohort and causal design, though its fit to the first risk-score model remains indirect.

### Gaps

- Need papers directly addressing diagnostic opportunity, differential follow-up, referral bias, or outcome ascertainment bias in dementia.
- Need to decide whether diagnosis opportunity is modeled, stratified, adjusted for, or used for sensitivity analyses.
- Need definitions for post-index PCP contact, neurology/geriatrics/psychiatry/memory-clinic contact, cognitive testing, competing death, and censoring.

## 6. EHR Text as a Signal Source

### Current State

The literature supports EHR text as a useful signal source, but the strongest current strategy is probably not end-to-end LLM scoring. Interpretable note-derived concepts are more defensible as an intermediate representation.

### Supporting Evidence

- `adejumo2024_hf_functional_status_nlp` shows cardiology notes can support clinical-state extraction and increase capture beyond explicit structured mentions.
- `khan2026_next_generation_efi` shows NLP-derived deficits from notes can support interpretable geriatric-risk modeling.
- `osman2024_nlp_ageing_syndromes` shows broad feasibility of NLP for ageing syndromes but highlights limited external validation.
- `lu2026_ehr_dementia_prediction_review` notes that unstructured EHR data are underused in dementia prediction models.

### Gaps

- Need an explicit cognitive/frailty note-concept inventory.
- Need specialist review of NLP extraction methods, annotation quality, note sectioning, negation, and portability.
- Need more direct dementia-note NLP papers and papers using outpatient/cardiology notes.

## 7. Structured and Longitudinal EHR Representation

### Current State

We now have review-level coverage of major EHR representation approaches, but several reviews are summary-grounded and need source checks before detailed architecture claims. The working hypothesis is that structured baselines and interpretable longitudinal concepts should precede more complex sequence models.

### Supporting Evidence

- `khan2026_next_generation_efi` supports structured plus note-derived deficit representations.
- `choi2016_retain`, `li2020_behrt`, and `rasmy2021_medbert` are now reviewed anchors for longitudinal EHR representation.
- `alsentzer2019_clinical_bert_embeddings`, `huang2019_clinicalbert_readmission`, `lee2019_biobert`, and `yang2022_gatortron` are now reviewed anchors for clinical text representation.

### Gaps

- Need deeper source checks of RETAIN, BEHRT, Med-BERT, ClinicalBERT, and GatorTron before using them for detailed architecture or performance claims.
- Need to decide how much temporality is required for the first model.
- Need comparison of interpretable concept features versus raw note embeddings.

## 8. Modeling Strategy

### Current State

The strongest current modeling lesson is conservative: start simple and treat architecture as secondary to target, label, timing, and validation. A model ladder has been drafted in the study-design template.

### Supporting Evidence

- `lu2026_ehr_dementia_prediction_review` found no clear evidence that AI methods solve the field's core limitations by themselves.
- `adejumo2024_hf_functional_status_nlp` supports a practical supervised ClinicalBERT extraction pattern.
- `khan2026_next_generation_efi` supports interpretable NLP-derived deficit features rather than opaque end-to-end scoring.
- `zhou2025_preoperative_frailty_llm` warns that high model performance can be label-dependent.

### Gaps

- Need stronger comparison papers for structured baselines versus text-enhanced models in dementia or cognitive impairment.
- Need a decision on whether LLMs are used for concept extraction, weak labeling, summarization, augmentation, or direct scoring.
- Need model evaluation tied to clinical use, not just AUROC.

## 9. Validation, Calibration, and Clinical Utility

### Current State

Validation is a major weakness in the literature and must be designed from day one. AUROC alone is not enough. Calibration, threshold performance, temporal/site validation, and clinical utility are central.

### Supporting Evidence

- `lu2026_ehr_dementia_prediction_review` is the primary anchor: external validation and calibration are sparse in EHR dementia prediction.
- `osman2024_nlp_ageing_syndromes` shows external validation is also limited in ageing-syndrome NLP.
- `adejumo2024_hf_functional_status_nlp` shows useful multi-site validation within one health system, but not broader external validation.
- `john2022_dementia_prediction_validation` is now reviewed and should be prioritized for source-checking before manuscript use.

### Gaps

- Need deeper source checks for validation details in the papers that become central to the validation section.
- Need to define temporal validation and site/practice validation options for our data.
- Need clinical thresholds tied to cardiology workflow.
- Need decision-curve or net-benefit framing if a score will guide action.

## 10. Data Transformation and Reproducibility

### Current State

This section is underdeveloped. The project anticipates an Epic-to-model-ready pipeline and possibly OMOP or another common data model, but reviewed evidence is thin.

### Supporting Evidence

- `adejumo2024_hf_functional_status_nlp` is relevant as an Epic-like cardiology-note NLP implementation analogue, but it is not a data-model paper.
- `lu2026_ehr_dementia_prediction_review` supports reproducibility concerns through reporting and implementation gaps.

### Gaps

- Need papers on Epic-to-OMOP or EHR-to-common-data-model translation for prediction modeling.
- Need papers on reproducible clinical-note preprocessing and feature extraction.
- Need a specialist reviewer for EHR schema/common-data-model implications.

## 11. Sequential Diagnosis and Future Action Policy

### Current State

This is future framing, not the first model's scope. The first model should score pre-encounter risk and remain compatible with later action-policy work.

### Supporting Evidence

- `aronsson2025_active_feature_acquisition`, `janisch2020_costly_features`, `vivar2020_peri_diagnostic_feature_acquisition`, `poh1996_information_value`, `horvitz1987_beliefs_actions_resources`, and `kaelbling1998_pomdp_survey` are now reviewed anchors.
- The 20260706 synthesis concluded these papers belong later but help frame future "what should the cardiologist do next?" work.

### Gaps

- Need deeper source checks only after the risk-score target and label strategy are better settled.
- Need to avoid drifting into action recommendation before the first model is defined.
- Need a later synthesis that connects risk scores to value-of-information or feature-acquisition policies.

## 12. Synthesis and Proposed Contribution

### Current State

The emerging contribution is not a new architecture by itself. The likely contribution is careful cohort and label construction for pre-cardiology cognitive-risk scoring using longitudinal EHR text, with explicit attention to downstream-action and diagnosis-opportunity bias.

### Current Working Contribution

- Encounter-level prediction anchored at cardiology encounter start.
- Inputs limited to pre-encounter longitudinal EHR data.
- Text-derived cognitive, functional, behavioral, caregiver, adherence, frailty, falls, delirium, social, and navigation concepts.
- Labels that distinguish cognitive outcome evidence from care-pathway evidence.
- Validation and calibration designed for clinical workflow.
- Reproducible data transformation path from local EHR data to model-ready features.

### Gaps

- Need to act on the cross-paper synthesis recommendations.
- Need a human decision on target, outcome window, and acceptable label source.

## 13. Open Questions

### Highest-Priority Questions

- What primary target should the first model use?
- Is the target current unmet cognitive care need, future cognitive impairment, or future coded diagnosis?
- What label can be built and validated with available data?
- What post-index events define diagnosis opportunity?
- What note-derived concepts should be extracted first?

### Method Questions

- Should the first model use all available history or fixed lookback windows?
- Should repeated cardiology encounters per patient be allowed?
- What is the structured baseline?
- What is the first text-enhanced model?
- How will calibration and thresholds be evaluated?

### Workflow Questions

- Which consolidated papers need source-level deepening before manuscript drafting?
- Which central papers need exact label and validation extraction from the PDF or supplement?
- Which NLP/concept-extraction specialist findings should be promoted into the first note-concept inventory?
- Which EHR schema/common-data-model findings should be promoted into the Epic-to-model-ready pipeline specification?

## Near-Term Priorities

1. Decide the first candidate target and outcome window with MD input.
2. Build the first cognitive/frailty note-concept inventory.
3. Source-check the highest-value papers before manuscript use, especially `lu2026_ehr_dementia_prediction_review`, `john2022_dementia_prediction_validation`, `zhou2025_preoperative_frailty_llm`, `adejumo2024_hf_functional_status_nlp`, `khan2026_next_generation_efi`, and `liang2025_target_trial_emulation`.
4. Use `searcher.md` to find direct cardiology cognitive-screening, referral, and care-gap literature.
5. Use the NLP/concept-extraction and EHR schema/common-data-model specialist reviewer findings to refine the note-concept inventory and Epic-to-model-ready pipeline specification.
