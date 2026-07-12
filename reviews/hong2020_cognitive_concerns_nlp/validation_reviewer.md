# Validation Review: hong2020_cognitive_concerns_nlp

## Review Status

Complete.

## Validation Design

The final dataset of 767 patients was randomly split into 90% train and 10% held-out test. Some model selection used cross-validation or a validation subset within the training data.

## Metrics

Reported metrics include AUC, accuracy, false positives, false negatives, sensitivity, specificity, PPV, and NPV.

## Main Results

Structured baseline: AUC 0.79, sensitivity 0.59, specificity 1.00. Regular-expression model: AUC 0.88. TF-IDF: AUC 0.90. Longformer: AUC 0.93, sensitivity 0.79, specificity 0.98.

## Strengths

The paper includes a held-out test set and compares against a structured-code/medication baseline.

## Limitations

The test set contains only 77 patients. There is no external validation, temporal validation, calibration analysis, subgroup analysis, decision-curve analysis, or clinical workflow evaluation. Thresholds were selected to maximize accuracy, which may not match clinical screening goals.

## Transportability

Unknown. The model was developed in one health system, using local notes and local documentation patterns.

## Use in Review

Use validation evidence cautiously as proof-of-concept discrimination, not as evidence of deployable performance.
