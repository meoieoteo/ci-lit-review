# Literature Review Outline

## 1. Introduction and Clinical Motivation

- Cardiovascular disease and cognitive impairment are clinically linked.
- Cardiologists may encounter signs of cognitive impairment before formal cognitive evaluation occurs.
- Longitudinal EHR data, especially free text, may contain signals of current unmet cognitive care need or future cognitive impairment.
- The immediate project focus is risk scoring before the cardiology encounter, not within-encounter test selection or post-encounter action policy.

## 2. Clinical Target and Prediction Setting

- Define the decision point as immediately before the start of a cardiology encounter.
- Define the unit of prediction as `patient_id + cardiology_encounter_id + encounter_start_time`.
- Separate possible targets:
  - Current unmet cognitive care need.
  - Currently present but undocumented cognitive impairment.
  - Future cognitive impairment.
  - Future coded dementia diagnosis.
  - Future referral, testing, or care pathway.
- Explain why these targets are not interchangeable.

## 3. Cohort Construction and Timing

- Define index date, observation window, and prediction horizon.
- Restrict model inputs to data strictly before the cardiology encounter.
- Exclude data generated during or after the cardiology encounter from predictors.
- Address repeated encounters per patient.
- Define required prior history and follow-up.

## 4. Label Definition and Outcome Validity

- Compare diagnosis-code labels, cognitive-test labels, referral/testing labels, chart-reviewed labels, and NLP-derived labels.
- Discuss the risk of treating absence of dementia codes as absence of cognitive impairment.
- Separate disease state, documentation, diagnosis opportunity, and downstream action.
- Identify label misclassification risks and validation needs.

## 5. Downstream-Action and Diagnosis-Opportunity Bias

- Explain how referral, testing, follow-up, specialty access, and documentation can create or obscure labels.
- Discuss the problem of clinically similar patients receiving different labels because one is worked up and another is not.
- Consider modeling or stratifying diagnosis opportunity, follow-up completeness, and care-pathway events.
- Frame this as a potential methodological contribution.

## 6. EHR Text as a Signal Source

- Review evidence that unstructured EHR text captures clinical information missing from structured data.
- Emphasize cognitive, functional, behavioral, caregiver, adherence, frailty, falls, delirium, social, and appointment-navigation signals.
- Distinguish raw text embeddings from interpretable note-derived concepts.
- Discuss note type, note date, sectioning, temporality, negation, and portability.

## 7. Structured and Longitudinal EHR Representation

- Review structured EHR baselines.
- Review longitudinal patient-history models.
- Discuss visit sequences, irregular time intervals, diagnoses, medications, labs, procedures, utilization, and notes.
- Compare interpretable deficit or concept features with learned embeddings.

## 8. Modeling Strategy

- Start with simple baselines before end-to-end large models.
- Suggested ladder:
  - Structured baseline model.
  - Structured data plus note-derived concepts.
  - Structured data plus note embeddings.
  - Longitudinal sequence model.
  - LLM-assisted extraction or augmentation.
  - End-to-end LLM scoring only if justified.
- Emphasize that model architecture is not the main contribution unless target and labels are defensible.

## 9. Modeling Strategy Resources

- Maintain a separate practical resource guide in [ml_resources/](ml_resources/).
- Curate secondary explanatory resources, textbooks, lectures, tutorials, and official documentation that help the team understand the modeling ladder in Section 8.
- Use original papers selectively when they are unusually instructive or directly tied to reviewed methods.
- Organize resources by topic, implementation stack, and intended audience.

## 10. Validation, Calibration, and Clinical Utility

- Review internal, temporal, site-level, and external validation.
- Emphasize calibration, threshold performance, and workflow-specific utility.
- Discuss sensitivity, specificity, PPV, NPV, calibration intercept/slope, and decision-curve or net-benefit analysis.
- Evaluate transportability across sites, populations, EHR systems, note types, and documentation practices.

## 11. Data Transformation and Reproducibility

- Review how Epic or local EHR data can be translated into reusable model-ready formats.
- Consider OMOP or other common data model pathways.
- Discuss reproducible feature definitions, note processing, code lists, and temporal extraction.
- Identify which parts of the pipeline are site-specific versus portable.

## 12. Sequential Diagnosis and Future Action Policy

- Treat this as later-stage framing, not the first model's scope.
- Review sequential diagnosis, active feature acquisition, value of information, POMDPs, and dynamic treatment regimes only insofar as they inform future work.
- Clarify that the current model scores risk before the encounter and does not recommend next tests or referrals.

## 13. Synthesis and Proposed Contribution

- Summarize the strongest lessons from the literature.
- Identify the main gap: careful target, label, cohort, timing, and validation design for pre-cardiology cognitive-risk scoring using longitudinal EHR text.
- State the likely contribution:
  - A defensible encounter-level cohort and label strategy.
  - Use of longitudinal EHR text through interpretable concepts and/or embeddings.
  - Explicit handling of downstream-action and diagnosis-opportunity bias.
  - Validation and calibration designed for clinical workflow.

## 14. Open Questions

- What primary target should the first model use?
- What label source is clinically meaningful and practically obtainable?
- What outcome horizon is appropriate?
- How should diagnosis opportunity be measured?
- Which note-derived concepts should be extracted first?
- What validation split best approximates deployment?
- What is the minimum useful output for a cardiologist before the encounter?
