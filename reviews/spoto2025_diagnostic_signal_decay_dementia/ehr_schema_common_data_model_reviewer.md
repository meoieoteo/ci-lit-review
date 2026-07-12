# EHR Schema and Common Data Model Review: spoto2025_diagnostic_signal_decay_dementia

## Review Status

specialist_complete

## Data Model Relevance

The paper uses Medicare inpatient claims, not a local EHR schema or common data model. Still, it highlights variables a local EHR-to-model pipeline should preserve when dementia diagnosis codes become labels or features.

## Useful Data Elements

- Diagnosis code and code family.
- Diagnosis setting, especially inpatient versus outpatient.
- Hospitalization date and sequence.
- Geographic context.
- Patient demographic and insurance-related context.
- Repeated diagnosis-code transitions over time.

## Schema Implications for This Project

For local Epic or OMOP-style extraction, dementia diagnoses should retain:

- source table and encounter type;
- diagnosis timestamp or encounter date;
- problem-list versus billing diagnosis origin, if available;
- ICD/SNOMED concept identity and mapped dementia category;
- first-observed and subsequent-observed code specificity;
- care setting in which the code appeared.

## Limitations

The paper does not provide implementation guidance for OMOP, Epic, note metadata, or feature generation. It is a conceptual warning for data provenance rather than a data transformation manual.

## Recommended Use

Promote its schema implications into the outcome-label data dictionary, especially code specificity and source-setting provenance.
