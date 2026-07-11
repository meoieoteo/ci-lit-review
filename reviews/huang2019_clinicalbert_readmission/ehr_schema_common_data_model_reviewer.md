# Specialist Review: EHR Schema and Common Data Model

## Specialist Scope
Assessment of ClinicalBERT readmission modeling for EHR data representation.

## Bottom Line
Limited schema guidance: the paper shows clinical notes can be used for prediction, but does not provide an Epic-to-CDM or encounter-level transformation pattern for this project.

## Data Model and Source System Summary
Clinical-note EHR corpus for pretraining and readmission prediction.

## Unit of Analysis and Identifiers
Likely admission/patient prediction, not cardiology encounter-level risk scoring.

## Encounter and Timeline Representation
Temporal note sequencing matters, but the summary does not provide reusable timestamp logic.

## Cohort and Eligibility Implementation
Readmission cohort design is not directly applicable to cognitive-risk cardiology encounters.

## Structured Feature Representation
Structured data are not the main focus.

## Note and Text Metadata Representation
Clinical note availability is central, but note-type and section metadata are not enough in the summary for implementation reuse.

## Label and Outcome Data Representation
Readmission is a hospital outcome, not a cognitive outcome or diagnosis-opportunity label.

## Vocabulary, Code Sets, and Mappings
No CDM vocabulary mapping contribution.

## Missingness, Data Quality, and Provenance
No major operational data-quality guidance.

## Reproducibility and Portability
Model-level portability is possible; data-extraction portability is not addressed.

## Fit to Epic-to-Model-Ready Pipeline
Low to moderate for text-modeling layer only.

## Strengths
- Shows how clinical notes can feed a predictive model.

## Concerns
- No encounter-start anchor or note-provenance specification for this use case.

## Missing Information
- Note metadata, SQL/extraction logic, and local-to-standard mappings.

## Implications for This Literature Review
Use as model background, not schema evidence.

## Recommended Follow-up
Pair with papers that describe note extraction and sectioning in operational EHR systems.
