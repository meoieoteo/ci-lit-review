# Specialist Review: EHR Dementia Prediction Quality

## Specialist Scope
Applicable as a review of EHR-text identification of ageing syndromes, including dementia. It is not itself a model-development paper.

## Bottom Line
background_only

## Prediction Task Clarity
Adequate for the review scope. The authors focus on identification of existing ageing syndromes and explicitly exclude future-onset prediction. For this project, that means it informs current cognitive-impairment detection more than future risk.

## Index Date, Observation Window, and Prediction Horizon
Not applicable at the review level. Included studies varied, and the review does not establish a common index date or prediction horizon.

## Data Source and Cohort Definition
Partial. The review includes varied EHR settings and syndromes. This breadth is useful for landscape mapping but limits direct transfer to a cardiology pre-encounter cohort.

## Outcome and Reference Standard
Partial. Manual text review is common among included studies, but reference standards vary. Dementia-specific reference-standard quality needs paper-level extraction from the included dementia studies.

## Comparator or Control Group
Partial. The review reports diagnostic-accuracy studies rather than a unified dementia case/control design. Lu-style control contamination concerns would need to be assessed in individual dementia papers.

## EHR Text and Structured Data Use
Adequate. The paper is directly about NLP applied to EHR text, with multiple note types represented.

## Missing Data and Feature Availability
Weak. Missingness and feature availability are not central review themes.

## Validation
Weak as a literature signal. Only four of 22 studies included external validation, which reinforces Lu's warning that EHR model performance often lacks transportability evidence.

## Calibration, Thresholds, and Clinical Utility
Weak. Diagnostic accuracy is summarized, but calibration, threshold selection, and action-linked utility are not a central focus.

## Reporting and Reproducibility
Partial. The use of PRISMA, PROSPERO registration, QUADAS-2, and SWiM is a strength. The included primary studies have variable reporting quality and no standard NLP taxonomy.

## Care-Pathway and Downstream-Action Bias
Weak. The review does not substantially evaluate how referral, documentation, coding, and diagnostic opportunity affect labels.

## Implementation Readiness
Background only. The review supports feasibility and identifies quality concerns, but implementation requires condition-specific model and validation evidence.

## Strengths
- Directly addresses NLP identification of ageing syndromes in EHRs.
- Includes dementia among target syndromes.
- Uses structured review methods and quality assessment.
- Clearly highlights external-validation scarcity.

## Concerns
- Broad syndrome scope dilutes dementia-specific conclusions.
- Excludes future-onset prediction.
- Heterogeneity prevents meta-analysis.
- Included-study reporting and validation quality are uneven.

## Missing Information
For this project, the dementia-specific included studies should be extracted separately, including note source, reference standard, index timing, and external validation.

## Implications for This Literature Review
This paper supports a background claim: EHR-note NLP for geriatric syndrome detection is feasible, but the field has validation and reporting weaknesses. It does not resolve the cognitive-risk-label problem.

## Recommended Follow-up
Identify and retrieve the dementia-specific primary studies included in the review if they overlap with this project's target.
