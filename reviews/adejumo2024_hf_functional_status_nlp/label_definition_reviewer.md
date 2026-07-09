# Specialist Review: Label Definition

## Specialist Scope
Assessment of the paper's NYHA and symptom labels as an analogue for cognitive or functional-state extraction from cardiology notes.

## Bottom Line
`usable_with_caveats`. The labels are clear for documented heart-failure functional status, but they validate documentation content rather than an independent patient-state outcome.

## Label Summary
The paper labels outpatient cardiology notes for explicit NYHA class and activity/rest-related heart-failure symptoms.

## Target Construct
- `other`: documented current heart-failure functional status.

This is not a dementia or cognitive-impairment label. Its value is as a documentation-extraction analogue.

## Label Source and Operational Definition
Expert-annotated note labels, focused on HPI and assessment/plan sections after MedSpaCy sectioning. NYHA II and III were combined in some analyses because of documentation ambiguity and guideline relevance.

## Index Date and Label Timing
The unit is the outpatient encounter note. The task is current-state extraction from documentation, not future prediction.

## Positive Case Definition
Positive labels correspond to annotated NYHA class mentions or symptom descriptions consistent with activity/rest limitation.

## Negative or Control Definition
Negatives are notes without the annotated target class/symptom category. This is appropriate for extraction but does not establish absence of true functional limitation.

## Indeterminate or Excluded Cases
Ambiguous symptom attribution is a known issue, especially where comorbidities could explain functional limitation.

## Label Validity Evidence
The study uses expert annotation and multi-site validation within one health system. This is strong for note-content extraction.

## Misclassification Risks
Misclassification can arise from local documentation style, clinician habit, comorbidity-related ambiguity, and class II/III wording.

## Downstream-Action and Diagnosis-Opportunity Bias
The extracted label reflects what clinicians documented. It may be influenced by visit type, care intensity, specialty practice, and documentation norms.

## Leakage Risks
Leakage is not a major concern for the extraction task. For this project, the lesson is that any cognitive-note extraction must keep note timing strictly before the cardiology encounter if used as a predictor.

## Fit to Pre-Cardiology Risk Scoring
Indirect but useful. It supports annotation-based extraction of patient-state concepts from cardiology notes, not cognitive-risk labeling.

## Strengths
- Clear note-level target.
- Expert annotation.
- Practical sectioning strategy.
- Multi-site validation within a cardiology health-system context.

## Concerns
- Label is documentation-dependent.
- Not cognitive impairment.
- Does not address future outcomes or downstream-action bias.

## Missing Information
More inter-annotator agreement and cross-health-system transfer evidence would strengthen label confidence.

## Implications for This Literature Review
Use as an analogue for extracting interpretable clinical concepts from cardiology notes. Do not cite it as evidence for cognitive labels.

## Recommended Follow-up
If adapting this pattern, define cognitive/functional note concepts with local clinician annotation and separate documented concern from true impairment.
