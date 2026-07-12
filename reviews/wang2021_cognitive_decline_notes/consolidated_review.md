# Consolidated Review: wang2021_cognitive_decline_notes

## Consolidation Status

Complete.

## One-Sentence Takeaway

Wang et al. are strong peer-reviewed evidence that clinical notes contain detectable cognitive-decline signals before structured MCI diagnosis, though generalizability beyond the selected MCI cohort remains unproven.

## Bottom Line

This is an anchor paper for note-based cognitive-decline detection. It supports using unstructured notes and section-level NLP in the review's modeling strategy.

## What Cited For

- Cognitive decline can be documented in notes before structured MCI diagnosis.
- Clinical notes add information not captured by structured EHR fields.
- Deep learning and strong conventional NLP baselines outperform keyword search.
- A non-keyword-filtered reference set is important for evaluating note models.

## What Not Cited For

- External validation.
- General-population incident dementia prediction.
- Cardiology-specific screening.
- Clinical utility after deployment.

## Publication Status and Evidence Weight

Publication status: peer-reviewed. Evidence strength: high for note-based detection, moderate for prospective prediction.

## Evidence Strength

High internal validity for a single-system note-classification study; limited transportability evidence.

## Key Contributions

Clear cognitive-decline label, manual annotation with agreement reporting, two reference datasets, multiple baselines, and strong AUROC/AUPRC performance.

## Key Limitations

Single health system, no external validation, selected MCI cohort, section-level rather than patient-level outcome, and possible documentation-pattern dependence.

## Agreements

All reviewers agree this is highly relevant direct evidence for EHR-note modeling.

## Tensions

The study is temporally before MCI diagnosis but not a conventional prospective risk model because the source cohort is selected by later MCI diagnosis.

## Label/Target/Timing

The label captures evidence of progressive cognitive decline in note sections over the four years before initial MCI diagnosis.

## Validation/Transportability

Internal validation is strong; cross-system validation is absent.

## Bias/Downstream Action

Potential biases include documentation intensity, specialty access, and differential recognition of cognitive symptoms. Downstream screening utility is proposed, not tested.

## Implications

Any cognitive-risk model for cardiology should consider note-derived evidence and should evaluate text models beyond keyword search while preserving simple baselines.

## Claims to Carry Forward

- Notes can reveal cognitive decline before structured diagnosis.
- Keyword search can be sensitive but poorly precise.
- Section-level NLP can make long clinical notes tractable.

## Claims to Treat Cautiously

- External portability of the model.
- Applicability to patients without future MCI diagnosis.
- Necessity of deep learning over strong simpler baselines.

## Open Questions

How would this approach perform in an unselected cardiology population with a pre-encounter prediction horizon and patient-level outcomes?

## Recommended Next Action

Carry forward as a central note-based detection paper and pair it with validation/implementation literature.
