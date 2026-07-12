# Primary Review: li2024_dementia_risk_notes

## Review Status

primary_review_complete

## Review-Relevant Contribution

Li et al. is a direct dementia-risk prediction paper using longitudinal EHR medical notes only. Its main contribution for this literature review is not the specific model architecture by itself, but the combination of explicit observation windows, explicit prediction horizons, and a long-note content-selection method evaluated against several content-selection baselines.

## Publication Status and Evidence Weight

Peer-reviewed journal article in *Computers in Biology and Medicine*, reviewed from the final PDF version of record. Evidence weight is moderate direct evidence for notes-only dementia-risk modeling and long-text handling. It is not strong clinical-utility evidence because validation is internal, the sample is balanced case-control, calibration is not reported, external validation is absent, and the outcome is EHR diagnosis status rather than adjudicated cognitive impairment.

## Fit to Problem Statement

The paper fits the project's current focus on pre-encounter risk scoring from longitudinal EHR text. It supports the intuition that pre-outcome notes contain predictive signal for future dementia diagnosis and that note history should be anchored by lookback and prediction windows. The clinical setting is primary care rather than cardiology, so the cardiology-facing workflow implication is extrapolated.

## Evidence Category

- `dementia_prediction`
- `unstructured_ehr_text`
- `longitudinal_ehr_representation`
- `label_definition`
- `validation_or_reporting_quality`

## Clinical Target

The target is future incident dementia diagnosis over a six-month or one-year prediction horizon, not current unmet cognitive care need and not within-encounter assessment. The authors describe primary care providers as intended beneficiaries.

## Data and Cohort Relevance

The data source, INPC through Regenstrief, is relevant because it is a large multi-system EHR network with routine clinical notes. The cohort is less deployment-like because controls were downsampled to create a balanced 4,796-case and 4,796-control dataset.

## EHR Text Relevance

High. The model uses medical notes only, concatenated chronologically over one- or two-year observation periods. The proposed method explicitly addresses the fact that longitudinal note documents exceed transformer input limits.

## Label or Outcome Relevance

The label is incident dementia case status versus matched controls with no dementia or MCI diagnosis. This is useful as a future coded-diagnosis target but carries the usual diagnosis-opportunity concerns: diagnosis requires recognition and documentation, and controls defined by absence of dementia/MCI diagnosis may include unrecognized impairment.

## Modeling Relevance

The paper is directly relevant to modeling strategy. It compares decision-focused sentence selection with early truncation, late truncation, random truncation, pPSO, LED_BookSum, and LED_PubMed, holding the Longformer classifier architecture constant. This helps isolate content selection as a modeling design choice for long clinical text.

## Validation and Utility Signals

The main validation signal is internal three-fold cross-validation. AUCs range from 77.15 to 81.64 for the proposed method across tested token limits, observation periods, and horizons. The study reports precision, sensitivity, specificity, F1, and accuracy but not calibration or clinically linked thresholds. No external validation, temporal validation, or decision-curve analysis is reported.

## Bias, Causality, and Downstream Action Issues

The paper does not explicitly address downstream-action bias. A future dementia diagnosis is partly a care-pathway and documentation outcome. Shorter horizons perform better, but shorter horizons may also increase the chance that notes contain near-diagnostic workup or recognition signals rather than earlier latent risk. The model may learn care utilization and documentation patterns as well as cognitive risk.

## Portability and Implementation Signals

The study uses a real multi-system EHR network and notes-only inputs, which is promising for portability. However, it does not specify note types, author specialties, note timestamps beyond observation windows, code lists, or enough schema detail to reproduce the cohort directly in Epic or OMOP. The authors report code availability through PDMlaboratory, but the data are restricted.

## Key Extracted Claims

- Longitudinal medical notes alone can support future dementia diagnosis discrimination in a retrospective EHR cohort.
- A one-year observation and one-year horizon model using decision-focused sentence selection achieved AUC 78.43 with a 1,024-token limit.
- Six-month horizons had AUCs above 80 for the proposed method.
- Decision-focused content selection outperformed truncation, pPSO, and generic LED summarization baselines under the one-year observation and one-year horizon design.
- Early truncation outperformed late truncation, suggesting notes closer to the index date contain more relevant signal.

## What This Paper Supports

- Including notes-only dementia-risk prediction as direct evidence in the review.
- Treating observation window and prediction horizon as core design variables.
- Considering content selection before transformer modeling for long longitudinal notes.
- Comparing text-selection strategies under a constant classifier architecture.

## What This Paper Does Not Support

- Clinical readiness of a cardiology-facing risk score.
- Real-world PPV or workload estimates under natural prevalence.
- External generalizability across health systems or EHR implementations.
- Validated diagnosis of true cognitive impairment independent of documentation.
- Superiority over a full structured-plus-text EHR model in the same cohort.

## Default Specialist Reviews Called

- `label_definition_reviewer`
- `validation_reviewer`
- `ehr_dementia_prediction_quality_reviewer`
- `ehr_schema_common_data_model_reviewer`
- `nlp_concept_extraction_reviewer`

## Additional Specialist Reviews Needed

No additional standing specialist reviewer is required. A later source-check pass should extract the exact dementia and MCI code lists if available outside the main article.

## Primary Reviewer Notes

This redo is based on the final article PDF rather than the NIH author-manuscript HTML. The main review conclusion remains similar, but the updated evidence note should be stricter about balanced case-control validation, label provenance, and lack of calibration.
