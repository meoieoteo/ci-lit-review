# Specialist Review: EHR Dementia Prediction Quality

## Specialist Scope

EHR text model for identifying MCI using cognitive-test labels.

## Bottom Line

Directly relevant as a pilot cognitive-impairment text model, but not clinically mature because discrimination is modest and sensitivity is very low at the reported high-specificity threshold.

## Prediction Task Clarity

The task is current MCI identification, not future dementia prediction.

## Index Date, Observation Window, and Prediction Horizon

Index is tied to cognitive assessment. The paper is not a cardiology-encounter risk-score design.

## Data Source and Cohort Definition

Kaiser Permanente Washington primary-care notes linked to ACT and general-population cognitive assessments.

## Outcome and Reference Standard

Cognitive test threshold is stronger than diagnosis codes but still imperfect and selectively observed.

## Comparator or Control Group

Controls are patients with assessment scores above threshold.

## EHR Text and Structured Data Use

Uses note-derived cognitive concepts, with demographics as comparator.

## Missing Data and Feature Availability

Cognitive testing availability is a major selection issue.

## Validation

Held-out general-population validation is reported; no external validation.

## Calibration, Thresholds, and Clinical Utility

Threshold results imply rule-in utility only; broad screening utility is poor.

## Reporting and Reproducibility

Concept inventory supports reproducibility, but local NLP implementation would need validation.

## Care-Pathway and Downstream-Action Bias

Testing and documentation are likely triggered by cognitive concern.

## Implementation Readiness

Not ready for deployment.

## Strengths

Direct note concepts, cognitive-test label, held-out validation.

## Concerns

Low sensitivity, no external validation, selective testing.

## Missing Information

Calibration and external transport.

## Implications for This Literature Review

Useful feasibility evidence and a caution against equating high specificity with useful screening.

## Recommended Follow-up

Use as direct but limited MCI note-concept evidence.
