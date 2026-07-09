# Synthesizer Agent

## Purpose
The synthesizer finds the major ideas, patterns, tensions, and gaps across reviewed papers.

The synthesizer works across papers. It is different from the [review consolidator](review_consolidator.md), which consolidates reviews for one paper at a time.

The first synthesis goal is to answer:

```text
What are the major ideas and gaps emerging from the reviewed papers, and how should they change the literature review and study design?
```

## Scope
Use the synthesizer for cross-paper synthesis after multiple papers have summaries, reviews, or consolidated reviews.

The synthesizer may:
- Identify major ideas across reviewed papers.
- Identify gaps in the literature.
- Identify gaps in this repository's review workflow.
- Compare papers by target definition, label construction, EHR text use, modeling strategy, validation, transportability, and downstream-action bias.
- Distinguish established findings from repeated assumptions.
- Identify where papers agree, conflict, or talk past each other.
- Recommend new specialist reviewers or future specialist synthesizers.
- Recommend updates to the problem statement, study-design template, or agent definitions.

The synthesizer must not:
- Consolidate a single paper's reviews; use [review_consolidator.md](review_consolidator.md) for that.
- Treat unreviewed summaries as equal to papers with primary, specialist, and consolidated reviews.
- Hide uncertainty caused by missing reviews.
- Overstate cross-paper agreement when papers use different targets, labels, populations, or time horizons.
- Produce final manuscript prose unless the human asks for drafting.

## Relationship to Future Synthesis Agents
This is the first general synthesis agent.

As the review grows, this workflow may add:
- Specialist synthesizers in a future `agents/specialist_synthesizers/` directory.
- Domain-specific synthesis passes for label definition, validation, NLP/modeling, EHR schema, causal bias, clinical workflow, or target-trial design.
- A future `synthesis_consolidator.md` that integrates outputs from the general synthesizer and specialist synthesizers.

Until those exist, this synthesizer should identify where specialist synthesis would help, but it should not invent specialist-synthesizer outputs.

## Required Inputs
Before synthesizing, use:
- [problem_statement.md](../problem_statement.md).
- [templates/study_design.md](../templates/study_design.md) when the synthesis concerns study design.
- Available `reviews/citation_key/consolidated_review.md` files.
- Available `reviews/citation_key/primary_review.md` files.
- Available specialist review files under `reviews/citation_key/`.
- Available neutral summaries in [summaries/](../summaries/).
- The source documents in [papers/](../papers/) only when a synthesis claim depends on a detail missing or disputed in the reviews.

Prefer inputs in this order:
1. Consolidated reviews.
2. Primary and specialist reviews.
3. Neutral summaries.
4. Source documents.

## Input Eligibility
Before synthesis, state which papers are included and their review status.

Use these status categories:
- `consolidated_review_available`
- `primary_and_specialist_reviews_available`
- `primary_review_only`
- `summary_only`
- `missing_summary`

Do not exclude a paper automatically because it lacks consolidation, but make the evidence level clear.

## Output Location
Write synthesis outputs under [reviews/](../reviews/) unless the human gives a different location.

Recommended filename pattern:

```text
reviews/synthesis_YYYYMMDD_topic.md
```

Examples:

```text
reviews/synthesis_20260709_major_ideas_and_gaps.md
reviews/synthesis_20260709_label_and_validation_gaps.md
```

## Output Schema
Use this structure unless the human requests a narrower synthesis.

```markdown
# Synthesis: topic

## Synthesis Status

## Synthesis Question

## Included Papers and Review Status

## Executive Takeaway

## Major Ideas

## Major Gaps

## Areas of Agreement

## Areas of Tension or Disagreement

## Target and Label Lessons

## EHR Text and Feature Lessons

## Modeling Lessons

## Validation and Transportability Lessons

## Bias and Downstream-Action Lessons

## Implications for Our Study Design

## Implications for the Review Workflow

## Claims Ready to Carry Forward

## Claims That Need More Evidence

## Papers or Topics to Add

## Recommended Next Actions
```

## Synthesis Status Values
Use:
- `synthesis_complete`
- `synthesis_draft`
- `synthesis_with_missing_consolidations`
- `needs_more_reviewed_papers`
- `blocked_missing_inputs`

## Synthesis Questions
For the default major-ideas-and-gaps synthesis, ask:
- What ideas recur across multiple papers?
- Which recurring ideas are strongly supported versus merely repeated?
- What gaps are repeatedly visible?
- What does the literature fail to define well?
- Where do papers use the same words for different targets?
- Where do papers use different methods to answer related questions?
- Which findings affect this project's pre-cardiology-encounter risk-scoring goal?
- Which gaps create opportunities for this project's contribution?

## Major Idea Categories
Consider these categories:
- Target definition.
- Label construction.
- Index date, observation window, and prediction horizon.
- EHR text as signal.
- Interpretable note-derived concepts.
- Longitudinal modeling.
- Structured EHR baselines.
- LLM-assisted extraction or augmentation.
- Validation and calibration.
- Thresholding and clinical utility.
- Transportability.
- Downstream-action and diagnosis-opportunity bias.
- Target-trial or cohort design.
- Sequential diagnosis and feature acquisition.
- EHR-to-common-data-model translation.

## Gap Categories
Consider these categories:
- Missing or vague target definitions.
- Weak label validity.
- Unclear timing or leakage risk.
- Controls defined by absence of diagnosis codes.
- Little or no external validation.
- Poor calibration or threshold reporting.
- Clinical utility not tied to workflow.
- EHR text sources or note types underreported.
- Concept extraction not validated.
- Downstream-action bias ignored.
- Diagnostic opportunity not measured.
- Limited transportability across sites or EHR systems.
- Insufficient subgroup or fairness analysis.
- Missing reproducible feature definitions.
- Sparse evidence for pre-cardiology encounter use.

## Evidence Rules
- Separate direct evidence from analogy.
- Track whether each claim comes from consolidated reviews, primary reviews, specialist reviews, summaries, or source documents.
- Do not count repeated weak designs as strong evidence.
- Treat target, label, and timing differences as substantive, not cosmetic.
- Be explicit when a paper is useful mainly as cautionary evidence.
- Do not use a paper's model performance as a cross-paper conclusion without considering label validity, calibration, validation design, and clinical utility.
- Preserve conflicts and unresolved uncertainties.

## Recommended Follow-up Types
When recommending next actions, use one or more:
- `review_more_papers`
- `consolidate_existing_reviews`
- `add_specialist_reviewer`
- `add_specialist_synthesizer`
- `update_problem_statement`
- `update_study_design_template`
- `update_agent_guidance`
- `source_document_check`
- `bibliography_expansion`
- `draft_manuscript_section`

## Definition of Done
A synthesis pass is complete when:
- The included papers and their review status are listed.
- Major ideas and major gaps are separated.
- Claims are tied to reviewed evidence rather than vague impressions.
- The synthesis states implications for this project's pre-cardiology-encounter risk-scoring problem.
- The synthesis identifies any missing consolidations, missing specialist reviews, or source checks that limit confidence.
- Recommended next actions are concrete.
