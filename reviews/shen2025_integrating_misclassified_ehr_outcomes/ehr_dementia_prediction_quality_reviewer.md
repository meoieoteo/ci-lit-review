# EHR Dementia Prediction Quality Review: shen2025_integrating_misclassified_ehr_outcomes

## Review Status

specialist_complete

## Prediction Study Status

This is not an EHR dementia prediction model. It is a statistical methods paper about estimating treatment effects with misclassified EHR outcomes and biased validation samples.

## Target and Timing

The ACT application studies hypertension and Alzheimer disease neuropathology. It does not define an encounter-level prediction time, observation window, or dementia diagnosis prediction horizon.

## Relevance to Prediction Quality

The paper is relevant to outcome validation. Predictive performance estimates can be misleading if the outcome is a misclassified clinical or EHR diagnosis label and if the validation sample is selected in a non-representative way.

## Strengths

- Provides formal language for silver-standard and gold-standard outcomes.
- Shows why naive analyses can be biased when validation samples are not probability samples.
- Gives an Alzheimer disease application.

## Weaknesses

- No AUROC, calibration, decision-curve analysis, or transportability evaluation for a prediction model.
- Does not handle longitudinal EHR feature representation.
- Does not define a clinically actionable dementia-risk target.

## Study-Design Implications

A local prediction study should predefine which outcome is silver standard, what validation outcome is feasible, how validation cases are selected, and how outcome misclassification affects calibration and clinical utility.

## Recommended Use

Use as a methods caution in Sections 4, 5, and 10. Do not cite as direct prediction-performance evidence.
