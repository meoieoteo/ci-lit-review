# Specialist Review: NLP Concept Extraction

## Specialist Scope
Assessment of a dementia prediction validation paper for text/concept-extraction implications.

## Bottom Line
The paper is not primarily an NLP paper, but it strongly cautions that text or concept extraction is unusable for external validation unless feature definitions and model specifications are fully reported.

## NLP Task and Clinical Concept Summary
No EHR note extraction task is central. The validated models use routinely collected structured observational health data.

## Note Sources and Text Window
No clinical-note source is central in the summary.

## Concept Inventory Relevance
Indirect: any note-derived concepts should be specified as reusable predictors if external validation is expected.

## Annotation and Reference Standard
Not applicable to note annotation.

## Extraction Method
No text extraction method.

## Context Handling
Not applicable.

## Temporality and Leakage
The paper's reporting criteria reinforce the need to specify observation windows and prediction horizons for any note-derived features.

## Evaluation Design
External validation through OHDSI patient-level prediction infrastructure is the main strength.

## Error Analysis
Not a concept-extraction error analysis.

## Portability and Implementation
High relevance to model specification and portability, even without NLP.

## Fit to Pre-Cardiology Risk Scoring
Important caution for pre-cardiology risk scoring: text features must be defined well enough to validate externally.

## Strengths
- Direct focus on external-validatability of dementia prediction models.

## Concerns
- Does not provide note-derived cognitive concepts.

## Missing Information
- No NLP implementation.

## Implications for This Literature Review
Use to argue that NLP features need reusable definitions, not just local model outputs.

## Recommended Follow-up
When designing note features, document them at the level needed for OHDSI-style external validation.
