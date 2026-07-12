# Specialist Review: EHR Schema and Common Data Model

## Specialist Scope

Schema implications of weekly structured/text mental-health prediction.

## Bottom Line

Useful for thinking about rolling person-time prediction records, but not a schema match for cardiology cognitive risk.

## Data Model and Source System Summary

De-identified mental-health EHR data.

## Unit of Analysis and Identifiers

Patient-week prediction records.

## Encounter and Timeline Representation

Weekly time steps with next-28-day outcome.

## Cohort and Eligibility Implementation

Mental-health service population.

## Structured Feature Representation

Hundreds of structured EHR features.

## Note and Text Metadata Representation

Clinical notes converted to BERT semantic vectors.

## Label and Outcome Data Representation

Crisis events linked to future weekly horizons.

## Vocabulary, Code Sets, and Mappings

Not central to dementia schema reuse.

## Missingness, Data Quality, and Provenance

Note availability is explicitly relevant.

## Reproducibility and Portability

Limited outside the source mental-health setting.

## Fit to Epic-to-Model-Ready Pipeline

Useful for representing repeated prediction times.

## Strengths

Clear rolling time origin.

## Concerns

Feature definitions are domain-specific.

## Missing Information

Detailed schema mappings and note metadata.

## Implications for This Literature Review

Supports building repeated encounter/timepoint records with strict horizon definitions.

## Recommended Follow-up

Use only as design analogy.
