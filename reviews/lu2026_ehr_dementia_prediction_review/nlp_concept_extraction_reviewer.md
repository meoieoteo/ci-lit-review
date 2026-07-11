# Specialist Review: NLP Concept Extraction

## Specialist Scope
Assessment of a systematic review of EHR dementia prediction for EHR text and concept-extraction implications.

## Bottom Line
Core cautionary source: EHR text is underused and promising, but the reviewed field often lacks target clarity, label validity, calibration, and external validation, so NLP features must be interpretable and time-anchored.

## NLP Task and Clinical Concept Summary
The review covers approaches ranging from keyword lists to embeddings and engineered text features from clinical text.

## Note Sources and Text Window
Clinical text sources include clinic letters and progress notes across reviewed studies.

## Concept Inventory Relevance
High as a field-level rationale for `cognition`, `function`, and care-process concepts, but it does not itself define the final inventory.

## Annotation and Reference Standard
The review emphasizes weak and variable outcome/reference standards; source checking is needed for specific NLP studies.

## Extraction Method
Heterogeneous methods including keyword, engineered text, embedding, and likely ML-based approaches.

## Context Handling
The field-level summary suggests reporting is too heterogeneous to assume good context handling.

## Temporality and Leakage
Major concern: text predictors must be separated from outcome-defining documentation and downstream workup.

## Evaluation Design
Review-level evidence, with external validation and calibration gaps across the field.

## Error Analysis
Field-level caution rather than detailed error analysis.

## Portability and Implementation
Strong caution that local text models require external validation and reporting detail.

## Fit to Pre-Cardiology Risk Scoring
High for framing why this project needs stricter target, timing, label, and validation discipline than prior EHR dementia work.

## Strengths
- Direct dementia/EHR prediction scope.
- Covers structured and unstructured EHR data.
- Highlights underuse of text.

## Concerns
- Review-level heterogeneity limits direct method adoption.
- Text use may inherit label and care-pathway bias.

## Missing Information
- Specific text concept inventories and validation details must be extracted from individual source papers.

## Implications for This Literature Review
Use as a central anchor for why interpretable, validated, pre-index note features are needed.

## Recommended Follow-up
Source-check the review's text-using studies to identify direct dementia-note NLP candidates.
