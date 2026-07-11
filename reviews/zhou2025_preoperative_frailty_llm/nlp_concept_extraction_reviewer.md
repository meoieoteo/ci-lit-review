# Specialist Review: NLP Concept Extraction

## Specialist Scope
Assessment of transformer/LLM classifiers for frailty labels from preoperative notes.

## Bottom Line
Important cautionary analogue: transformer performance depends on the label construct, and direct note classification should not be mistaken for interpretable concept extraction.

## NLP Task and Clinical Concept Summary
The task is supervised classification of frailty labels from preoperative anesthesia clinic notes using BERT-family models.

## Note Sources and Text Window
Preoperative anesthesia history and physical notes from a single institution.

## Concept Inventory Relevance
Relevant to `frailty` and possibly `function`, but it does not expose a detailed interpretable concept inventory.

## Annotation and Reference Standard
Labels come from VES-13 questionnaire responses or EHR-derived eFI, which measure different constructs.

## Extraction Method
BERT, RoBERTa, BioBERT, and PubMedBERT classifiers with frozen base weights and trained classification heads.

## Context Handling
The summary does not show explicit handling of negation, temporality, experiencer, or note sections.

## Temporality and Leakage
Preoperative notes precede surgery, but labels may be closely tied to assessment context. Cognitive-risk adaptation would need strict pre-cardiology timing.

## Evaluation Design
Separate train/validation/test splits with AUC, precision-recall, F1, accuracy, sensitivity, specificity, and bootstrapped confidence intervals.

## Error Analysis
The key error-analysis lesson is construct mismatch between VES-13 and eFI labels.

## Portability and Implementation
Single-institution note style and specialty context limit portability.

## Fit to Pre-Cardiology Risk Scoring
Moderate as a label-definition and note-classification caution; lower as a concept-extraction method.

## Strengths
- Direct note-based frailty classification.
- Compares label constructs.

## Concerns
- Opaque classification rather than interpretable concept extraction.
- Label choice changes what the model learns.

## Missing Information
- No detailed note-concept annotation schema.

## Implications for This Literature Review
Use to argue for concept-level features and explicit label constructs before training direct note classifiers.

## Recommended Follow-up
Source-check label construction and performance differences before citing as a central label caution.
