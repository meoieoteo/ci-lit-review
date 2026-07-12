# Specialist Review: NLP Concept Extraction

## Specialist Scope

Assessment of note-based phenotyping and text feature extraction in Wei et al.

## Bottom Line

Wei provides direct evidence that simple note-derived n-gram features can substantially improve MCI/ADRD phenotyping. It is not a deep concept-extraction paper, but its top features are directly relevant to a cognitive note-concept inventory.

## NLP Task and Clinical Concept Summary

The task is patient/visit-level MCI/ADRD phenotype classification from clinical notes plus structured data. Text features are unigrams, bigrams, and trigrams weighted by TF-IDF.

## Note Sources and Text Window

Notes include office visit notes, admission notes, progress notes, discharge notes, and correspondence from all specialties. Notes under 500 words are removed. For patients with MED/ICD records, notes after first MED/ICD evidence are selected.

## Concept Inventory Relevance

Relevant concept families:

- `cognition`
- `behavior_or_neuropsychiatric_symptoms`
- `diagnostic_workup`
- `care_navigation_or_referral`

Top features include "dementia," "cognitive impairment," "Alzheimer," "MCI," "memory," "cognitive," and "decline."

## Annotation and Reference Standard

Manual neurologist chart review provides patient-level labels. There is no span-level or concept-level annotation.

## Extraction Method

Lowercasing, stop-word and special-character removal, lemmatization, n-gram extraction, TF-IDF weighting, and LASSO logistic regression feature selection.

## Context Handling

The method does not explicitly model negation, temporality, uncertainty, experiencer, or section context.

## Temporality and Leakage

Because notes after medication/ICD evidence are used for some patients and chart review is based on notes, this is appropriate for phenotyping documented cases but not for pre-diagnosis prediction.

## Evaluation Design

Evaluation is phenotype classification, not concept extraction. The note-only model achieved AUROC 0.94 and AUPRC 0.94.

## Error Analysis

The paper reports useful qualitative error patterns. False positives often reflected symptoms resembling MCI/ADRD from alternative causes. False negatives often came from specialists outside cognitive care who sparsely documented the diagnosis.

## Portability and Implementation

Simple TF-IDF features are implementable, but terminology, note templates, and specialist documentation practices may vary by institution.

## Fit to Pre-Cardiology Risk Scoring

Useful as evidence that notes contain cognitive phenotype signal. Not directly a pre-cardiology risk model because it uses documentation of known diagnosis.

## Strengths

- Notes-only performance is strong.
- Simple interpretable features.
- Error analysis provides concept-design clues.
- Uses notes from all specialties.

## Concerns

- No assertion/negation handling.
- Explicit diagnosis terms may dominate.
- No span-level annotations.
- No section or temporality modeling.

## Missing Information

Full feature list, note-section behavior, negated mention handling, and selected examples.

## Implications for This Literature Review

Wei supports including simple term and n-gram baselines in the NLP model ladder before LLMs.

## Recommended Follow-up

Promote top feature families into the cognitive note-concept inventory, but separate explicit diagnosis terms from pre-diagnosis cognitive evidence.
