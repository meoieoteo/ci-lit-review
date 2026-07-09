# Specialist Review: Label Definition

## Specialist Scope
Assessment of Lu et al. 2026 for dementia label definition, target construct, timing, leakage, and diagnosis-opportunity concerns.

## Bottom Line
`high_misclassification_risk`. The review shows that dementia prediction labels in EHR studies are often weakly aligned with the intended clinical construct.

## Label Summary
Included studies use heterogeneous dementia labels: diagnosis codes, medication codes, rule-based definitions, specialist clinic codes, manual chart review, ML-derived labels, and established diagnostic criteria.

## Target Construct
- `current_undocumented_cognitive_impairment`
- `future_coded_dementia_diagnosis`
- `prevalent_known_dementia`
- `future_cognitive_impairment`

The problem is that many papers do not distinguish these constructs.

## Label Source and Operational Definition
Heterogeneous and often underreported. Only a small minority of models used established clinical diagnostic criteria.

## Index Date and Label Timing
Often unclear across included studies. This makes leakage and target interpretation difficult to assess.

## Positive Case Definition
Varies by study; frequently based on recorded diagnosis or related proxies.

## Negative or Control Definition
Major concern. Absence of a dementia code can mean unrecognized or undocumented dementia.

## Indeterminate or Excluded Cases
Often not clearly handled in published reports.

## Label Validity Evidence
Weak across much of the literature. PROBAST outcome-domain problems are a central finding.

## Misclassification Risks
High, especially when diagnosis codes are treated as ground truth.

## Downstream-Action and Diagnosis-Opportunity Bias
Strong concern. Dementia labels can depend on recognition, referral, specialist access, cognitive testing, documentation, and coding.

## Leakage Risks
Cannot be ruled out when index date and predictor windows are unclear.

## Fit to Pre-Cardiology Risk Scoring
High as a design warning. It supports defining the project's target before model development.

## Strengths
- Directly identifies outcome-definition ambiguity.
- Separates diagnostic and prognostic use cases.
- Highlights weak reference standards.

## Concerns
- Does not prescribe a new label.
- Cannot resolve underreporting in primary studies.

## Missing Information
Model-level label algorithms in supplements should be reviewed for candidate methods.

## Implications for This Literature Review
This paper justifies a dedicated label-definition section and label-definition reviewer.

## Recommended Follow-up
Use its categories to audit every candidate dementia-label paper.
