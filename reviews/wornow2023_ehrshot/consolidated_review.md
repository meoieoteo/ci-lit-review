# Consolidated Review: wornow2023_ehrshot

## Consolidation Status

Complete.

## One-Sentence Takeaway

EHRSHOT is a lower-publication-weight but useful structured-EHR benchmark showing that foundation models can help in few-shot settings while still requiring strong baselines and task-specific validation.

## Bottom Line

Use this paper for modeling-strategy context, especially few-shot evaluation and structured-EHR foundation-model benchmarking. Do not use it as dementia-specific evidence.

## What Cited For

- Few-shot evaluation design in longitudinal EHR data.
- Releasing benchmark tasks, code, and pretrained structured-EHR model weights.
- Evidence that foundation-model gains are strongest in low-label regimes and may disappear or reverse for some tasks.
- The need to compare against count-based GBM or similarly strong simple baselines.

## What Not Cited For

- Dementia prediction.
- Note-based cognitive-concern extraction.
- External transportability.
- Clinical utility or deployment readiness.

## Publication Status and Evidence Weight

Publication status: preprint. Evidence strength: indirect and lower publication weight.

## Evidence Strength

Moderate for benchmark-methodology motivation; low for clinical claims relevant to our population.

## Key Contributions

The paper defines a longitudinal structured-EHR benchmark with 15 tasks and evaluates a 141M-parameter structured-EHR transformer against count-based GBM across few-shot regimes.

## Key Limitations

No clinical notes, no dementia tasks, single institution, selected cohort, one foundation model, no external validation, and some very small positive test sets.

## Agreements

All reviewers agree it is useful for modeling strategy but indirect for the review's clinical question.

## Tensions

EHRSHOT advances reproducibility while still relying on access-controlled data and single-site validation.

## Label/Target/Timing

The paper is valuable for its explicit prediction times and horizons. Its targets are not cognitive-risk targets.

## Validation/Transportability

The benchmark has internal train/validation/test splits and few-shot evaluations. Transportability outside Stanford Medicine is unknown.

## Bias/Downstream Action

The extracted paper discusses privacy and governance more than fairness, calibration, or clinical action. It should not be cited for downstream benefit.

## Implications

For a pre-cardiology cognitive-risk model, EHRSHOT supports evaluating performance across label-scarce regimes and maintaining strong structured baselines. It also underscores that a model without clinical text may miss cognitive signals.

## Claims to Carry Forward

- Few-shot performance should be explicitly measured.
- Foundation models need strong simple baselines.
- Longitudinal structured-EHR modeling benefits from precise prediction-time definitions.

## Claims to Treat Cautiously

- Generalization of CLMBR-T-base to other institutions.
- Clinical usefulness of benchmark gains.
- Applicability to dementia or note-heavy phenotypes.

## Open Questions

Would a similar benchmark for cognitive-risk screening need notes, cognitive assessments, referral outcomes, and cardiology-specific index encounters?

## Recommended Next Action

Carry forward as indirect Section 8 support and pair with dementia-specific note and EHR prediction studies.
