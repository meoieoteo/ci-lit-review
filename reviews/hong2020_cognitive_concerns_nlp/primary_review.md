# Primary Review: hong2020_cognitive_concerns_nlp

## Review Status

Complete.

## Review-Relevant Contribution

Hong et al. provide direct evidence that progress-note NLP can detect cognitive concerns in older patients better than structured dementia-related codes and medications alone.

## Publication Status and Evidence Weight

Publication status: workshop abstract / arXiv preprint. Evidence weight: direct but low-to-moderate because the work is short, small, and lacks detailed validation reporting.

## Fit to Problem Statement

Fit is strong for the dementia/cognitive-risk and EHR-note portions of the problem statement. Fit is weak for cardiology-specific timing, pre-encounter actionability, target-trial design, and implementation evaluation.

## Evidence Category

Direct but lower publication weight.

## Clinical Target

Broad cognitive concerns, including subjective cognitive concern, MCI, and dementia. The target is detection of existing concern in EHR records, not prospective prediction before a cardiology encounter.

## Data and Cohort Relevance

The cohort comes from Mass General Brigham and uses EHR data from a one-year window in 2018. Patients are older adults, with mean age around 80-81 years in train/test. This is clinically relevant, but single-system and small.

## EHR Text Relevance

Highly relevant. The paper directly evaluates progress notes and shows that note-based approaches improve sensitivity over structured features.

## Label or Outcome Relevance

The label is clinician-adjudicated cognitive concern, which is valuable because it is not only ICD-code based. However, the label combines subjective concern, MCI, and dementia, and the annotation procedure is not reported in enough detail for high confidence.

## Modeling Relevance

The model comparison is useful: structured logistic regression, regular-expression counts, TF-IDF, and Longformer. The central modeling lesson is that simple lexical note models already recover much of the gain, while the transformer is best but only marginally better in this small dataset.

## Validation and Utility Signals

The study reports a held-out test set and conventional discrimination/classification metrics. It does not provide external validation, calibration, clinical utility, threshold-decision analysis, or workflow evaluation.

## Bias/Causality/Downstream Action Issues

No causal design. The label and notes may encode clinician attention, documentation intensity, access to specialty care, and coding practices. Downstream actions are proposed as future work through active learning and review of edge cases.

## Portability/Implementation Signals

Portability is uncertain. The work is tied to MGB notes and local clinician labels. Regular-expression and TF-IDF approaches may be easier to inspect and port than Longformer, but likely require local validation and terminology adaptation.

## Key Extracted Claims

- Cognitive concerns are often present in unstructured clinician notes rather than structured claims or diagnosis data.
- A structured medication/ICD baseline had AUC 0.79 and sensitivity 0.59.
- Note-based models improved AUC to 0.88-0.93.
- The best model was Longformer, but term-based NLP performed close to it.
- Structured features missed patients with subjective concern, MCI, and dementia.

## What This Paper Supports

Use this paper to support the claim that dementia/cognitive-concern case finding benefits from clinical notes and that structured-code-only methods can miss relevant patients.

## What This Paper Does Not Support

Do not cite it as strong evidence for deployable dementia prediction, cardiology-specific cognitive-risk screening, external validity, calibrated risk prediction, or treatment/action benefit.

## Default Specialist Reviews Called

All default specialist reviewers completed.

## Additional Specialist Reviews Needed

None required.

## Primary Reviewer Notes

The paper is useful because it is directly on cognitive concerns in notes. Its short format and small test set should be made visible whenever it is used in synthesis.
