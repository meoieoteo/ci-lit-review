# Specialist Review: NLP Concept Extraction

## Specialist Scope
Assessment of explainable MCI/AD prediction for note-concept extraction relevance.

## Bottom Line
The paper is cognitive-domain relevant but not an EHR note NLP paper; it does not guide extraction of cognitive concepts from cardiology notes.

## NLP Task and Clinical Concept Summary
No NLP concept-extraction task is central.

## Note Sources and Text Window
No routine clinical-note source in the summary.

## Concept Inventory Relevance
Indirect cognitive-domain relevance only.

## Annotation and Reference Standard
ADNI variables and labels, not note annotation.

## Extraction Method
XGBoost with feature selection and SHAP, not text extraction.

## Context Handling
Not applicable.

## Temporality and Leakage
Longitudinal/fixed observation window issues may matter for prediction, but not note leakage.

## Evaluation Design
Structured ADNI model evaluation, not NLP validation.

## Error Analysis
No NLP error analysis.

## Portability and Implementation
Limited portability to EHR text settings because ADNI variables are richer and more standardized than routine care.

## Fit to Pre-Cardiology Risk Scoring
Low for NLP; moderate as caution that cognitive prediction often relies on nonroutine data.

## Strengths
- Cognitive target domain.
- Explainability with SHAP.

## Concerns
- ADNI setting is not routine EHR text.
- No cardiology-note concepts.

## Missing Information
- No note inventory or annotation workflow.

## Implications for This Literature Review
Do not cite for note-concept extraction.

## Recommended Follow-up
Use only for cognitive-prediction context after source checking.
