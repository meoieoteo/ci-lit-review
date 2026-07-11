# Primary Review: john2022_dementia_prediction_validation

## Review Status
primary_review_complete

## Review-Relevant Contribution
This paper is a core validation and reporting-quality paper for the review. It tests whether published dementia prediction models can be externally validated using observational health data and shows that many models lack enough reporting detail for validation.

## Fit to Problem Statement
Fit is high for validation, reporting, transportability, and reproducible cohort/model specification. The paper is not cardiology-specific and does not use unstructured EHR text, but it directly supports the project's need to define index date, observation window, prediction horizon, predictors, outcome, and full model specification before building a pre-cardiology cognitive-risk model.

## Evidence Category
- `dementia_prediction`
- `study_population_definition`
- `label_definition`
- `validation_or_reporting_quality`
- `ehr_to_common_data_model`
- `background_or_context`

## Clinical Target
Incident dementia or Alzheimer disease and related dementias. The exact clinical target varies across the published models reviewed and externally validated.

## Data and Cohort Relevance
The study is highly relevant to observational health data and OMOP/OHDSI-style validation. It reinforces that models developed in one database or cohort cannot be assumed to transport to another without clear definitions and external validation.

## EHR Text Relevance
Low direct relevance. The externally validated models use structured observational health data, not clinical notes. The indirect lesson is that note-derived models will need at least the same level of transparent time-window, predictor, and outcome reporting.

## Label or Outcome Relevance
Moderate to high. The paper focuses on incident dementia prediction and evaluates whether target/outcome definitions are reported well enough for external validation. It does not solve dementia label validity, but it demonstrates that even published models often fail to report the details needed to reconstruct labels and time-at-risk.

## Modeling Relevance
The paper validates existing models rather than proposing a new architecture. It covers traditional statistical and machine-learning approaches and uses OHDSI patient-level prediction infrastructure. The validated predictors are primarily fixed-length structured feature sets derived from OMOP observational health data, such as demographics, diagnosis-code indicators, medication-derived predictors, and model risk-score components. The modeling lesson is that deployability depends on full specification and validation, not just algorithm choice.

## Validation and Utility Signals
This is the paper's strongest contribution. The authors found that only a minority of published models reported enough information for full external validation; only three selected models were externally validated. Some models transported reasonably to some databases, but missing baseline hazard or full model specification limited recalibration and reuse.

## Bias, Causality, and Downstream Action Issues
The paper is not primarily about downstream-action bias. However, dementia outcomes in observational databases remain vulnerable to diagnosis opportunity, coding, and follow-up differences. The paper supports the need to report target and time-at-risk carefully enough to detect these problems.

## Portability and Implementation Signals
High relevance. Use of OMOP CDM and OHDSI patient-level prediction infrastructure is directly relevant to the project's reproducibility and transportability aims. The paper also shows that transportability is often blocked by incomplete reporting.

## Key Extracted Claims
- The authors identified 59 dementia prediction models.
- All models reported prediction method, development database, and target/outcome definitions.
- Only 22 models reported index date.
- Only 21 models reported predictor time window.
- Only 9 models reported full model specifications.
- Walters, Mehta, and Nori models were selected for external validation.
- Recalibration could not be fully assessed for at least one model because baseline hazard was not reported.

## What This Paper Supports
This paper supports making index date, observation window, prediction horizon, target definition, model specification, and external validation first-order design requirements. It also supports using common data model thinking for transportability.

## What This Paper Does Not Support
It does not support claims that existing dementia prediction models are ready for cardiology deployment. It does not establish the value of unstructured EHR text. It does not provide a label strategy for current unmet cognitive care need.

## Default Specialist Reviews Called
- `ehr_dementia_prediction_quality_reviewer.md`
- `label_definition_reviewer.md`
- `validation_reviewer.md`

## Additional Specialist Reviews Needed
- EHR schema/common-data-model reviewer.
- Causal bias/downstream-action reviewer if this paper is used to motivate outcome-ascertainment design.

## Primary Reviewer Notes
Treat this paper as a design-standards paper. It should be cited when arguing that dementia prediction models must be reported and specified well enough for external validation, recalibration, and transport across observational databases.
