# Specialist Review: EHR Schema and Common Data Model

## Specialist Scope
Assessment of structured plus free-text EHR representation for a next-generation electronic frailty index.

## Bottom Line
Strong data-representation analogue: the paper combines diagnoses, labs, procedures, medications, and free-text deficits into an interpretable longitudinal EHR feature set, though not in Epic or OMOP. The final modeling representation is a fixed-length binary deficit/concept feature set rather than a raw variable-length event sequence.

## Data Model and Source System Summary
Longitudinal regional EHR data from Central Finland, 2010-2023.

## Unit of Analysis and Identifiers
Patient-level frailty trajectories and outcomes; not encounter-level cardiology scoring.

## Encounter and Timeline Representation
Longitudinal history is central. Local implementation would need encounter-start anchoring for all deficits.

## Cohort and Eligibility Implementation
Population-based retrospective EHR design, source-check needed for eligibility details.

## Structured Feature Representation
The eFI includes ICD-10 diagnoses, laboratory items, prescribed medications/procedures as relevant, and free-text-derived deficits. These are collapsed into 53 binary deficit/concept features for eFI construction.

## Note and Text Metadata Representation
Free-text notes from multiple care settings are used, but note-type and timestamp implementation need source checking.

## Label and Outcome Data Representation
Frailty deficit accumulation and outcomes such as mortality, severe infections, and fractures; not dementia labels.

## Vocabulary, Code Sets, and Mappings
ICD-10 and laboratory definitions are central; mapping to local Epic/OMOP concepts would be required.

## Missingness, Data Quality, and Provenance
Binary deficit construction makes missingness and observation opportunity important.

## Reproducibility and Portability
Conceptually portable, but local vocabularies, language, and note documentation practices may limit direct reuse.

## Fit to Epic-to-Model-Ready Pipeline
High as a feature-engineering template; moderate as a CDM template.

## Strengths
- Interpretable binary deficits.
- Structured plus text feature integration.
- Longitudinal EHR foundation.

## Concerns
- Not Epic or OMOP.
- Deficit absence may reflect documentation absence.

## Missing Information
- Full code sets, note metadata, and NLP provenance need source checking.

## Implications for This Literature Review
Use as an anchor for interpretable note-derived and structured geriatric feature representation.

## Recommended Follow-up
Extract candidate deficit concepts and map each to Epic source fields, standard vocabularies, and note evidence rules.
