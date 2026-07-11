# Primary Review: lu2026_ehr_dementia_prediction_review

## Review Status
primary_review_complete

## Review-Relevant Contribution
This is a core review paper for the project. It directly surveys EHR-based dementia prediction models, evaluates model quality, and identifies weaknesses that map to the project's central concerns: outcome definition, label construction, EHR data type, calibration, external validation, and downstream clinical use.

## Fit to Problem Statement
Fit is high. The project is focused on pre-cardiology-encounter risk scoring using longitudinal EHR data, especially unstructured text, for current unmet cognitive care need or future cognitive impairment. Lu et al. do not focus on cardiology, but they define the broader EHR dementia prediction landscape and show that many existing models are clinically under-specified and methodologically fragile.

## Evidence Category
- `dementia_prediction`
- `current_cognitive_impairment_detection`
- `unstructured_ehr_text`
- `longitudinal_ehr_representation`
- `study_population_definition`
- `label_definition`
- `validation_or_reporting_quality`
- `clinical_decision_support`
- `downstream_action_bias`
- `background_or_context`

## Clinical Target
The paper distinguishes diagnostic models, which identify unrecognized or known dementia, from prognostic models, which predict future dementia. This distinction is directly relevant because our project still needs to choose between current unmet cognitive care need and future cognitive impairment as the main target.

## Data and Cohort Relevance
The review emphasizes routine EHR data as a scalable source for dementia detection, but also shows that cohort construction is often weak. Many models use non-nested case-control designs, unclear prediction windows, and poorly justified comparator groups. This matters for our project because patients without dementia codes cannot safely be treated as true negatives.

## EHR Text Relevance
The paper is important but cautionary for EHR text. Only 46 of 434 models used unstructured EHR data alone, and 41 used both structured and unstructured EHR data. The authors note that clinical notes may capture cognitive, functional, and behavioral changes that structured fields miss, but the review does not show that note-based models are already mature enough for direct clinical deployment.

## Label or Outcome Relevance
This is one of the strongest contributions. Lu et al. show that outcome definitions are often ambiguous, with many studies using recorded diagnoses as labels without specifying whether the task is known dementia, unrecognized dementia, or future dementia. This directly supports making label definition a first-order design task in our study rather than a backend implementation detail.

## Modeling Relevance
The paper suggests that model complexity is not the main limiting factor. Internal-validation AUROC did not differ substantially across statistical, machine-learning, and deep-learning methods. Included studies used heterogeneous and often incompletely reported input representations, including fixed engineered EHR feature sets, keyword/text-derived features, embeddings, and other NLP features. For our purposes, this argues against treating LLMs, transformers, or other AI methods as the contribution by themselves. The defensible contribution is more likely to come from better problem definition, better label construction, appropriate use of notes, explicit representation design, and validation.

## Validation and Utility Signals
The validation message is severe. Only 47 of 434 developed models were externally validated. Calibration was reported for only 69 models across 9 studies. Thresholds were rarely reported or clinically justified. This is directly relevant to any cardiology-facing score, because a score that is not calibrated or thresholded for a specific action cannot guide a cardiologist reliably.

## Bias, Causality, and Downstream Action Issues
The paper does not frame the issue as downstream-action bias in our exact terms, but it strongly supports the concern. Reliance on diagnosis codes creates misclassification because diagnosis depends on whether a patient was evaluated, where they received care, and whether dementia was recognized and coded. That creates a label that is partly a function of health-care pathways, not just cognitive state.

## Portability and Implementation Signals
Portability is a major concern. Most studies used US data, external validation was sparse, and coding practices vary across health systems. The review also notes that no models have clearly reached routine clinical implementation. This supports building the Inova/Epic-to-common-format data transformation path carefully rather than assuming an EHR model will transport easily.

## Key Extracted Claims
- The review included 56 studies, 434 developed models, and 155 external validations.
- Most models used structured EHR data only.
- Most models were prognostic rather than diagnostic.
- Only 4% of models used established clinical diagnostic criteria as reference standards.
- AUROC was commonly reported, but calibration was rarely assessed.
- All developed models were rated high risk of bias under PROBAST.
- The authors found no clear performance advantage from AI methods over traditional statistical methods.
- The authors identify unclear clinical intent, weak outcome definitions, incomplete reporting, and poor validation as major barriers to clinical use.

## What This Paper Supports
This paper supports using the literature review to sharpen target definition, index-date logic, outcome labeling, missing-data handling, calibration, and external validation plans. It supports the premise that EHR data are promising for dementia detection, but only if the clinical task and labels are rigorously defined. It also supports treating unstructured notes as potentially important because structured data can miss cognitive, behavioral, and functional signals.

## What This Paper Does Not Support
It does not establish that EHR dementia prediction models are ready for direct clinical deployment. It does not prove that unstructured text outperforms structured EHR data. It does not answer the cardiology-specific workflow question. It does not solve the causal problem created by downstream evaluation, referral, and diagnosis pathways. It does not identify a single best modeling method for our use case.

## Default Specialist Reviews Called
- `skeptical_lu.md`

## Additional Specialist Reviews Needed
- Validation/calibration reviewer.
- Clinical target and label-definition reviewer.
- EHR text/NLP reviewer.
- Causal bias and downstream-action reviewer.
- Data schema and Epic-to-common-model reviewer.

## Primary Reviewer Notes
For our project, this paper should be treated as a design constraint paper. It is less useful as a source of a deployable model and more useful as evidence that the field's main weakness is not lack of algorithms. The central warning is that dementia prediction from EHRs can look quantitatively promising while still being clinically ambiguous, biased by outcome ascertainment, poorly calibrated, and hard to implement.
