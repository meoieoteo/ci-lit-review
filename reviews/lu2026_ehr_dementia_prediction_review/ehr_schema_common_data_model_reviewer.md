# Specialist Review: EHR Schema and Common Data Model

## Specialist Scope
Assessment of systematic-review evidence on EHR data sources, predictor definitions, reproducibility, and implementation readiness.

## Bottom Line
Core data-model caution: EHR dementia prediction studies often lack enough detail on predictors, time origins, labels, calibration, and validation to support reuse or external implementation.

## Data Model and Source System Summary
The review covers routine EHR sources across many studies, with structured and unstructured predictors.

## Unit of Analysis and Identifiers
Heterogeneous across studies; this heterogeneity is itself a concern for encounter-level model design.

## Encounter and Timeline Representation
Index dates, observation windows, and prediction horizons are often unclear or inconsistently reported in the field.

## Cohort and Eligibility Implementation
Study populations vary widely; cohort construction needs explicit source-population and eligibility rules.

## Structured Feature Representation
Common structured predictors include demographics, conditions, procedures, medications, labs, vital signs, and utilization. Many included models appear to collapse longitudinal history into fixed engineered feature sets, but representation details are often underreported.

## Note and Text Metadata Representation
Clinical text is used in some studies, but note-type and text-feature definitions appear underreported. Text representations include keyword features, engineered NLP features, embeddings, and other heterogeneous approaches rather than one consistent sequence-modeling strategy.

## Label and Outcome Data Representation
Diagnosis-code and documentation-based labels are vulnerable to misclassification and care-pathway effects.

## Vocabulary, Code Sets, and Mappings
The review supports the need for reusable code sets and feature definitions, but does not provide one universal mapping.

## Missingness, Data Quality, and Provenance
Missingness and healthcare utilization may encode care opportunity rather than disease state.

## Reproducibility and Portability
Major field weakness; external validation and reusable reporting are limited.

## Fit to Epic-to-Model-Ready Pipeline
High as a rationale for building a transparent local pipeline with explicit time anchors and feature provenance.

## Strengths
- Direct EHR dementia prediction focus.
- Reporting and validation critique aligns with this project.

## Concerns
- Review-level synthesis cannot substitute for implementation details from individual models.

## Missing Information
- Need source checks for any central quantitative or schema claim.

## Implications for This Literature Review
Use as the primary methodological anchor for data-transformation rigor and reproducibility concerns.

## Recommended Follow-up
Extract a checklist of required pipeline fields: source population, index time, lookback, horizon, predictor domains, label provenance, and validation split.
