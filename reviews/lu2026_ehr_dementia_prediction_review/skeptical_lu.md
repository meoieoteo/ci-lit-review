# Specialist Review: skeptical_lu

## Specialist Scope
This specialist review applies a skeptical-review stance to Lu et al. 2026. The local `agents/specialist_reviewers/skeptical_lu.md` file is currently empty, so this review follows the standard specialist reviewer template while focusing on skeptical appraisal.

## Bottom Line
Lu et al. is highly useful for identifying failure modes in EHR dementia prediction, but it should not be used as evidence that any particular modeling strategy is adequate. The paper's strongest value is negative and methodological: it shows that the field is immature, poorly standardized, and vulnerable to label and validation problems.

## Domain-Specific Findings
The review's broad conclusion is persuasive because the evidence base is large and the methodological critique is consistent across multiple dimensions: outcome ambiguity, weak reference standards, incomplete reporting, sparse calibration, and limited external validation. Its use of PROBAST gives the critique structure.

The most important skeptical finding is that many models appear to predict coded or documented dementia rather than dementia itself. In real clinical workflows, the code is downstream of recognition, referral, specialist evaluation, documentation, and coding. That makes the label partly a care-process artifact.

The review also undercuts a naive AI-first framing. It reports similar internal-validation AUROC across statistical, machine-learning, and deep-learning approaches. The methodological bottleneck is data and target validity, not algorithm novelty.

## Strengths
- Directly relevant to EHR-based dementia detection and prediction.
- Clear distinction between diagnostic and prognostic tasks.
- Large included model count.
- Uses established prediction-model review and bias frameworks.
- Gives concrete reasons existing models are not ready for clinical use.
- Highlights calibration and threshold reporting, not just AUROC.

## Concerns
- The review summarizes a heterogeneous literature, so pooled or mean AUROC values should not be overinterpreted.
- Included models vary by population, data source, prediction horizon, target definition, and validation strategy.
- Because the review relies on published reports, poor reporting in primary studies limits what the authors can determine.
- PROBAST ratings are useful, but model-level counts can make heavily multi-model studies influence the apparent distribution of problems.
- The review does not deeply resolve how to build better labels for unrecognized current cognitive impairment versus future dementia.

## Missing Information
- Detailed comparison of specific note-processing approaches is limited in the main article.
- The main text does not provide enough detail to judge which unstructured-text methods are most promising.
- Cardiology-facing use cases are not addressed.
- The review does not provide an operational recipe for creating a label that accounts for downstream referral and diagnosis pathways.
- Supplementary files likely contain model-level details that should be inspected before using this paper to prioritize specific prior models.

## Implications for This Literature Review
This paper should anchor our quality checklist for dementia/EHR prediction papers. Any candidate model paper should be checked for prediction task, index date, prediction horizon, true label source, comparator group definition, missing-data handling, calibration, external validation, and clinical threshold logic.

For the project, Lu et al. strengthens the case that our contribution may come from better target and cohort construction, especially handling downstream action and unstructured-text evidence, rather than from applying a more complex model.

## Recommended Follow-up
- Pull the Lu supplementary files and extract model-level references relevant to unstructured notes.
- Use this paper to define a review checklist for all EHR dementia prediction studies.
- Create a dedicated label-definition reviewer or template informed by the outcome failures Lu et al. identifies.
- Add a validation/calibration specialist reviewer before reviewing additional prediction model papers.
