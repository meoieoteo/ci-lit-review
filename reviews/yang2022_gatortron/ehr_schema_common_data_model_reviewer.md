# Specialist Review: EHR Schema and Common Data Model

## Specialist Scope
Assessment of GatorTron for EHR data representation and portability.

## Bottom Line
Moderate text-source relevance but limited schema guidance. The paper uses a large clinical-note repository, not a reproducible Epic-to-model-ready pipeline for this project.

## Data Model and Source System Summary
UF Health Integrated Data Repository clinical notes plus additional text sources.

## Unit of Analysis and Identifiers
Text examples for NLP benchmarks, not cardiology encounters.

## Encounter and Timeline Representation
No reusable pre-cardiology encounter timeline.

## Cohort and Eligibility Implementation
Not a cardiology cohort construction paper.

## Structured Feature Representation
Structured EHR features are not central.

## Note and Text Metadata Representation
Clinical note corpus is central, but detailed note-type and timestamp implementation are not the main contribution.

## Label and Outcome Data Representation
Benchmark NLP labels, not dementia-risk outcomes.

## Vocabulary, Code Sets, and Mappings
No CDM vocabulary mapping.

## Missingness, Data Quality, and Provenance
De-identification and corpus composition matter, but operational data quality is not the focus.

## Reproducibility and Portability
Model-level portability depends on access and infrastructure; extraction portability is not established.

## Fit to Epic-to-Model-Ready Pipeline
Low to moderate for text model selection; low for data transformation.

## Strengths
- Large clinical-note corpus.

## Concerns
- Local note corpus and compute dependencies.
- No encounter-level feature provenance.

## Missing Information
- Epic/OMOP mapping and note metadata details.

## Implications for This Literature Review
Use as clinical LLM background, not a pipeline model.

## Recommended Follow-up
Prioritize local data representation and validation before model scale.
