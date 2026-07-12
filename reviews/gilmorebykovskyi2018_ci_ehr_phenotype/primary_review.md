# Primary Review: gilmorebykovskyi2018_ci_ehr_phenotype

## Review Status

Complete.

## Review-Relevant Contribution

Gilmore-Bykovskyi et al. show that unstructured inpatient EHR notes commonly contain cognitive and behavioral descriptors relevant to cognitive impairment, often in informal clinician language.

## Publication Status and Evidence Weight

Publication status: peer-reviewed JAMIA article. Evidence weight: moderate as phenotype/terminology evidence; indirect for predictive modeling.

## Fit to Problem Statement

Strong for EHR text and cognitive-impairment phenotype design. Weak for dementia risk prediction, outpatient cardiology context, and model validation.

## Evidence Category

Indirect phenotype-design evidence.

## Clinical Target

Cognitive impairment symptoms among hospitalized patients with claims-identified dementia.

## Data and Cohort Relevance

Hospitalized older adults with dementia and hip fracture/stroke. This is relevant to acute-care documentation but not directly to cardiology visits.

## EHR Text Relevance

High. The study reviews free-text documentation across many note and flowsheet sources.

## Label or Outcome Relevance

Dementia status came from Medicare claims codes. The study derives symptom categories in known dementia patients rather than identifying unknown cases.

## Modeling Relevance

The paper does not train a prediction model. It is useful for feature and terminology design.

## Validation and Utility Signals

Reliability of text classification is good, with Cohen kappa 0.82 and Gwet AC1 0.83. No predictive validation is performed.

## Bias/Causality/Downstream Action Issues

Documentation reflects clinician recognition and language, not necessarily true cognitive status. Dementia and delirium cannot be separated.

## Portability/Implementation Signals

The authors caution that terminology may vary across settings and EHRs. Future validation in broader populations is needed.

## Key Extracted Claims

- Ninety percent of reviewed EHRs had at least one narrative statement reflecting cognitive-impairment symptoms.
- Common categories included confusion, orientation, executive function/reasoning, global cognition, and agitation.
- Most cognitive descriptions used clinically derived, informal descriptors rather than formal diagnostic terminology.

## What This Paper Supports

Use to justify broad note terminology and concept sets for cognitive-impairment phenotyping.

## What This Paper Does Not Support

Do not use it for model performance, dementia risk prediction, external validation, or cardiology screening utility.

## Default Specialist Reviews Called

All default specialist reviewers completed.

## Additional Specialist Reviews Needed

None required.

## Primary Reviewer Notes

This paper is valuable for reminding us that the relevant note signal may be symptom language, not only diagnosis names.
