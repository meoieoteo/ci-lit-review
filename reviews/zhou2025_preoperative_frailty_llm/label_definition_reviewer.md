# Specialist Review: Label Definition

## Specialist Scope
Assessment of VES-13 and eFI frailty labels as a warning for proxy labels in EHR text models.

## Bottom Line
`label_construct_clear`. This paper is most valuable because it shows that label source can define what the model learns.

## Label Summary
Binary preoperative frailty using either VES-13 score >= 3 or eFI score >= 0.3.

## Target Construct
- `frailty_or_functional_status`

The construct is not dementia, but the label-source issue is directly analogous to cognitive-risk labels.

## Label Source and Operational Definition
VES-13 is a patient questionnaire. eFI is an EHR-derived index incorporating comorbidities, functional status, labs, and physical exam findings.

## Index Date and Label Timing
The input is the preoperative anesthesia clinic note. The task is current frailty classification, not future prediction.

## Positive Case Definition
VES-13 score >= 3 or eFI score >= 0.3.

## Negative or Control Definition
Below-threshold VES-13 or eFI score.

## Indeterminate or Excluded Cases
Not central in the summary.

## Label Validity Evidence
The strongest evidence is cross-label testing. VES-13-trained models transferred better to eFI labels than eFI-trained models transferred to VES-13 labels.

## Misclassification Risks
eFI may reflect coding, labs, documentation, and care processes more than the same patient-reported construct captured by VES-13.

## Downstream-Action and Diagnosis-Opportunity Bias
Not directly addressed, but eFI labels are EHR-derived and therefore vulnerable to documentation and testing opportunity.

## Leakage Risks
The paper is current-note classification. For this project, the analogous risk is using post-index cognitive evidence as if it were pre-index signal.

## Fit to Pre-Cardiology Risk Scoring
Strong as a label-methodology warning. It supports comparing candidate cognitive labels rather than assuming codes, tests, referrals, and chart review mean the same thing.

## Strengths
- Explicit cross-label validation.
- Clear operational thresholds.
- Shows construct mismatch despite same broad label name.

## Concerns
- Frailty, not dementia.
- Single-center surgical population.
- No external validation.

## Missing Information
Calibration, subgroup label behavior, and broader frailty reference-standard discussion.

## Implications for This Literature Review
This is one of the best analogies for why cognitive-risk target definition must precede modeling.

## Recommended Follow-up
Design cross-label checks for diagnosis-code, cognitive-test, referral, and chart-review cognitive labels.
