# Specialist Review: NLP Concept Extraction

## Specialist Scope

Transformer classification of cognitive impairment evidence in note snippets.

## Bottom Line

Strong short-form evidence that ClinicalBERT can identify explicit cognitive impairment evidence, but it is not an interpretable concept inventory.

## NLP Task and Clinical Concept Summary

Classifies 800-character snippets as Yes/No/Neither for cognitive impairment evidence.

## Note Sources and Text Window

Clinician notes with dementia-related keyword windows.

## Concept Inventory Relevance

Relevant to cognition evidence and distinction between concern and impairment.

## Annotation and Reference Standard

Human annotation of snippets; full reliability details limited.

## Extraction Method

TF-IDF L1 logistic regression and fine-tuned ClinicalBERT.

## Context Handling

ClinicalBERT may capture context; explicit assertion/temporality rules are not central.

## Temporality and Leakage

No future prediction task; text and label are same snippet.

## Evaluation Design

Internal holdout sequence classification.

## Error Analysis

Limited in the short source.

## Portability and Implementation

Needs local notes and annotation for transport.

## Fit to Pre-Cardiology Risk Scoring

Useful as a component for extracting current cognitive evidence before an encounter.

## Strengths

High reported AUC and clear baseline comparison.

## Concerns

Keyword enrichment and sequence-level evaluation.

## Missing Information

Detailed guidelines, reliability, and patient-level aggregation.

## Implications for This Literature Review

Supports transformer-based cognitive evidence extraction from notes.

## Recommended Follow-up

Do not use as a standalone risk-score precedent.
