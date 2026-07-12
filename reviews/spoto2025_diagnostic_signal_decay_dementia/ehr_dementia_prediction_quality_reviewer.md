# EHR Dementia Prediction Quality Review: spoto2025_diagnostic_signal_decay_dementia

## Review Status

specialist_complete

## Prediction Study Status

This is not an EHR dementia prediction model. It is a claims-based analysis of dementia diagnosis-code patterns and their temporal/geographic variation.

## Target and Timing

The study observes dementia code categories across inpatient hospitalizations from 2016-2018. It does not define an index cardiology encounter, prediction horizon, or pre-index feature window.

## Relevance to Prediction Quality

The paper is relevant because it questions the outcome labels often used in dementia prediction. If future dementia diagnosis is the target, the target can be affected by code specificity, hospitalization exposure, coding practices, and geography.

## Strengths

- Large-scale national claims evidence.
- Focuses on diagnosis-code behavior rather than model architecture.
- Highlights that label quality can degrade even after dementia has entered the administrative record.

## Weaknesses

- No EHR text, structured clinical features, model evaluation, calibration, or clinical utility analysis.
- Restricted to inpatient claims among beneficiaries with dementia-coded hospitalizations.
- Preprint status limits authority for central claims.

## Study-Design Implications

A dementia-risk model should not treat all future ICD-coded dementia outcomes as equally informative. Outcome definitions should record care setting, first-code source, code specificity, and whether the endpoint reflects incident recognition or repeat nonspecific documentation.

## Recommended Use

Use in Section 5 as a methodological caution about outcome observability and code quality.
