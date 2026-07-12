# Primary Review: shen2025_integrating_misclassified_ehr_outcomes

## Review Status

primary_complete

## Citation Key

`shen2025_integrating_misclassified_ehr_outcomes`

## Core Question

Does the paper provide methods for dealing with misclassified EHR outcomes and non-probability validation samples?

## Answer

Yes. The paper is an indirect but useful methods preprint. It develops estimators for treatment-effect analysis when a large EHR cohort has a misclassified binary outcome and a smaller validation sample has a gold-standard outcome but is not a probability sample.

## Relevance to Problem Statement

The problem statement centers on the risk of treating future EHR diagnosis labels as truth. This paper provides a formal statistical frame for one version of that problem: a "silver standard" EHR outcome can have imperfect sensitivity and specificity, and validation samples can be selected in biased ways.

## Evidence Most Relevant to This Review

- The paper explicitly separates a large EHR-derived cohort with a misclassified outcome from a smaller validation sample with a gold-standard outcome.
- It models outcome misclassification and selection into the validation sample.
- Simulations show that ignoring non-probability validation sampling can bias corrected estimates.
- The ACT application compares clinical Alzheimer disease diagnosis with autopsy-defined Alzheimer disease neuropathology.
- In the ACT example, the clinical diagnosis outcome had imperfect sensitivity and specificity relative to autopsy neuropathology.

## Study Design Notes

This is a causal-inference/statistical methods paper, not a dementia prediction paper. The application uses hypertension as the exposure, clinical Alzheimer disease diagnosis as the silver-standard outcome, and autopsy neuropathology as the gold-standard outcome.

## Label and Outcome Implications

The paper supports a two-tier outcome strategy: use large-scale coded or clinical EHR outcomes for coverage, but estimate misclassification using a smaller validation sample when a more credible adjudicated or chart-reviewed outcome is available.

## Downstream-Action and Diagnosis-Opportunity Implications

The paper handles outcome misclassification and validation-sample selection, but it does not directly model diagnosis opportunity as a post-index care pathway. Its relevance is strongest for correcting biased outcome measurement, not for defining care-contact mechanisms.

## Limitations for This Review

- Preprint status means lower publication weight.
- The estimand is a treatment effect, not predictive risk or clinical utility.
- Correctness depends on treatment, outcome, and selection-model assumptions.
- The gold standard in the application is neuropathology, which is related to but not identical with clinical cognitive-care need.
- The paper is not cardiology-specific and does not use EHR text.

## How to Use in the Literature Review

Cite as lower-weight methods support for validation-sample design and misclassified EHR outcome correction. Do not cite it as direct evidence about cardiology cognitive screening, dementia prediction model performance, or EHR text.

## Claims to Carry Forward

- Silver-standard EHR outcomes can be formally corrected when a validation sample with a gold-standard outcome is available.
- Selection into the validation sample matters.
- Clinical Alzheimer disease labels can be imperfect relative to autopsy neuropathology.

## Claims to Treat Cautiously

- Direct translation of the proposed estimators to risk prediction without additional methods work.
- Treating autopsy neuropathology as equivalent to a cardiology-facing cognitive-care label.

## Recommended Follow-Up

Use this paper to motivate a local validation plan with chart review, adjudicated cognitive status, or enriched note review, and document how validation cases are sampled.
