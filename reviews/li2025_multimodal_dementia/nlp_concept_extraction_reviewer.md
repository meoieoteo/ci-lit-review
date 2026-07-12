# Specialist Review: NLP Concept Extraction

## Specialist Scope

Long-note modeling and decision-focused content selection for dementia detection.

## Bottom Line

Relevant to handling lengthy notes, but it is more representation learning/content selection than interpretable concept extraction.

## NLP Task and Clinical Concept Summary

Medical-note classification for dementia detection.

## Note Sources and Text Window

Medical notes within specified observation windows before prediction horizon.

## Concept Inventory Relevance

Limited explicit concept inventory; stronger as a long-document modeling precedent.

## Annotation and Reference Standard

Patient-level dementia label rather than note-level concept annotation.

## Extraction Method

Longformer note modeling and decision-focused content selection.

## Context Handling

Transformer representation may learn context, but explicit negation/temporality handling is not the focus.

## Temporality and Leakage

Observation/horizon design helps; exact note cutoffs need source checking.

## Evaluation Design

Nested cross-validation across windows/horizons.

## Error Analysis

Not summarized.

## Portability and Implementation

Long-note strategy is portable but computationally heavier than concept extraction.

## Fit to Pre-Cardiology Risk Scoring

Good for long-note modeling; less useful for clinical concept inventory.

## Strengths

Addresses long clinical notes and multimodal fusion.

## Concerns

Less interpretable than concept features; lower publication weight.

## Missing Information

Which note segments drive predictions.

## Implications for This Literature Review

Supports considering long-document encoders or content selection for pre-encounter notes.

## Recommended Follow-up

Use alongside interpretable concept papers rather than as a replacement.
