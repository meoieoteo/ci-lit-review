# Primary Review: zhou2025_preoperative_frailty_llm

## Review Status
primary_review_complete

## Review-Relevant Contribution
This paper evaluates transformer language models for identifying preoperative frailty from clinical notes and shows that model performance depends strongly on the label source used to define frailty.

## Fit to Problem Statement
The paper is indirectly relevant. It is not about dementia or cardiology, but it closely matches the project's concern that EHR-derived labels can encode different constructs. The VES-13 versus eFI comparison is a useful warning for cognitive-risk labels based on diagnosis codes, tests, referrals, or chart-derived proxies.

## Evidence Category
unstructured_ehr_text; label_definition; validation_or_reporting_quality; clinical_decision_support; background_or_context

## Clinical Target
Preoperative frailty among older adults undergoing major spine surgery.

## Data and Cohort Relevance
The cohort is single-center and surgical, not cardiology. The data source is still clinically relevant because it uses routine preoperative clinical notes, which are analogous to encounter-adjacent documentation.

## EHR Text Relevance
Strong. The models classify frailty using selected text from anesthesia preoperative H&P notes, including medical history, HPI, and assessment/plan sections.

## Label or Outcome Relevance
Strong as a label-methodology warning. VES-13 and eFI labels did not transfer symmetrically, suggesting that label source can define the target construct as much as the model architecture does.

## Modeling Relevance
The paper compares BERT, RoBERTa, BioBERT, and PubMedBERT classifiers with frozen base weights and trained classification heads. It is relevant to choosing clinical versus general transformer variants, but the main lesson is label validity rather than architecture selection.

## Validation and Utility Signals
The study uses internal train/validation/test splits and cross-label testing between VES-13 and eFI datasets. RoBERTa trained and tested on VES-13 performed very well, while eFI-trained models generalized poorly to VES-13. External validation is absent, and calibration is not reported.

## Bias, Causality, and Downstream Action Issues
The paper does not address downstream-action bias directly. However, it illustrates construct bias: eFI-derived frailty may reflect coded comorbidities and EHR-recorded deficits rather than the same patient state captured by VES-13.

## Portability and Implementation Signals
Portability is limited by single-center design, spine-surgery population, anesthesia note type, and 512-token truncation. Still, the cross-label validation design is a useful template for testing whether two candidate labels represent the same target.

## Key Extracted Claims
- VES-13-trained RoBERTa achieved AUC 0.99 on VES-13 validation.
- VES-13-trained BioBERT and PubMedBERT achieved AUC 0.87 on eFI validation.
- eFI-trained models achieved AUC about 0.88-0.91 on eFI validation but only about 0.60-0.62 on VES-13 validation.
- The authors interpret this as evidence that VES-13 and eFI capture different frailty constructs.

## What This Paper Supports
It supports careful label-source evaluation, cross-label testing, and skepticism toward assuming that EHR-derived proxy labels match clinically assessed states.

## What This Paper Does Not Support
It does not support dementia prediction, future cognitive-impairment risk, cardiology-specific deployment, or clinical action thresholds for referral.

## Default Specialist Reviews Called
ehr_dementia_prediction_quality_reviewer.md

## Additional Specialist Reviews Needed
A label-definition reviewer would be useful for extracting this paper's implications for dementia/cognitive-impairment labels.

## Primary Reviewer Notes
This paper's most important contribution for the project is not that LLMs classify frailty; it is that label choice changes what the model learns.
