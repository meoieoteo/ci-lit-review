# Consolidated Review: du2024_llm_cognitive_decline_notes

## Consolidation Status

Complete.

## One-Sentence Takeaway

Du et al. show that GPT-4 can classify cognitive-decline note sections, but local task-trained models remain competitive and an ensemble provides the strongest performance.

## Bottom Line

This paper is direct and timely for LLM modeling strategy. It argues against assuming standalone LLM superiority.

## What Cited For

- LLM evaluation on real EHR notes for cognitive decline.
- GPT-4 outperforming Llama 2 but not local models.
- Error-analysis prompting and ensemble gains.
- Complementary error profiles between LLMs and traditional models.

## What Not Cited For

- External generalizability.
- Standalone LLM superiority.
- Patient-level incident dementia prediction.
- Clinical utility.

## Publication Status and Evidence Weight

Publication status: peer-reviewed. Evidence strength: direct for model comparison; moderate for clinical claims.

## Evidence Strength

Moderate-to-high internally; limited externally.

## Key Contributions

The study updates a cognitive-note detection task for the LLM era and provides a practical comparison to locally trained models.

## Key Limitations

Same selected MCI-linked MGB dataset as Wang, no external validation, rapidly changing LLM versions, and limited ensemble testing.

## Agreements

All reviewers agree this is valuable direct evidence for Section 8.

## Tensions

LLMs are attractive for flexible reasoning, but the best result comes from combining them with local models rather than replacing local models.

## Label/Target/Timing

Section-level cognitive-decline evidence in notes from the four years before MCI diagnosis.

## Validation/Transportability

Internal testing is useful; transportability is unknown.

## Bias/Downstream Action

No workflow or outcome evaluation. LLM errors may differ from local-model errors, which can be useful but also complicates monitoring.

## Implications

For a cardiology cognitive-risk workflow, LLMs should be tested as components or adjudicators against local baselines, with secure deployment and version control.

## Claims to Carry Forward

- General-domain LLMs may not beat local task-trained models.
- Error profiles can be complementary.
- Ensembles may improve precision and recall.

## Claims to Treat Cautiously

- Performance stability across sites or model versions.
- Clinical benefit from LLM use.
- Applicability beyond the selected MCI cohort.

## Open Questions

Would an LLM add value in an unselected cardiology population when structured predictors and longitudinal notes are both available?

## Recommended Next Action

Carry forward as direct LLM comparison evidence and pair with Wang 2021 for the underlying label and dataset.
