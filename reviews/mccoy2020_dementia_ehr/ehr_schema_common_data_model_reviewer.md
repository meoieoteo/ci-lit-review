# Specialist Review: EHR Schema and Common Data Model

## Specialist Scope

EHR representation of discharge notes, index hospitalization, covariates, and future dementia codes.

## Bottom Line

The cohort timeline is clear, but schema details are not enough to reproduce in an Epic outpatient cardiology pipeline.

## Data Model and Source System Summary

Two academic medical-center EHR systems.

## Unit of Analysis and Identifiers

Patient-level analysis anchored to one selected hospitalization.

## Encounter and Timeline Representation

Index hospitalization/discharge and post-discharge follow-up are explicit.

## Cohort and Eligibility Implementation

Adult inpatient discharges excluding prior/current dementia codes.

## Structured Feature Representation

Age, sex, race, Charlson comorbidity, and diagnosis outcomes.

## Note and Text Metadata Representation

Discharge notes are the text source; outpatient note classes are not addressed.

## Label and Outcome Data Representation

Future dementia diagnosis codes in inpatient/outpatient encounters.

## Vocabulary, Code Sets, and Mappings

Cognitive symptom term list is the reusable vocabulary element.

## Missingness, Data Quality, and Provenance

Hospitalized population and discharge-note availability shape provenance.

## Reproducibility and Portability

Moderate for hospital discharge workflows; limited for cardiology encounters.

## Fit to Epic-to-Model-Ready Pipeline

Useful for defining index/follow-up logic, not for direct cardiology schema.

## Strengths

Clear index encounter and follow-up outcome timing.

## Concerns

Limited detail on note metadata and code-set implementation.

## Missing Information

Exact code lists, note extraction fields, and copied-forward handling.

## Implications for This Literature Review

Separating index encounter, text source, and future diagnosis date is essential.

## Recommended Follow-up

Use as a timeline design example for future-code outcomes.
