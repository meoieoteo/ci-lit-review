# Consolidated Review: hong2020_cognitive_concerns_nlp

## Consolidation Status

Complete.

## One-Sentence Takeaway

Hong et al. offer direct proof-of-concept evidence that progress-note NLP improves cognitive-concern detection over structured EHR features, but the study's short format, small test set, and limited validation keep its evidentiary weight modest.

## Bottom Line

This is a useful direct paper for the modeling-strategy section. It should be cited for the importance of unstructured notes and for the value of simple NLP baselines, not for deployment-ready dementia prediction.

## What Cited For

- EHR notes contain cognitive-concern information missed by ICD codes and dementia medications.
- Simple note-based models can substantially improve sensitivity over structured features.
- Transformer models may perform best, but gains over TF-IDF or regular-expression approaches may be small in limited data.

## What Not Cited For

- External validity.
- Prospective dementia prediction.
- Cardiology-specific cognitive risk.
- Clinical utility or implementation benefit.
- A validated dementia-stage label.

## Publication Status and Evidence Weight

Publication status: workshop abstract / arXiv preprint. Evidence strength: direct but lower publication weight.

## Evidence Strength

Moderate for proof-of-concept note relevance; low for clinical deployment and transportability.

## Key Contributions

The paper provides a clean comparison of structured-only features, rule/term-based NLP, and transformer-based note classification for cognitive concerns.

## Key Limitations

Small single-system dataset, small held-out test set, broad label, possible leakage from same-window notes, no external validation, no calibration, and no clinical workflow evaluation.

## Agreements

All reviewers agree that the paper is directly relevant to cognitive-note phenotyping and should be down-weighted for publication and validation limitations.

## Tensions

The strongest topical fit comes from a paper with weak publication depth. The transformer result is appealing, but the simpler NLP baselines are nearly as informative and more transparent.

## Label/Target/Timing

The target is clinician-adjudicated cognitive concern during the same year as input extraction. This is not a prospective pre-encounter prediction design.

## Validation/Transportability

Validation is limited to a small random held-out test set in one health system. Transportability is unknown.

## Bias/Downstream Action

Models may detect documentation and access patterns as much as underlying cognitive state. Downstream action is proposed but not tested.

## Implications

For our review, this paper supports designing models that include clinical text and benchmark against simple lexical methods before relying on more complex LLM/transformer approaches.

## Claims to Carry Forward

- Structured dementia proxies can miss patients with cognitive impairment signals.
- Note-derived features can materially improve detection sensitivity.
- Transparent NLP baselines deserve serious consideration.

## Claims to Treat Cautiously

- Longformer superiority.
- Generalizable performance.
- Utility for early detection or pre-cardiology screening.

## Open Questions

Would the same gains hold under temporal validation, external-site validation, and a cleaner prediction horizon before a cardiology encounter?

## Recommended Next Action

Carry forward as direct but lower-weight evidence in Section 8. Pair it with stronger peer-reviewed dementia EHR studies and broader clinical NLP validation literature.
