# Specialist Review: NLP Concept Extraction

## Specialist Scope
Assessment of Med-PaLM for clinical NLP and LLM use in this project.

## Bottom Line
Useful medical LLM background, but not evidence for EHR note concept extraction, cardiology deployment, or dementia-risk scoring.

## NLP Task and Clinical Concept Summary
The task is medical question answering and model alignment on MultiMedQA, not EHR note extraction.

## Note Sources and Text Window
No routine EHR notes.

## Concept Inventory Relevance
Indirect only for LLM capabilities; it does not define clinical-note concepts.

## Annotation and Reference Standard
QA benchmarks and human evaluation, not note annotation.

## Extraction Method
Prompting, chain-of-thought, self-consistency, and instruction prompt tuning.

## Context Handling
Not evaluated for EHR negation, temporality, experiencer, or section handling.

## Temporality and Leakage
Not applicable to pre-index EHR data.

## Evaluation Design
Benchmark QA evaluation; not clinical feature extraction validation.

## Error Analysis
Safety and answer quality concerns are relevant background but not note-concept errors.

## Portability and Implementation
Implementation in protected EHR workflows would require separate validation and governance.

## Fit to Pre-Cardiology Risk Scoring
Low direct fit. It may inform possible LLM augmentation only after concept tasks are defined.

## Strengths
- Medical LLM benchmark and alignment context.

## Concerns
- QA performance does not imply reliable EHR extraction.
- No local clinical-note validation.

## Missing Information
- No Epic note extraction, cognitive annotation, or model-ready feature design.

## Implications for This Literature Review
Use as LLM background, not as support for direct scoring or extraction claims.

## Recommended Follow-up
If LLMs are used, constrain them to audited concept extraction or review support with local validation.
