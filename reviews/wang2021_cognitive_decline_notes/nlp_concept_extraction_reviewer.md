# NLP / Concept Extraction Review: wang2021_cognitive_decline_notes

## Review Status

Complete.

## NLP Task

Section-level classification of whether a clinical note section contains evidence of cognitive decline.

## NLP Methods

The main model uses CNN, RNN, and attention layers with word2vec embeddings trained on a large MCI-note corpus. Baselines use TF-IDF unigram features with logistic regression, random forest, SVM, and XGBoost.

## Concept Handling

The study uses expert-curated keywords to enrich training data and attention weights to identify informative words. It does not rely solely on dictionary matching.

## Strengths

The paper explicitly evaluates a non-keyword-filtered dataset and shows that the model increases PPV over keyword search while maintaining high sensitivity.

## Limitations

The model may still depend on explicit cognitive terminology, and all positives in dataset II contained at least one expert keyword. The approach does not normalize extracted concepts to a standard ontology.

## Use in Review

Use as a strong example of note-section NLP for cognitive-decline evidence and as a caution that keyword-sensitive designs need independent non-keyword-filtered evaluation.
