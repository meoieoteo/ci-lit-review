# Specialist Review: EHR Schema and Common Data Model

## Specialist Scope

MIMIC ICU structured time series and notes for multimodal prediction.

## Bottom Line

Useful for time-indexed multimodal representation, but not a common-data-model precedent for outpatient cardiology.

## Data Model and Source System Summary

MIMIC-III ICU data and NOTEEVENTS.

## Unit of Analysis and Identifiers

ICU visit/admission sample.

## Encounter and Timeline Representation

First 48 hours after ICU admission.

## Cohort and Eligibility Implementation

Visits with available notes.

## Structured Feature Representation

17 clinical variables represented as time series.

## Note and Text Metadata Representation

Notes are embedded by hour; exact note-type handling should be checked.

## Label and Outcome Data Representation

In-hospital mortality.

## Vocabulary, Code Sets, and Mappings

Not central.

## Missingness, Data Quality, and Provenance

Note absence excludes patients.

## Reproducibility and Portability

MIMIC-based reproducibility is good; clinical portability is limited.

## Fit to Epic-to-Model-Ready Pipeline

Low for Epic cardiology; moderate for time-series/text fusion mechanics.

## Strengths

Explicit 48-hour observation window.

## Concerns

ICU-specific time origin and note workflows.

## Missing Information

Detailed note metadata and missingness effects.

## Implications for This Literature Review

Time-window discipline and multimodal joins are the reusable lessons.

## Recommended Follow-up

Use as architecture context only.
