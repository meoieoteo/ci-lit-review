# Study Design Template: Pre-Cardiology Cognitive-Risk Scoring

## Purpose
Use this template to specify the design of this project's own prediction study before modeling begins.

The central design requirement is to separate:
- The clinical target.
- The prediction time.
- The observation window.
- The outcome window.
- The care pathway that creates or obscures outcome labels.

## Study Objective
State the exact objective in one or two sentences.

Example:

```text
Develop and validate an encounter-level model that uses longitudinal EHR data available before a cardiology encounter to estimate the probability of current unmet cognitive care need or future cognitive impairment.
```

## Clinical Use Case
Describe the intended decision point.

Required fields:
- User:
- Setting:
- Decision moment:
- Intended model output:
- Actions the model may inform:
- Actions outside the current model scope:

Project default:

```text
The decision moment is immediately before the start of a cardiology encounter. The model may support cardiologist awareness and documentation, but it does not recommend diagnostic tests, referrals, treatment, or downstream policy.
```

## Unit of Prediction
Define one row of the analytic dataset.

Project default:

```text
patient_id + cardiology_encounter_id + encounter_start_time
```

Each patient may contribute multiple cardiology encounters if the sampling strategy allows repeated encounters.

Specify:
- Whether repeated encounters per patient are allowed:
- Minimum time between included encounters:
- How clustering by patient will be handled:
- Whether encounters after known dementia diagnosis are included:

## Source Population
Describe the population from which eligible encounters are sampled.

Specify:
- Health system:
- Data source:
- Care setting:
- Calendar period:
- Minimum patient age:
- Required prior EHR history:
- Required follow-up:
- Inclusion criteria:
- Exclusion criteria:

## Index Date or Time Origin
Define the index time precisely.

Project default:

```text
encounter_start_time for the cardiology encounter
```

Rules:
- Inputs may include data strictly before `encounter_start_time`.
- Inputs must not include data collected during the cardiology encounter.
- Inputs must not include data collected after the cardiology encounter.
- Outcome ascertainment may use post-index data, but outcome features must not leak into predictors.

## Observation Window
Define the lookback period for predictors.

Specify:
- Earliest allowed lookback:
- Latest allowed predictor timestamp:
- Whether all prior history is used:
- Whether fixed windows are used:
- How sparse history is handled:
- How external records or imported notes are handled:

Candidate windows:
- All available history before index.
- 5 years before index.
- 2 years before index.
- 1 year before index.
- Recent window plus long-history summaries.

## Candidate Targets
List all target definitions under consideration. Do not collapse these into a single "dementia prediction" target.

### Current Unmet Cognitive Care Need
Definition:

Potential label sources:
- Chart-reviewed cognitive impairment without adequate documentation or follow-up.
- Cognitive concern documented outside the problem list.
- Functional, caregiver, behavioral, or safety evidence suggesting unmet need.

Key risks:
- Requires clinical adjudication.
- May be expensive to label.
- May still depend on documentation quality.

### Currently Present but Undocumented Cognitive Impairment
Definition:

Potential label sources:
- Subsequent cognitive testing shortly after index.
- Specialist diagnosis shortly after index.
- Chart review using pre-index and near-index evidence.

Key risks:
- Post-index workup may be caused by cardiology action.
- Short follow-up can miss true impairment.

### Future Cognitive Impairment
Definition:

Potential label sources:
- New cognitive test abnormality.
- New diagnosis after a clean baseline period.
- Chart-reviewed incident impairment.

Key risks:
- Outcome depends on surveillance intensity.
- Death and loss to follow-up are competing concerns.

### Future Coded Dementia Diagnosis
Definition:

Potential label sources:
- ICD diagnosis codes.
- Problem list additions.
- Dementia medications.
- Specialist diagnosis codes.

Key risks:
- Diagnosis codes may reflect documentation, referral, access, and care opportunity.
- Absence of a code is not proof of absence of disease.

### Future Referral, Testing, or Care Pathway
Definition:

Potential label sources:
- Referral orders.
- Cognitive screening orders or results.
- Neurology, geriatrics, psychiatry, or memory-clinic encounters.
- PCP communication or follow-up.

Key risks:
- This is a downstream action target, not a disease-state target.
- It may be useful operationally but should not be interpreted as cognitive impairment.

## Primary Target Selection
State the selected primary target.

Required rationale:
- Why this target matches the clinical use case:
- Why the label is available:
- Why label timing is defensible:
- How label misclassification will be assessed:
- What this target does not mean:

## Outcome Window
Define when outcomes are observed relative to the index encounter.

Specify:
- Outcome window start:
- Outcome window end:
- Minimum required follow-up:
- Clean baseline or washout period:
- Whether events on index day are included:
- How death is handled:
- How loss to follow-up is handled:

Candidate windows:
- 0 to 90 days after index for near-term unmet care need evidence.
- 0 to 1 year after index for future diagnosis or evaluation.
- 1 to 3 years after index for incident cognitive impairment.
- Multiple horizons with separate models or labels.

## Label Construction
Describe the exact algorithm or adjudication process.

For each candidate label, specify:
- Positive criteria:
- Negative or control criteria:
- Indeterminate criteria:
- Required evidence date:
- Whether pre-index evidence is allowed:
- Whether post-index evidence is allowed:
- Whether a label can be assigned from absence of evidence:
- Planned validation sample:
- Estimated sensitivity and specificity:

## Downstream-Action and Diagnosis-Opportunity Bias
Describe how the design will distinguish disease evidence from opportunity to be diagnosed.

Required fields:
- Post-index referral indicators:
- Post-index cognitive testing indicators:
- Post-index PCP contact:
- Post-index neurology, geriatrics, psychiatry, or memory-clinic contact:
- Follow-up completeness:
- Health-system contact intensity:
- Competing death:
- Censoring definition:
- Whether these variables are outcomes, stratifiers, sensitivity variables, or excluded from predictors:

Questions to answer:
- Could two equivalent patients receive different labels because one was worked up and the other was not?
- Does the label measure impairment, documentation, diagnosis, referral, testing, or follow-up?
- Will the analysis model diagnosis opportunity separately from cognitive outcome evidence?
- Will sensitivity analyses restrict to patients with adequate opportunity for diagnosis?

## Predictor Sources
List all input data sources available strictly before index.

Structured EHR:
- Demographics:
- Diagnoses:
- Medications:
- Procedures:
- Labs:
- Vitals:
- Utilization:
- Prior referrals:
- Cognitive tests:

Unstructured EHR text:
- Note types:
- Note authors or specialties:
- Time windows:
- Exclusions:
- De-identification or preprocessing:
- Timestamp rules:

Other sources:
- Claims:
- Registries:
- Imaging metadata:
- Social determinants fields:
- External documents:

## Note-Derived Concept Inventory
Define candidate interpretable concepts before choosing raw embeddings or end-to-end LLM features.

Candidate concept families:
- Cognitive symptoms.
- Functional impairment.
- Instrumental activities of daily living.
- Medication adherence or management difficulty.
- Appointment navigation difficulty.
- Caregiver involvement or concern.
- Behavioral or psychiatric symptoms.
- Delirium, confusion, or altered mental status.
- Falls, frailty, gait, mobility, or balance.
- Driving, financial, or home-safety concerns.
- Social isolation or lack of support.
- Hearing, vision, language, or health-literacy barriers.
- Prior cognitive screening or refusal.

For each concept, specify:
- Definition:
- Evidence phrases or examples:
- Negation and uncertainty handling:
- Temporality handling:
- Note types allowed:
- Whether concept is patient-state, caregiver-state, or care-process evidence:

## Modeling Ladder
Pre-specify the modeling ladder.

Recommended order:
1. Structured baseline model.
2. Structured data plus note-derived concepts.
3. Structured data plus note embeddings.
4. Longitudinal sequence model.
5. LLM-assisted extraction or augmentation.
6. End-to-end LLM scoring only if justified by earlier results.

For each model tier, specify:
- Inputs:
- Prediction horizon:
- Training sample:
- Validation sample:
- Interpretability method:
- Calibration method:
- Expected role in the final study:

## Data Splitting and Validation
Define validation from the beginning.

Required fields:
- Development sample:
- Internal validation method:
- Temporal validation:
- Site or practice validation:
- External validation:
- Patient-level leakage prevention:
- Encounter-level leakage prevention:
- Model selection procedure:
- Final locked model procedure:

Minimum reporting:
- Discrimination:
- Calibration plot:
- Calibration intercept:
- Calibration slope:
- Sensitivity:
- Specificity:
- PPV:
- NPV:
- Threshold rationale:
- Decision-curve or net-benefit analysis:

## Fairness and Subgroup Evaluation
Specify planned subgroup analyses.

Candidate strata:
- Age group.
- Sex.
- Race and ethnicity.
- Language.
- Insurance or socioeconomic proxy.
- Baseline cardiovascular condition.
- Prior healthcare utilization.
- Primary-care attachment.
- Neurology or geriatrics access.
- Follow-up completeness.

For each subgroup, specify:
- Sample size:
- Outcome prevalence:
- Calibration:
- Threshold performance:
- Missingness:
- Label opportunity concerns:

## Missing Data
Describe how missingness will be represented and interpreted.

Required fields:
- Which variables can be missing:
- Whether missingness is structural, random, or care-process related:
- Imputation method:
- Missing indicators:
- Complete-case exclusions:
- Sensitivity analyses:

## Leakage Checks
List explicit leakage checks.

Required checks:
- No predictor timestamp at or after `encounter_start_time`.
- No cardiology encounter note content used as input.
- No post-index referral, test, diagnosis, or medication used as input.
- No label-defining code or phrase used when it occurs after index.
- No future encounter count or follow-up duration used as input unless intentionally modeled before index.
- No repeated patient split across training and validation when patient-level independence is required.

## Sensitivity Analyses
Pre-specify analyses that test target and label assumptions.

Candidate analyses:
- Vary outcome horizon.
- Vary required lookback history.
- Restrict to patients with sufficient follow-up.
- Restrict to patients with PCP contact after index.
- Stratify by post-index diagnostic opportunity.
- Exclude patients with prior dementia codes.
- Separate diagnosis-code labels from cognitive-test labels.
- Compare raw diagnosis target with adjudicated or composite target.
- Compare note-derived concepts with raw text embeddings.

## Deployment Fit
Describe what would be required for a cardiology workflow.

Fields:
- Intended display timing:
- Score refresh cadence:
- Explanation format:
- Alert or passive display:
- Human review requirement:
- Documentation implications:
- Monitoring after deployment:
- Failure modes:

## Open Design Decisions
Maintain a running list.

| Decision | Options | Current Lean | Evidence Needed | Owner | Due Date |
| --- | --- | --- | --- | --- | --- |
| Primary target |  |  |  |  |  |
| Outcome horizon |  |  |  |  |  |
| Minimum lookback |  |  |  |  |  |
| Label validation |  |  |  |  |  |
| External validation |  |  |  |  |  |

## Version Notes
Record major design changes here.

| Date | Change | Rationale |
| --- | --- | --- |
| YYYY-MM-DD |  |  |
