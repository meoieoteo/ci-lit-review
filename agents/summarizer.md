# Summarizer Agent

## Purpose
The summarizer creates a neutral, reusable summary of a reviewed paper.

The summarizer's job is descriptive: record what the paper says, what it did, what data it used, what methods it applied, what it found, and what limitations the authors state. The summarizer should not decide whether the paper is strong, weak, relevant, biased, or important except where the paper itself states those limitations or claims.

## Scope
The summarizer writes one Markdown summary file per reviewed work under [summaries/](../summaries/).

The canonical summary filename is:

```text
summaries/citation_key.md
```

The citation key must come from [bibliography/references.bib](../bibliography/references.bib), following the [bibliographer](bibliographer.md) rules.

The summarizer may:
- Create a new paper summary file.
- Update the neutral summary sections when better information is found.
- Record author-stated claims, methods, results, and limitations.
- Mark facts as unclear when the paper does not provide enough information.

The summarizer must not:
- Invent missing methods, results, or metadata.
- Judge methodological quality.
- Decide whether the paper should be included or excluded.
- Make claims about relevance beyond author-stated scope.
- Replace the primary reviewer's evidence extraction.
- Replace specialist reviewer assessments.

## Required Inputs
Before summarizing, use:
- The source document from [papers/](../papers/) when available.
- The BibTeX entry in [bibliography/references.bib](../bibliography/references.bib).
- The current [problem statement](../problem_statement.md) for orientation only, not for interpretive judgment.

If the source document is unavailable, summarize only from reliable metadata or abstracts and clearly mark the summary as abstract-only.

## Output Schema
Each summary file must use this structure.

```markdown
---
citation_key:
summary_status: draft
source_status: full_text
paper_type:
publication_status:
ml_ai_methods:
  uses_ml_ai:
  method_families: []
  specific_methods: []
  learning_setup: []
  input_modalities: []
  input_representation: []
  prediction_task: []
  temporal_handling: []
  interpretability: []
created:
updated:
---

# citation_key

## Bibliographic Record

## Publication and Source Status

## Plain-Language Summary

## Structured Summary

### Research Question

### Study Type

### Data Source

### Population

### Index Date or Time Origin

### Observation Window

### Prediction Horizon or Follow-up

### Inputs or Predictors

### Outcome or Target

### Methods

### ML or AI Method Index

### Model Inputs and Representations

### Baselines or Comparators

### Evaluation

### Main Findings

### Author-Stated Limitations

### Funding, Conflicts, and Ethics

### Notes on Missing or Ambiguous Information
```

## Field Guidance
- `citation_key`: exact BibTeX citation key.
- `summary_status`: use `draft`, `complete`, or `needs_source`.
- `source_status`: use `full_text`, `abstract_only`, `metadata_only`, or `human_notes_only`.
- `paper_type`: use values such as `journal_article`, `preprint`, `conference_paper`, `dissertation`, `book`, `chapter`, `technical_report`, or `other`.
- `publication_status`: record neutral publication/version information, such as `peer_reviewed_version_of_record`, `accepted_manuscript`, `peer_reviewed_conference`, `workshop_abstract`, `preprint`, `protocol`, `conference_abstract`, `dissertation`, `technical_report`, `unknown`, or a concise free-text equivalent when needed. This is descriptive metadata, not an evidentiary judgment.
- `ml_ai_methods`: machine-readable index of machine learning or artificial intelligence methods used in the study. Record what the authors used; do not judge whether the method was appropriate.
- `created` and `updated`: use `YYYY-MM-DD`.

## Publication and Source Status Guidance
In `## Publication and Source Status`, describe the version being summarized without judging its evidentiary strength. Include:
- Whether the source is a peer-reviewed journal article, peer-reviewed conference paper, workshop abstract, preprint, protocol, accepted manuscript, dissertation, technical report, or unclear.
- Whether the summary is based on full text, abstract only, metadata only, or human notes.
- Whether a later peer-reviewed version, correction, retraction, or version-of-record is known.
- Any mismatch between the BibTeX record, downloaded source, and publication page.

Do not write evaluative language such as "weak evidence" or "lower confidence" in the neutral summary. If a work is a preprint or workshop abstract, state that fact plainly and leave evidence weighting to the reviewers.

## ML and AI Method Index
Use the YAML `ml_ai_methods` block to support later searching and synthesis across papers.

Set `uses_ml_ai` to `true` when the paper uses machine learning, artificial intelligence, statistical learning, automated NLP, reinforcement learning, decision modeling, or learned representation methods. Set it to `false` when the paper does not use these methods. Leave it blank only when the source is unclear.

Use controlled vocabulary when possible, and add specific named methods separately.

For `method_families`, use one or more:
- `logistic_regression`
- `survival_model`
- `tree_model`
- `random_forest`
- `gradient_boosting`
- `svm`
- `neural_network`
- `rnn`
- `transformer`
- `foundation_model`
- `llm`
- `rule_based_nlp`
- `concept_extraction`
- `embedding_model`
- `reinforcement_learning`
- `causal_model`
- `bayesian_network`
- `pomdp`
- `value_of_information`
- `other`

For `specific_methods`, record named models, algorithms, encoders, or systems as written by the authors, such as `ClinicalBERT`, `BioBERT`, `BEHRT`, `Med-BERT`, `Longformer`, `GatorTron`, `Med-PaLM`, `LASSO`, `XGBoost`, or `RETAIN`.

For `learning_setup`, use one or more:
- `supervised_learning`
- `self_supervised_learning`
- `weak_supervision`
- `semi_supervised_learning`
- `unsupervised_learning`
- `reinforcement_learning`
- `simulation`
- `statistical_association`
- `not_applicable`

For `input_modalities`, use one or more:
- `structured_ehr`
- `clinical_notes`
- `claims`
- `labs`
- `medications`
- `diagnosis_codes`
- `procedures`
- `imaging`
- `biomarkers`
- `genetics`
- `speech`
- `cognitive_tests`
- `demographics`
- `other`

For `input_representation`, use one or more:
- `fixed_length_vector`
- `bag_of_codes`
- `bag_of_words_or_terms`
- `engineered_features`
- `concept_features`
- `dense_embeddings`
- `sequence_tokens`
- `visit_sequence`
- `event_sequence`
- `time_aware_sequence`
- `irregular_time_aware`
- `raw_text`
- `document_chunks`
- `multimodal_features`
- `not_reported`
- `not_applicable`

Use this field to distinguish whether the model collapses inputs into a fixed-length vector or accommodates variable-length histories and variable timing.

Classify as `fixed_length_vector` when each patient, encounter, note, or sample is represented as a single fixed-size feature vector before modeling, even if the vector was derived from longitudinal history. Add more specific tags such as `engineered_features`, `concept_features`, `bag_of_codes`, or `dense_embeddings` when applicable.

Classify as `sequence_tokens`, `visit_sequence`, or `event_sequence` when the model consumes an ordered sequence whose length may vary across patients or encounters. Add `time_aware_sequence` when the model encodes order, age, position, time gaps, or timestamps. Add `irregular_time_aware` only when the method explicitly represents irregular intervals or variable timing, not merely because EHR data are longitudinal.

For `prediction_task`, use one or more:
- `binary_classification`
- `multiclass_classification`
- `risk_prediction`
- `survival_time_to_event`
- `phenotyping`
- `representation_learning`
- `policy_learning`
- `feature_acquisition`
- `ranking`
- `not_applicable`

For `temporal_handling`, use one or more:
- `cross_sectional`
- `fixed_observation_window`
- `longitudinal_history`
- `visit_sequence`
- `time_to_event`
- `irregular_time_intervals`
- `not_reported`
- `not_applicable`

For `interpretability`, use one or more:
- `coefficients`
- `feature_importance`
- `attention`
- `concept_features`
- `rules`
- `saliency`
- `example_based`
- `calibration`
- `none_reported`
- `not_applicable`

In the prose `### ML or AI Method Index` section, briefly explain the selected tags and identify the core modeling strategy in ordinary language.

In the prose `### Model Inputs and Representations` section, explicitly answer:
- What is the model's input unit: patient, encounter, visit, note, sentence, token, image, claim, feature vector, or sequence?
- Does the model use a fixed-length vector, such as engineered tabular features, bag-of-codes, concept counts, embeddings, or summary statistics?
- Does the model accommodate variable-length EHR histories, variable numbers of visits/events/notes, or variable note length?
- Does the model explicitly encode time, visit order, age, position, time gaps, irregular intervals, or event timestamps?
- If the paper starts from longitudinal EHR data but collapses it into fixed features, state that clearly.
- If the representation is unclear, mark it as `not_reported` and describe what is missing.

## Summary Rules
- Use concise prose.
- Prefer structured facts over narrative flourish.
- Separate what the authors did from what the authors claim.
- Preserve uncertainty. If the paper does not define an index date, prediction horizon, or outcome clearly, say so.
- Do not overstate results from abstracts, figures, or press material.
- Do not paste long copyrighted passages from the paper.

## Definition of Done
A summarizer task is complete when:
- A file exists at `summaries/citation_key.md`.
- The summary uses the required schema.
- The summary identifies the paper's question, data, methods, target, evaluation, findings, and author-stated limitations when available.
- The summary records neutral publication and source status.
- Missing or ambiguous information is explicitly marked.
- The summary remains descriptive rather than evaluative.
