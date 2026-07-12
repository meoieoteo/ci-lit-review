# Specialist Review: NLP Concept Extraction

## Specialist Scope

Keyword, embedding, and UMLS concept feature extraction from medical notes.

## Bottom Line

UMLS concept exposure features were the most useful representation, but cross-institution performance problems limit reuse.

## NLP Task and Clinical Concept Summary

Note feature engineering for dementia prediction rather than span-level concept extraction.

## Note Sources and Text Window

Medical notes in the three years before index, excluding the final year.

## Concept Inventory Relevance

Relevant for dementia risk concepts; exact concepts should be reviewed before adding to inventory.

## Annotation and Reference Standard

No separate manual span-level annotation reference is central in the summary.

## Extraction Method

TF-ICF keyword selection, BERT/ClinicalBERT embeddings, UMLS concept exposure aggregation.

## Context Handling

Misspellings and spelling variants are considered. Negation/temporality handling should be checked.

## Temporality and Leakage

One-year gap reduces immediate diagnostic leakage.

## Evaluation Design

Internal and external institution tests compare representations.

## Error Analysis

External performance degradation suggests local documentation and vocabulary mismatch.

## Portability and Implementation

UMLS helps but does not solve transport.

## Fit to Pre-Cardiology Risk Scoring

Good for note-feature strategy; not cardiology-indexed.

## Strengths

Compares interpretable concept features to embeddings.

## Concerns

No clear context/assertion evaluation in summary.

## Missing Information

Concept list, assertion handling, and error cases.

## Implications for This Literature Review

Use as evidence that concept features may outperform opaque embeddings for dementia notes.

## Recommended Follow-up

Extract concept families if source time allows.
