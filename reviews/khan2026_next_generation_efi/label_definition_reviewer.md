# Specialist Review: Label Definition

## Specialist Scope
Assessment of the eFI and note-derived deficit labels as analogues for cognitive/frailty concept construction.

## Bottom Line
`usable_with_caveats`. The paper is useful for interpretable deficit construction, but its labels are frailty-deficit features and outcomes, not validated cognitive-impairment labels.

## Label Summary
The main construct is a 53-item electronic frailty index, including 10 free-text-derived deficits. Outcomes include mortality, severe infection, fracture, and utilization.

## Target Construct
- `frailty_or_functional_status`
- cognitive-adjacent note-derived deficit, not dementia.

## Label Source and Operational Definition
Structured ICD/lab/procedure/medication items plus deep-learning NLP-NER extraction from clinical notes.

## Index Date and Label Timing
Entry year and baseline eFI are used for outcome models; annual eFI values are calculated longitudinally.

## Positive Case Definition
Deficits are binary items; frailty severity derives from deficit accumulation.

## Negative or Control Definition
Absence of a deficit may reflect true absence or lack of documentation/opportunity.

## Indeterminate or Excluded Cases
Not fully resolved in the summary.

## Label Validity Evidence
NLP-NER F1 scores range from 0.74 to 0.92 across free-text deficits. This supports extraction but not necessarily disease-state truth.

## Misclassification Risks
Documentation intensity, care access, language, and note practices may affect free-text deficits.

## Downstream-Action and Diagnosis-Opportunity Bias
Healthcare utilization and recorded deficits are care-process-dependent. Patients with more healthcare contact may have more documented deficits.

## Leakage Risks
For this project, eFI concepts would need timestamps strictly before cardiology encounter start.

## Fit to Pre-Cardiology Risk Scoring
Strong as a concept-feature analogy. Weak as a cognitive outcome label.

## Strengths
- Interpretable concept-feature representation.
- Includes cognitive-adjacent, functional, sensory, social, and assistance deficits.
- Longitudinal EHR construction.

## Concerns
- Preprint status.
- Not dementia-specific.
- Deficit absence may mean missing documentation.
- Non-US setting may limit label portability.

## Missing Information
Detailed NLP-NER annotation and validation methods from supplements are needed before adopting the pipeline.

## Implications for This Literature Review
Supports a note-concept inventory approach, especially for frailty, function, cognition-adjacent deficits, social support, and assistance needs.

## Recommended Follow-up
Extract the exact eFI item list and map candidate deficits to cognitive-risk concepts.
