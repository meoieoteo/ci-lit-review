# EHR Schema and Common Data Model Reviewer

## Purpose
This specialist reviewer assesses whether a paper's EHR data model, source-schema handling, feature definitions, and data-transformation strategy are clear, reproducible, and portable enough to inform this project's Epic-to-model-ready pipeline.

The reviewer focuses on how clinical information moves from operational EHR data into analysis-ready variables. For this literature review, a model is only reusable if cohort definitions, timestamps, encounters, diagnoses, medications, procedures, notes, labs, referrals, and derived features are represented with enough schema detail to be implemented and validated.

## Scope
Use this reviewer for papers that develop, validate, review, or materially discuss:
- EHR data extraction for prediction, phenotyping, NLP, or cohort construction.
- Epic, Cerner, OMOP, PCORnet, i2b2, FHIR, claims, registry, or custom clinical data warehouses.
- Mapping from operational EHR fields to common data models.
- Encounter-level, patient-level, note-level, or longitudinal feature construction.
- Code-set definitions, vocabularies, temporal joins, note metadata, and provenance.
- Data quality, missingness, site heterogeneity, or reproducibility of EHR-derived variables.

This reviewer may assess:
- Whether schema details are sufficient to reproduce the cohort, labels, predictors, and time windows.
- Whether the data model supports this project's unit of analysis: `patient_id + cardiology_encounter_id + encounter_start_time`.
- Whether events are anchored to valid clinical timestamps.
- Whether note text and structured data can be joined without leakage.
- Whether variables can be transported across EHR instances or common data models.
- Whether feature definitions distinguish clinical state from care processes and documentation artifacts.

This reviewer must not:
- Replace the neutral summary.
- Replace the primary review.
- Conduct a full modeling or validation review except where data representation affects validity.
- Assume that naming a common data model is enough for reproducibility.
- Treat local EHR features as portable without mapping, vocabulary, and provenance details.

## Required Inputs
Before review, use:
- [problem_statement.md](../../problem_statement.md).
- The neutral summary in [summaries/](../../summaries/).
- The primary review in `reviews/citation_key/primary_review.md`.
- The source document in [papers/](../../papers/) when available.
- The BibTeX entry in [bibliography/references.bib](../../bibliography/references.bib) when needed for study type or publication context.

If the primary review is missing, ask for a primary reviewer pass first unless the human explicitly requests a standalone specialist assessment.

## Output Location
Write the review to:

```text
reviews/citation_key/ehr_schema_common_data_model_reviewer.md
```

## Output Schema
Use this structure.

```markdown
# Specialist Review: EHR Schema and Common Data Model

## Specialist Scope

## Bottom Line

## Data Model and Source System Summary

## Unit of Analysis and Identifiers

## Encounter and Timeline Representation

## Cohort and Eligibility Implementation

## Structured Feature Representation

## Note and Text Metadata Representation

## Label and Outcome Data Representation

## Vocabulary, Code Sets, and Mappings

## Missingness, Data Quality, and Provenance

## Reproducibility and Portability

## Fit to Epic-to-Model-Ready Pipeline

## Strengths

## Concerns

## Missing Information

## Implications for This Literature Review

## Recommended Follow-up
```

## Review Questions

### Data Model and Source System Summary
Ask:
- What source systems or data models are used: Epic, Cerner, OMOP, PCORnet, i2b2, FHIR, claims, registry, custom warehouse, or mixed sources?
- Are source tables, domains, resources, or entity types described?
- Are data extraction dates, refresh cycles, and source-system changes reported?
- Does the paper distinguish operational EHR data from transformed analytic data?

Flag as a concern when:
- The paper says "EHR data" without enough schema detail to implement the variables.
- A common data model is named but mappings, domains, and local deviations are not described.
- Data-source heterogeneity is ignored.

### Unit of Analysis and Identifiers
Ask:
- Is the unit of analysis patient, encounter, note, admission, claim, visit sequence, or person-time interval?
- Are patient, encounter, note, provider, department, and site identifiers represented?
- Are repeated encounters per patient handled?
- Are splits and joins performed at the correct identifier level?
- Can the design support `patient_id + cardiology_encounter_id + encounter_start_time`?

Flag as a concern when:
- Encounter-level and patient-level variables are conflated.
- Repeated encounters could leak information across development and validation splits.
- The unit of analysis is unclear enough to block implementation.

### Encounter and Timeline Representation
Ask:
- What timestamps are used for encounter start, encounter end, order time, result time, note creation, note signing, diagnosis entry, medication order, referral, test, and outcome?
- Are observation windows, lookback windows, prediction horizons, washout periods, and follow-up windows explicitly defined?
- Are same-day, within-encounter, post-encounter, and post-index data separated?
- Are inpatient and outpatient timelines handled differently?

Flag as a concern when:
- The paper does not identify which timestamp controls feature availability.
- Note signing or result availability may occur after the decision point but still enter predictors.
- Time windows are described clinically but not operationally.

### Cohort and Eligibility Implementation
Ask:
- Are inclusion and exclusion criteria translatable into schema operations?
- Are cardiology encounters, outpatient visits, age criteria, prior-history requirements, and follow-up requirements operationally defined?
- Are source-population denominators and cohort flow reported?
- Are exclusions likely to select patients with more complete EHR histories?

Flag as a concern when:
- Eligibility depends on undocumented clinical judgment.
- Follow-up or prior-history requirements create a selected population unlike deployment.
- Cohort construction cannot be reproduced from the reported schema.

### Structured Feature Representation
Ask:
- Which structured domains are used: diagnoses, problem list, medications, labs, procedures, orders, vitals, demographics, encounters, referrals, utilization, social history, or cognitive tests?
- Are features derived from raw events, grouped concepts, counts, recency, trajectories, or embeddings?
- Are vocabularies and code systems reported?
- Are local codes mapped to standard concepts?
- Are features restricted to availability before the index time?

Flag as a concern when:
- Feature definitions are too vague to reproduce.
- Local codes or flowsheet rows are used without mapping details.
- Structured features encode downstream workup rather than pre-index clinical state.

### Note and Text Metadata Representation
Ask:
- Are note types, author types, specialties, departments, service lines, encounter links, creation times, signing times, addenda, and copied-forward text addressed?
- Can notes be joined to encounters and patients without including post-index text?
- Are note sections, templates, or document classes described?
- Are de-identification, note filtering, and text extraction steps reported?

Flag as a concern when:
- Notes are treated as undifferentiated text.
- Note timestamps are insufficient to determine feature availability.
- Outcome-defining notes may be included among predictors.

### Label and Outcome Data Representation
Ask:
- Where do labels come from in the schema: diagnosis codes, problem lists, encounters, orders, referrals, cognitive tests, medications, chart review, NLP, registry, or claims?
- Are label dates and evidence dates represented separately?
- Are labels linked to events, encounters, providers, or specialties?
- Can cognitive outcome evidence be separated from care-pathway evidence?

Flag as a concern when:
- Label provenance is unclear.
- Outcome timing depends on billing or documentation date rather than clinical event date.
- Future diagnosis, testing, or referral labels are not distinguished from impairment evidence.

### Vocabulary, Code Sets, and Mappings
Ask:
- Are ICD, SNOMED, RxNorm, LOINC, CPT, HCPCS, NDC, local flowsheet, order, referral, and note-type code sets reported where relevant?
- Are concept-set construction methods described?
- Are mappings versioned, audited, or validated?
- Are local-to-standard mappings complete enough for reuse?

Flag as a concern when:
- Code sets are missing for central variables.
- The paper relies on proprietary or local concepts without definitions.
- Vocabulary versions and mapping quality are absent.

### Missingness, Data Quality, and Provenance
Ask:
- Does the paper describe missingness by variable, site, time, subgroup, or encounter type?
- Is missingness interpreted as absence, unknown, not measured, or not applicable?
- Are implausible values, duplicates, conflicting events, copied-forward notes, and data-entry artifacts handled?
- Is feature provenance preserved enough to audit model behavior?

Flag as a concern when:
- Missing structured data are treated as normal values without clinical rationale.
- Missingness likely reflects care intensity or access.
- Data quality checks are absent for heavily transformed EHR features.

### Reproducibility and Portability
Ask:
- Could another institution implement the same cohort, labels, features, and time windows?
- Are SQL, code, concept sets, data dictionaries, mappings, or pseudocode available?
- Does the study test portability across sites, EHRs, common data models, or time periods?
- Are implementation assumptions stated clearly enough to adapt to Epic data?

Flag as a concern when:
- Reimplementation would require guessing central variables.
- The paper's method depends on local schema conventions without translation guidance.
- Portability is claimed but not tested or operationalized.

### Fit to Epic-to-Model-Ready Pipeline
Ask:
- Does the paper directly inform an Epic-to-model-ready data transformation path?
- Does it support OMOP, FHIR, PCORnet, i2b2, custom warehouse, or direct Epic extraction for this project?
- Which schema choices should this project adopt, avoid, or source-check?
- What data dictionary fields or concept sets should be created before modeling?

Flag as a concern when:
- The paper is methodologically relevant but provides little implementation guidance.
- The proposed representation would not preserve encounter timing or note availability.

## Definition of Done
An EHR schema and common data model specialist review is complete when:
- `reviews/citation_key/ehr_schema_common_data_model_reviewer.md` exists.
- The source system, unit of analysis, time anchors, feature representation, label representation, vocabularies, and portability issues are explicit.
- The review states whether the paper helps this project's Epic-to-model-ready pipeline.
- Missing schema details and leakage risks are separated from ordinary limitations.
- Recommended follow-up identifies needed code sets, data dictionaries, mappings, or source checks.
