# Specialist Review: EHR Dementia Prediction Quality

## Specialist Scope
Assessment of John et al. 2022 as evidence for EHR/observational-data dementia prediction quality, reporting, validation, and implementation readiness.

## Bottom Line
`methodologically_informative`. This paper is highly useful for showing why published dementia prediction models often cannot be reused or externally validated, even when they appear quantitatively promising.

## Prediction Task Clarity
partial. The paper evaluates models for incident dementia or ADRD prediction, but the underlying models vary in target, time origin, predictor windows, and horizons.

## Index Date, Observation Window, and Prediction Horizon
weak across the reviewed model literature. The key finding for this domain is that index date and predictor windows were often not reported.

## Data Source and Cohort Definition
adequate for the validation study; variable for the reviewed model literature. Use of OMOP-mapped observational health databases is important for reproducibility and transportability.

## Outcome and Reference Standard
partial. The paper evaluates reported target/outcome definitions but does not eliminate the problem that dementia labels in observational data can reflect diagnosis and coding processes.

## Comparator or Control Group
partial. The summary does not provide enough detail to assess negative/control definitions across validated models.

## EHR Text and Structured Data Use
not_applicable for EHR text; adequate for structured observational data. The paper does not test clinical-note features.

## Missing Data and Feature Availability
partial. The paper's emphasis on reporting criteria is relevant, but missingness handling is not the central extracted point in the current summary.

## Validation
adequate and central. The paper directly evaluates external validation feasibility and performs validation for selected models.

## Calibration, Thresholds, and Clinical Utility
partial. Calibration is considered, but missing model components such as baseline hazard can prevent recalibration. Clinical utility and cardiology-specific thresholds are not addressed.

## Reporting and Reproducibility
strong direct relevance. Incomplete reporting is the main barrier identified.

## Care-Pathway and Downstream-Action Bias
partial. The paper does not frame the problem this way, but dementia labels in observational data remain vulnerable to diagnosis opportunity and coding.

## Implementation Readiness
partial. OMOP/OHDSI infrastructure improves feasibility, but many published models are not implementable from their reports.

## Strengths
- Directly tests external validation feasibility.
- Uses observational health data and common data model infrastructure.
- Identifies concrete missing reporting elements.

## Concerns
- Does not address cardiology workflow.
- Does not use unstructured text.
- Does not solve label validity or downstream-action bias.

## Missing Information
- Detailed label algorithms for each model.
- Threshold and clinical action logic for cardiology-facing use.
- Subgroup transportability details from the current summary.

## Implications for This Literature Review
This paper should anchor the validation/reporting section and reinforce that our model must be externally validatable from its published description.

## Recommended Follow-up
- Use this paper to refine reporting requirements in the study-design template.
- Run source-document checks before citing exact counts or model-specific validation results in manuscript prose.
