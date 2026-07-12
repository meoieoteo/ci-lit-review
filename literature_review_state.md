# Literature Review State

This file tracks where the literature review stands relative to [literature_review_outline.md](literature_review_outline.md). It is a working state document, not manuscript prose.

## Current Evidence Base

### Reviewed Papers

This is a processing-status inventory only. Interpretive grouping belongs in the numbered outline sections below.

- `adejumo2024_hf_functional_status_nlp`
- `alsentzer2019_clinical_bert_embeddings`
- `amini2024_speech_ad_progression`
- `aronsson2025_active_feature_acquisition`
- `benmiled2023_dementia_notes`
- `blumlein2022_causal_tree_dtr`
- `bynum2024_regional_variation_diagnostic_intensity_dementia`
- `choi2016_retain`
- `du2024_llm_cognitive_decline_notes`
- `garriga2023_mental_health_crises_notes`
- `gilmorebykovskyi2018_ci_ehr_phenotype`
- `grammenos2024_explainable_mci_ad`
- `grueso2021_mci_ad_ml_review`
- `heckerman1991_probabilistic_similarity_networks`
- `hong2020_cognitive_concerns_nlp`
- `horvitz1987_beliefs_actions_resources`
- `huang2019_clinicalbert_readmission`
- `janisch2020_costly_features`
- `john2022_dementia_prediction_validation`
- `kaelbling1998_pomdp_survey`
- `kashyap2025_explainable_dementia_types`
- `khan2026_next_generation_efi`
- `kumar2021_ad_progression_ml_review`
- `lee2019_biobert`
- `li2020_behrt`
- `li2024_dementia_risk_notes`
- `li2025_multimodal_dementia`
- `liang2025_target_trial_emulation`
- `liu2018_deep_rl_dtr`
- `liu2024_detection_rates_mci_primary_care`
- `lu2026_ehr_dementia_prediction_review`
- `lyu2022_multimodal_mortality_notes`
- `mattke2023_expected_diagnosed_mci_dementia_medicare`
- `mccoy2020_dementia_ehr`
- `osman2024_nlp_ageing_syndromes`
- `pellegrini2018_neuroimaging_ml_review`
- `penfold2022_mci_nlp`
- `poh1996_information_value`
- `rasmy2021_medbert`
- `ruan2025_icu_multimodal_notes`
- `shao2019_probable_dementia_ehr`
- `shen2025_integrating_misclassified_ehr_outcomes`
- `singhal2022_medpalm`
- `song2022_home_health_notes`
- `spoto2025_diagnostic_signal_decay_dementia`
- `steinberg2021_ehr_language_models`
- `tyagi2021_cognitive_impairment_ehr`
- `tzeng2024_annual_wellness_visits_early_dementia_diagnosis`
- `vivar2020_peri_diagnostic_feature_acquisition`
- `wang2021_cognitive_decline_notes`
- `wei2025_mci_adrd_phenotyping_ehr`
- `wornow2023_ehrshot`
- `wornow2023_shaky_foundations_ehr_fm`
- `yang2022_gatortron`
- `yazzourh2025_medical_knowledge_rl_dtr`
- `zhou2025_preoperative_frailty_llm`

### Summary-Only Papers

- None currently tracked as summary-only in this state file.

### Bibliography and Source Intake Pending Summary/Review

The following papers were added to the bibliography/source inventory on 2026-07-12 from `clinical_notes_dementia_papers.md` and `clinical_notes_NOT_dementia.md`, but have not yet gone through formal summary, primary review, specialist review, or consolidation because no usable source document is currently available:

- `li2025_decision_focused_dissertation` (unverified metadata; no durable public source found)
- `amrollahi2021_sepsis_notes` (metadata only; direct source retrieval returned 403)

Intake details are recorded in `bibliography/clinical_notes_intake_20260712.md`.

### Pending Source and Workflow Follow-Up

- `bynum2024_regional_variation_diagnostic_intensity_dementia` and `tzeng2024_annual_wellness_visits_early_dementia_diagnosis` were reviewed from lawful full-text HTML before PDFs were available. PDFs are now saved in `papers/` and should be used for source-checking exact quantitative claims.

### Review Depth Note

All papers currently in the review inventory now have primary reviews, current specialist reviews, and consolidated reviews. Review files were produced through multiple agent workflows. Many older reviews were generated from neutral summaries rather than deep source re-extraction. The newest direct EHR text/modeling and Section 5 reviews listed above were generated from downloaded full text or lawful full-text HTML, but exact quantitative claims should still be source-checked before manuscript drafting. On 2026-07-12, PDFs were added for several papers previously reviewed from HTML: `wang2021_cognitive_decline_notes`, `du2024_llm_cognitive_decline_notes`, `li2024_dementia_risk_notes`, `gilmorebykovskyi2018_ci_ehr_phenotype`, `bynum2024_regional_variation_diagnostic_intensity_dementia`, and `tzeng2024_annual_wellness_visits_early_dementia_diagnosis`. `li2024_dementia_risk_notes` has since been reprocessed from the final article PDF. On 2026-07-12, ten additional clinical-note and multimodal EHR papers from `clinical_notes_dementia_papers.md` and `clinical_notes_NOT_dementia.md` were processed through summary, primary review, current specialist reviews, and consolidation: `penfold2022_mci_nlp`, `benmiled2023_dementia_notes`, `mccoy2020_dementia_ehr`, `li2025_multimodal_dementia`, `tyagi2021_cognitive_impairment_ehr`, `kashyap2025_explainable_dementia_types`, `garriga2023_mental_health_crises_notes`, `lyu2022_multimodal_mortality_notes`, `song2022_home_health_notes`, and `ruan2025_icu_multimodal_notes`.

Publication-weight caution:

- `hong2020_cognitive_concerns_nlp` is direct but lower publication weight because it is a short ML4H/arXiv extended abstract.
- `li2025_multimodal_dementia` is direct but lower publication weight because it is a dissertation rather than a peer-reviewed journal article.
- `tyagi2021_cognitive_impairment_ehr` is direct for cognitive-impairment NLP but lower publication weight because it is a short ML4H/arXiv-style source and does not validate patient-level risk prediction.
- `spoto2025_diagnostic_signal_decay_dementia` is direct but lower publication weight because it is an arXiv preprint.
- `shen2025_integrating_misclassified_ehr_outcomes` is methodologically relevant but indirect and lower publication weight because it is an arXiv preprint.
- `ruan2025_icu_multimodal_notes` is indirect and lower publication weight because it is an arXiv preprint and addresses ICU outcomes rather than dementia.
- `wornow2023_ehrshot` is indirect and lower publication weight because the downloaded source is a preprint benchmark.
- `wornow2023_shaky_foundations_ehr_fm` is peer-reviewed but indirect for dementia.

### Cross-Paper Synthesis

- `synthesis/synthesis_20260709_major_ideas_and_gaps.md`: Current cross-paper synthesis of major ideas, gaps, tensions, and study-design implications.
- `synthesis/synthesis_20260712_up_to_date_snapshot.md`: Up-to-date snapshot after adding ten clinical-note and multimodal EHR papers from `clinical_notes_dementia_papers.md` and `clinical_notes_NOT_dementia.md`.

## 1. Introduction and Clinical Motivation

### Current State

The core motivation is coherent but still needs more direct clinical evidence. The reviewed literature supports the idea that routine EHR data and clinical text contain signals relevant to cognitive or geriatric status, but we have not yet reviewed much cardiology-specific cognitive-care literature.

### Supporting Evidence

- `lu2026_ehr_dementia_prediction_review` supports the broad relevance of EHR data for dementia detection and prediction, while warning that the field is not clinically mature.
- `wang2021_cognitive_decline_notes` directly supports the claim that clinical notes can contain evidence of cognitive decline before structured MCI diagnosis.
- `li2024_dementia_risk_notes` directly supports the possibility of dementia-risk prediction from medical notes with explicit observation periods and prediction horizons.
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
- `wang2021_cognitive_decline_notes` distinguishes section-level evidence of cognitive decline from future patient-level diagnosis; it is detection before MCI code among patients selected by later MCI diagnosis.
- `li2024_dementia_risk_notes` is closer to prospective risk framing, with incident dementia cases and explicit six-month or one-year horizons, but uses retrospective case-control sampling.
- `du2024_llm_cognitive_decline_notes` reuses the Wang note-section label and is therefore model-comparison evidence, not an independent target definition.

### Gaps

- Need to decide the first primary target: current unmet cognitive care need versus future cognitive impairment versus future coded diagnosis.
- Need MD input on which target is clinically meaningful before a cardiology encounter.
- Need more papers on operational definitions of unmet cognitive care need, undiagnosed cognitive impairment, and cardiology-relevant cognitive-care opportunities.

## 3. Cohort Construction and Timing

### Current State

The index time should be the start of the cardiology encounter. Inputs should be limited to EHR data strictly before that time. This is clear in our design but often unclear in the broader literature.

### Supporting Evidence

- `lu2026_ehr_dementia_prediction_review` identifies unclear prediction tasks, unclear time origins, and weak model reporting as common limitations.
- `li2024_dementia_risk_notes` is a useful timing example because it explicitly varies one- versus two-year observation periods and six-month versus one-year prediction horizons.
- `wang2021_cognitive_decline_notes` uses notes from the four years before initial MCI diagnosis, which supports pre-diagnosis text signal but does not define an encounter-level risk setting.
- `wornow2023_ehrshot` provides an indirect benchmark example with explicit prediction times and horizons across structured EHR tasks.
- The 20260706 synthesis concluded that index date, observation window, and prediction horizon need to be tracked explicitly for every reviewed paper.

### Gaps

- Need more reviewed evidence on encounter-level prediction designs.
- Need a concrete study-design decision on repeated cardiology encounters per patient.
- Need rules for prior-history requirements and follow-up requirements.
- Need to decide whether the first model's horizon should prioritize near-term recognition opportunity, future diagnosis, or future cognitive-care pathway events.

## 4. Label Definition and Outcome Validity

### Current State

This is a core methodological problem. Diagnosis codes, cognitive tests, chart review, referrals, and NLP-derived labels measure different things. Absence of a dementia code is not a defensible negative label by itself.

### Supporting Evidence

- `lu2026_ehr_dementia_prediction_review` is the main anchor: many EHR dementia models use weak or ambiguous outcome definitions, and only a small minority use established diagnostic criteria.
- `wang2021_cognitive_decline_notes` provides a strong manual note-section label for cognitive decline, including annotator training, expert adjudication, and reported agreement.
- `du2024_llm_cognitive_decline_notes` uses the same manual label and shows how LLM evaluation depends on that underlying construct.
- `li2024_dementia_risk_notes` uses incident dementia case status and matched controls, but the exact code algorithm and prevalence translation need deeper checking.
- `wei2025_mci_adrd_phenotyping_ehr` provides direct chart-review-labeled MCI/ADRD phenotyping evidence and shows clinical notes substantially outperform ICD-only and medication-only phenotypes.
- `gilmorebykovskyi2018_ci_ehr_phenotype` shows that claims-identified dementia patients often have informal cognitive/behavioral symptom language in notes, but the derivation cohort lacks controls and does not validate predictive accuracy.
- `mattke2023_expected_diagnosed_mci_dementia_medicare` and `liu2024_detection_rates_mci_primary_care` show that absence of MCI claims is not a reliable negative cognitive label because expected MCI greatly exceeds diagnosed MCI.
- `spoto2025_diagnostic_signal_decay_dementia` adds a lower-weight caution that dementia-code specificity itself can degrade or vary across settings.
- `shen2025_integrating_misclassified_ehr_outcomes` supports treating EHR outcomes as silver-standard labels when a richer validation outcome is available.
- `zhou2025_preoperative_frailty_llm` provides a strong analogue: VES-13 and eFI labels produced different frailty constructs.
- `osman2024_nlp_ageing_syndromes` shows that NLP phenotyping studies often rely on manual text review but vary in validation quality.
- `khan2026_next_generation_efi` supports interpretable deficit extraction but does not validate a dementia label.

### Gaps

- Need deeper source checks for label details in the papers that become central to the label-definition section.
- Need papers on validated dementia and cognitive-impairment EHR phenotypes.
- Need a plan for indeterminate cases rather than forcing all patients into positive or negative labels.
- Need to decide how to separate cognitive state, cognitive documentation, cognitive workup, and formal diagnosis in the first label.

## 5. Downstream-Action and Diagnosis-Opportunity Bias

### Current State

This may be the project's most important methodological contribution. Future diagnosis, testing, and referral labels are partly caused by downstream clinical action and opportunity for diagnosis.

The Section 5 evidence base now contains direct support for diagnostic-intensity variation, annual wellness visits as diagnosis opportunity, large-scale expected-versus-diagnosed MCI/dementia gaps, primary-care MCI detection variation, and dementia coding-pattern variability. It also includes an indirect methods paper for misclassified EHR outcomes and non-random validation samples.

### Supporting Evidence

- `lu2026_ehr_dementia_prediction_review` supports the concern indirectly through diagnosis-code and documentation limitations.
- `wang2021_cognitive_decline_notes` shows notes may contain cognitive decline evidence before a structured MCI diagnosis, highlighting the gap between disease evidence and coded diagnosis.
- `gilmorebykovskyi2018_ci_ehr_phenotype` shows even claims-identified dementia patients may not have cognitive-impairment symptom documentation in the reviewed note window, highlighting documentation opportunity.
- `li2024_dementia_risk_notes` uses future incident dementia status, which is useful but still susceptible to diagnosis opportunity and follow-up ascertainment.
- The problem statement gives the central example: two equivalent patients may diverge because one is referred and one is not.
- `liang2025_target_trial_emulation` is relevant for formalizing cohort and causal design, though its fit to the first risk-score model remains indirect.
- `bynum2024_regional_variation_diagnostic_intensity_dementia` is direct evidence that regional diagnostic intensity changes the probability of receiving a new ADRD diagnosis even after adjustment for observed risk factors.
- `tzeng2024_annual_wellness_visits_early_dementia_diagnosis` directly supports annual wellness visits as diagnosis opportunity, especially for earlier MCI detection.
- `mattke2023_expected_diagnosed_mci_dementia_medicare` directly supports the claim that Medicare claims capture only a small fraction of expected MCI and that detection differs by race/ethnicity, dual eligibility, and Medicare coverage type.
- `liu2024_detection_rates_mci_primary_care` directly supports clinician- and practice-level variation in MCI detection, with most expected MCI cases undiagnosed in primary care claims.
- `spoto2025_diagnostic_signal_decay_dementia` is direct but lower-publication-weight evidence that inpatient dementia codes can lose specificity and vary geographically.
- `shen2025_integrating_misclassified_ehr_outcomes` is indirect methods evidence for treating EHR outcomes as silver-standard labels and designing validation samples that account for misclassification and selection.

### Gaps

- Need source checks of exact code lists, supplements, and quantitative claims before using central Section 5 estimates in manuscript prose.
- Need to decide how much weight to give the two preprints, `spoto2025_diagnostic_signal_decay_dementia` and `shen2025_integrating_misclassified_ehr_outcomes`, relative to the peer-reviewed Section 5 anchors.
- Need to decide whether diagnosis opportunity is modeled, stratified, adjusted for, or used for sensitivity analyses.
- Need definitions for annual wellness visits, post-index PCP contact, neurology/geriatrics/psychiatry/memory-clinic contact, cognitive testing, hospitalization, competing death, and censoring.

## 6. EHR Text as a Signal Source

### Current State

The literature now strongly supports EHR text as a useful signal source for cognitive decline and dementia risk. The strongest current strategy is still probably not end-to-end LLM scoring alone. Interpretable note-derived concepts, section-level classifiers, and strong local baselines are more defensible as intermediate or comparison representations.

### Supporting Evidence

- `wang2021_cognitive_decline_notes` is a direct anchor: note-section NLP detected cognitive decline before structured MCI diagnosis and outperformed keyword search and conventional baselines internally.
- `du2024_llm_cognitive_decline_notes` shows GPT-4 can classify cognitive-decline note sections, but did not outperform locally trained task-specific models; an ensemble had the best performance.
- `li2024_dementia_risk_notes` shows notes alone can support dementia-risk discrimination when observation period and prediction horizon are defined.
- `wei2025_mci_adrd_phenotyping_ehr` shows that note-derived TF-IDF n-gram features improve MCI/ADRD phenotyping over ICD-only and medication-only features, with a chart-review reference label.
- `hong2020_cognitive_concerns_nlp` is direct but lower publication weight evidence that progress-note NLP improves cognitive-concern detection over structured ICD/medication features.
- `shao2019_probable_dementia_ehr` supports structured-plus-unstructured EHR case finding for probable dementia, with label and validation caveats.
- `gilmorebykovskyi2018_ci_ehr_phenotype` supports broad cognitive/behavioral terminology beyond formal diagnostic terms, including confusion, orientation, executive function, and agitation.
- `adejumo2024_hf_functional_status_nlp` shows cardiology notes can support clinical-state extraction and increase capture beyond explicit structured mentions.
- `khan2026_next_generation_efi` shows NLP-derived deficits from notes can support interpretable geriatric-risk modeling.
- `osman2024_nlp_ageing_syndromes` shows broad feasibility of NLP for ageing syndromes but highlights limited external validation.
- `lu2026_ehr_dementia_prediction_review` notes that unstructured EHR data are underused in dementia prediction models.

### Gaps

- Need an explicit cognitive/frailty note-concept inventory.
- Need to decide whether the first text representation is terms/concepts, section classifiers, embeddings, LLM-extracted concepts, or a staged comparison.
- Need more outpatient/cardiology-specific cognitive-note papers.
- Need source-level extraction of note types, sectioning, negation, temporality, and annotation rules from the central direct papers before manuscript use.

## 7. Structured and Longitudinal EHR Representation

### Current State

We now have review-level coverage of major EHR representation approaches, but several reviews are summary-grounded and need source checks before detailed architecture claims. The working hypothesis is that structured baselines and interpretable longitudinal concepts should precede more complex sequence models.

### Supporting Evidence

- `khan2026_next_generation_efi` supports structured plus note-derived deficit representations.
- `shao2019_probable_dementia_ehr` directly compares structured EHR signals with unstructured-note information for probable dementia case finding.
- `li2024_dementia_risk_notes` supports a notes-only longitudinal representation over one- or two-year observation windows.
- `wornow2023_ehrshot` provides indirect structured-EHR benchmark support for longitudinal event-sequence modeling and few-shot evaluation, but excludes clinical text and is a preprint.
- `steinberg2021_ehr_language_models` provides peer-reviewed indirect support for self-supervised structured-EHR sequence representations, especially when task-specific labels are limited.
- `choi2016_retain`, `li2020_behrt`, and `rasmy2021_medbert` are now reviewed anchors for longitudinal EHR representation.
- `alsentzer2019_clinical_bert_embeddings`, `huang2019_clinicalbert_readmission`, `lee2019_biobert`, and `yang2022_gatortron` are now reviewed anchors for clinical text representation.
- `wornow2023_shaky_foundations_ehr_fm` is an indirect peer-reviewed caution that clinical foundation models often lack evaluations tied to health-system usefulness.

### Gaps

- Need deeper source checks of RETAIN, BEHRT, Med-BERT, ClinicalBERT, and GatorTron before using them for detailed architecture or performance claims.
- Need to decide how much temporality is required for the first model.
- Need comparison of interpretable concept features versus raw note embeddings.
- Need a structured baseline that can be compared fairly with text-enhanced models and any longitudinal sequence model.

## 8. Modeling Strategy

### Current State

The strongest current modeling lesson is conservative: start simple, treat architecture as secondary to target/label/timing/validation, and require direct comparison against strong local baselines. A model ladder has been drafted in the study-design template.

The representation distinction is now explicit in the summarizer and has been backfilled for central modeling papers: some methods use fixed-length engineered or concept-feature vectors, while others consume variable-length visit, event, or text sequences and sometimes encode timing.

### Supporting Evidence

- `lu2026_ehr_dementia_prediction_review` found no clear evidence that AI methods solve the field's core limitations by themselves.
- `wang2021_cognitive_decline_notes` shows deep learning can outperform keyword search and conventional models for note-section cognitive decline detection, but XGBoost is a strong baseline.
- `du2024_llm_cognitive_decline_notes` directly supports evaluating LLMs against local models; GPT-4 did not beat locally trained models, while an ensemble improved results.
- `li2024_dementia_risk_notes` supports long-note content selection as a real modeling issue; decision-focused selection outperformed truncation and generic summarization for notes-only dementia risk prediction.
- `wei2025_mci_adrd_phenotyping_ehr` supports a strong simple NLP baseline: TF-IDF note n-grams plus regularized logistic regression can be highly competitive for MCI/ADRD phenotyping.
- `hong2020_cognitive_concerns_nlp` provides lower-publication-weight support that simple term-based NLP may be close to transformer performance in small cognitive-concern datasets.
- `wornow2023_shaky_foundations_ehr_fm` argues that foundation-model claims should be evaluated for sample efficiency, capacity-aware utility, calibration, fairness, usability, and deployment burden rather than benchmark accuracy alone.
- `wornow2023_ehrshot` gives lower-publication-weight benchmark evidence that structured-EHR foundation-model gains are strongest in low-label regimes and can shrink or reverse with more labels or different tasks.
- `adejumo2024_hf_functional_status_nlp` supports a practical supervised ClinicalBERT extraction pattern.
- `khan2026_next_generation_efi` supports interpretable NLP-derived deficit features rather than opaque end-to-end scoring.
- `zhou2025_preoperative_frailty_llm` warns that high model performance can be label-dependent.
- `choi2016_retain`, `li2020_behrt`, and `rasmy2021_medbert` clarify the sequence-model side of the ladder: variable-length structured EHR histories can be represented as visit/code/concept sequences rather than fixed vectors.
- `steinberg2021_ehr_language_models` supports evaluating learned structured-EHR representations against count-based and gradient-boosted baselines rather than assuming end-to-end neural models are better.
- `john2022_dementia_prediction_validation` clarifies the opposite pattern: many externally validated observational-health models use fixed structured predictor sets.

### Gaps

- Need stronger comparison papers for structured baselines versus text-enhanced models in dementia or cognitive impairment.
- Need a decision on whether LLMs are used for concept extraction, weak labeling, summarization, augmentation, adjudication, ensembling, or direct scoring.
- Need to decide whether the first model is fixed-feature, concept-feature, embedding-based, sequence-based, or a staged comparison of these.
- Need model evaluation tied to clinical use, not just AUROC.

## 9. Modeling Strategy Resources

### Current State

This is now separated from the evidence review. The outline points to a dedicated practical resource guide under [ml_resources/](ml_resources/), maintained by the [ML resource curator](agents/ml_resource_curator.md). The initial resource file is:

- `ml_resources/modeling_strategy_resources.md`

This section is for human education and implementation orientation, not manuscript evidence.

### Supporting Resources

- `ml_resources/modeling_strategy_resources.md` currently covers statistical learning, scikit-learn, OHDSI PatientLevelPrediction, XGBoost, LightGBM, NLP basics, Hugging Face, Dive into Deep Learning, PyTorch, interpretability resources, SHAP, InterpretML, and medspaCy.
- `agents/ml_resource_curator.md` defines the workflow for maintaining this section and future resource guides.

### Gaps

- Need a concise clinical NLP resource guide focused on sectioning, negation, temporality, assertion status, annotation, and error analysis.
- Need an Epic-to-OMOP or Epic-to-model-ready data transformation resource guide.
- Need a validation/calibration resource guide aimed at MDs and data managers.

## 10. Validation, Calibration, and Clinical Utility

### Current State

Validation is a major weakness in the literature and must be designed from day one. AUROC alone is not enough. Calibration, threshold performance, temporal/site validation, and clinical utility are central.

### Supporting Evidence

- `lu2026_ehr_dementia_prediction_review` is the primary anchor: external validation and calibration are sparse in EHR dementia prediction.
- `wang2021_cognitive_decline_notes` has strong internal note-classification validation, including a non-keyword-filtered dataset, but no external validation.
- `du2024_llm_cognitive_decline_notes` provides internal LLM/local-model comparison and ensemble testing, but no external validation and potential model-version instability.
- `li2024_dementia_risk_notes` reports internal cross-validation and explicit horizons, but case-control balancing limits real-world PPV and calibration interpretation.
- `wei2025_mci_adrd_phenotyping_ehr` reports chart-review labels, nested cross-validation, bootstrap confidence intervals, and two-site experiments, but lacks calibration, inter-rater reliability, and non-Boston external validation.
- `steinberg2021_ehr_language_models` is indirect but useful for temporal train/development/test splitting and strong baseline comparison in structured-EHR modeling.
- `hong2020_cognitive_concerns_nlp` and `shao2019_probable_dementia_ehr` are useful direct studies but have small/single-system validation limitations.
- `wornow2023_shaky_foundations_ehr_fm` provides a framework for clinical foundation-model evaluation beyond AUROC/AUPRC.
- `wornow2023_ehrshot` provides few-shot benchmark design ideas, while also reinforcing that internal benchmark gains are not clinical utility.
- `osman2024_nlp_ageing_syndromes` shows external validation is also limited in ageing-syndrome NLP.
- `adejumo2024_hf_functional_status_nlp` shows useful multi-site validation within one health system, but not broader external validation.
- `john2022_dementia_prediction_validation` is now reviewed and should be prioritized for source-checking before manuscript use.
- `shen2025_integrating_misclassified_ehr_outcomes` gives indirect methods support for validation samples that estimate EHR outcome misclassification while accounting for non-random validation-sample selection.

### Gaps

- Need deeper source checks for validation details in the papers that become central to the validation section.
- Need to define temporal validation and site/practice validation options for our data.
- Need clinical thresholds tied to cardiology workflow.
- Need decision-curve or net-benefit framing if a score will guide action.
- Need prevalence-aware PPV/NPV expectations for any label derived from future dementia diagnosis or cognitive-care events.

## 11. Data Transformation and Reproducibility

### Current State

This section is underdeveloped but now has better workflow support. The project anticipates an Epic-to-model-ready pipeline and possibly OMOP or another common data model. The new EHR schema/common-data-model specialist reviews clarify that papers often provide model concepts without enough source-system, timestamp, vocabulary, note metadata, or provenance detail for direct implementation.

### Supporting Evidence

- `adejumo2024_hf_functional_status_nlp` is relevant as an Epic-like cardiology-note NLP implementation analogue, but it is not a data-model paper.
- `lu2026_ehr_dementia_prediction_review` supports reproducibility concerns through reporting and implementation gaps.
- `john2022_dementia_prediction_validation` supports OMOP/OHDSI-style reproducibility and external validation, though mainly for fixed structured predictor sets.
- `khan2026_next_generation_efi` supports a structured-plus-text concept-feature pattern that would require local Epic and vocabulary mapping.
- `wang2021_cognitive_decline_notes` supports note sectioning as a concrete preprocessing step for cognitive text modeling.
- `li2024_dementia_risk_notes` supports explicit note lookback windows, chronological concatenation, sentence splitting, deduplication, and long-text content selection.
- `gilmorebykovskyi2018_ci_ehr_phenotype` supports using multidisciplinary notes and flowsheet free text, not only physician notes.
- `wei2025_mci_adrd_phenotyping_ehr` contributes concrete ICD groups, dementia-related medications, note-type categories, and chart-review strata for an MCI/ADRD phenotyping pipeline, while still lacking full Epic/OMOP mapping detail.
- `steinberg2021_ehr_language_models` contributes structured-EHR sequence representation and OHDSI-compatible CLMBR implementation context, but not note or dementia-label pipeline detail.
- `wornow2023_ehrshot` supports the value of standard structured-EHR preprocessing pipelines and notes possible OMOP ingestion, but it excludes clinical text and is not a deployment pipeline for our task.

### Gaps

- Need papers on Epic-to-OMOP or EHR-to-common-data-model translation for prediction modeling.
- Need papers on reproducible clinical-note preprocessing and feature extraction.
- Need to promote EHR schema/common-data-model specialist findings into a concrete Epic-to-model-ready pipeline specification.
- Need a local inventory of note types, section headers, timestamp fields, authorship disciplines, and note-finalization times available before cardiology encounter start.

## 12. Sequential Diagnosis and Future Action Policy

### Current State

This is future framing, not the first model's scope. The first model should score pre-encounter risk and remain compatible with later action-policy work.

### Supporting Evidence

- `aronsson2025_active_feature_acquisition`, `janisch2020_costly_features`, `vivar2020_peri_diagnostic_feature_acquisition`, `poh1996_information_value`, `horvitz1987_beliefs_actions_resources`, and `kaelbling1998_pomdp_survey` are now reviewed anchors.
- The 20260706 synthesis concluded these papers belong later but help frame future "what should the cardiologist do next?" work.

### Gaps

- Need deeper source checks only after the risk-score target and label strategy are better settled.
- Need to avoid drifting into action recommendation before the first model is defined.
- Need a later synthesis that connects risk scores to value-of-information or feature-acquisition policies.

## 13. Synthesis and Proposed Contribution

### Current State

The emerging contribution is not a new architecture by itself. The likely contribution is careful cohort and label construction for pre-cardiology cognitive-risk scoring using longitudinal EHR text, with explicit attention to downstream-action and diagnosis-opportunity bias.

### Current Working Contribution

- Encounter-level prediction anchored at cardiology encounter start.
- Inputs limited to pre-encounter longitudinal EHR data.
- Text-derived cognitive, functional, behavioral, caregiver, adherence, frailty, falls, delirium, social, and navigation concepts, including informal clinician language rather than only diagnosis terms.
- Labels that distinguish cognitive outcome evidence from care-pathway evidence.
- Staged comparison of structured baselines, text-derived concepts, note classifiers/embeddings, and LLM-assisted components rather than assuming end-to-end LLM scoring.
- Validation and calibration designed for clinical workflow.
- Reproducible data transformation path from local EHR data to model-ready features.

### Gaps

- Need to act on the cross-paper synthesis recommendations.
- Need a human decision on target, outcome window, and acceptable label source.

## 14. Open Questions

### Highest-Priority Questions

- What primary target should the first model use?
- Is the target current unmet cognitive care need, future cognitive impairment, or future coded diagnosis?
- What label can be built and validated with available data?
- What post-index events define diagnosis opportunity?
- Should diagnostic-intensity, annual-wellness-visit, primary-care detection, and geographic/access variables be modeled as label-observation mechanisms, sensitivity-analysis strata, or post-index care-pathway descriptors?
- Should future diagnosis labels be stratified by source setting and dementia-code specificity?
- What local validation sample could estimate sensitivity and specificity of EHR cognitive outcomes?
- What note-derived concepts should be extracted first?
- Should cognitive-note evidence before structured diagnosis be treated as an input signal, a label source, or both?

### Method Questions

- Should the first model use all available history or fixed lookback windows?
- Should repeated cardiology encounters per patient be allowed?
- What is the structured baseline?
- What is the first text-enhanced model?
- Should the first model represent history as fixed-length engineered/concept features, variable-length EHR sequences, text embeddings, or a staged comparison?
- Should LLMs be used as standalone scorers, concept extractors, adjudicators, or ensemble members?
- How will calibration and thresholds be evaluated?

### Workflow Questions

- Which consolidated papers need source-level deepening before manuscript drafting?
- Which central papers need exact label and validation extraction from the PDF or supplement?
- Which NLP/concept-extraction specialist findings should be promoted into the first note-concept inventory?
- Which EHR schema/common-data-model findings should be promoted into the Epic-to-model-ready pipeline specification?
- Which ML resource guides should the ML resource curator build next?

## Near-Term Priorities

1. Decide the first candidate target and outcome window with MD input.
2. Use the completed Section 5 reviews to define diagnosis-opportunity variables, outcome-provenance fields, and sensitivity analyses for future diagnosis labels.
3. Build the first cognitive/frailty note-concept inventory using `wang2021_cognitive_decline_notes`, `du2024_llm_cognitive_decline_notes`, `gilmorebykovskyi2018_ci_ehr_phenotype`, `hong2020_cognitive_concerns_nlp`, `wei2025_mci_adrd_phenotyping_ehr`, and `khan2026_next_generation_efi`.
4. Source-check the highest-value papers before manuscript use, especially `lu2026_ehr_dementia_prediction_review`, `wang2021_cognitive_decline_notes`, `li2024_dementia_risk_notes`, `du2024_llm_cognitive_decline_notes`, `wei2025_mci_adrd_phenotyping_ehr`, `john2022_dementia_prediction_validation`, `bynum2024_regional_variation_diagnostic_intensity_dementia`, `tzeng2024_annual_wellness_visits_early_dementia_diagnosis`, `mattke2023_expected_diagnosed_mci_dementia_medicare`, `liu2024_detection_rates_mci_primary_care`, `zhou2025_preoperative_frailty_llm`, `adejumo2024_hf_functional_status_nlp`, `khan2026_next_generation_efi`, and `liang2025_target_trial_emulation`.
5. Use `searcher.md` to find direct cardiology cognitive-screening, referral, and care-gap literature.
6. Decide the first staged modeling comparison: structured baseline, structured plus note concepts, notes-only classifier/embedding, and optional LLM-assisted ensemble.
7. Use `agents/ml_resource_curator.md` to split out focused ML resource guides for clinical NLP, data transformation, and validation/calibration.
