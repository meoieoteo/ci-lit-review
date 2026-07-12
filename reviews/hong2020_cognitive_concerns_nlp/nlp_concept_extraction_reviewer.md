# NLP / Concept Extraction Review: hong2020_cognitive_concerns_nlp

## Review Status

Complete.

## NLP Task

Patient-level classification of cognitive concern from progress notes.

## NLP Methods

The paper compares regular-expression counts, TF-IDF features, and Longformer sequence classification. Longformer uses sliding windows to handle long text, with patient-level class assignment by aggregation across windows.

## Concept Handling

The regular-expression model uses 15 cognitive-concern categories. TF-IDF identifies correlated terms such as dementia, memory, cognitive, and impairment. The paper does not describe normalization to UMLS/SNOMED concepts or negation/temporality handling.

## Strengths

The comparison across simple lexical methods and a transformer is highly useful. The finding that term-based models nearly match the transformer suggests that transparent NLP features may be strong baselines for cognitive-concern case finding.

## Limitations

The short paper provides limited detail on preprocessing, annotation, section filtering, negation, family-history exclusion, and whether model predictions rely on explicit diagnosis mentions rather than subtler cognitive signals.

## Use in Review

Use to support inclusion of note-derived cognitive concepts and long-document NLP baselines. Treat as insufficient evidence that transformer NLP is necessary or superior for this use case.
