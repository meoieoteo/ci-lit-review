# Specialist Review: NLP Concept Extraction

## Specialist Scope

Cognitive-function concept extraction from routine clinical notes.

## Bottom Line

This is a directly useful concept-extraction paper because it maps text phrases to cognitive concepts, but model recall is too low for standalone screening.

## NLP Task and Clinical Concept Summary

Phrase extraction and mapping to 42 cognitive-function concepts for MCI identification.

## Note Sources and Text Window

Primary-care clinic notes around cognitive assessment.

## Concept Inventory Relevance

Highly relevant for cognition concepts; less informative for function, frailty, social risk, or caregiver signals.

## Annotation and Reference Standard

10,391 clinic notes were annotated. Cognitive tests define patient status rather than span-level concept truth.

## Extraction Method

Concept extraction followed by LASSO logistic regression.

## Context Handling

Negation, temporality, experiencer, and uncertainty handling should be source-checked before reuse.

## Temporality and Leakage

Notes may contain concerns related to the assessment process.

## Evaluation Design

Patient-level validation with modest AUC and low sensitivity.

## Error Analysis

Low sensitivity indicates many MCI-positive patients are missed.

## Portability and Implementation

Concepts are portable candidates; extraction rules need local adaptation.

## Fit to Pre-Cardiology Risk Scoring

Good for feature inventory; not directly a cardiology risk model.

## Strengths

Interpretable cognitive concepts and full-text annotation.

## Concerns

Low recall and unclear context handling.

## Missing Information

Detailed annotation guidelines and assertion handling.

## Implications for This Literature Review

Carry forward cognitive concept extraction as a direct design precedent.

## Recommended Follow-up

Compare its concept inventory with Wang, Du, Li, and Wei reviews.
