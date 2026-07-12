# EHR Dementia Prediction Quality Review: hong2020_cognitive_concerns_nlp

## Review Status

Complete.

## Dementia-Relevance

High. The paper directly studies cognitive concerns related to dementia in EHR notes.

## Prediction Versus Phenotyping

This is closer to phenotyping/case finding than prospective prediction. The input window and label window overlap.

## Clinical Specificity

The label is clinically broad. It may be useful for identifying patients needing cognitive evaluation, but it does not separate subjective concern, MCI, mild dementia, moderate dementia, and severe dementia.

## Feature Quality

The comparison between structured features and note-based features is valuable. The results show that structured codes and medications alone can miss cognitive impairment signals.

## Model Quality

The study uses sensible baselines and a long-document transformer. However, the small dataset and limited reporting make the transformer result exploratory.

## Implementation Quality

The authors propose an active learning loop and annotation tool for future work, but no deployed implementation is evaluated.

## Review Use

This paper should be cited as direct, early evidence that EHR notes matter for cognitive-concern detection. It should not anchor claims about prospective dementia prediction quality.
