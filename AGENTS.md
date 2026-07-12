AGENTS.md

## Objective
We are conducting a literature review of papers relevant to our [problem statement](problem_statement.md). Our goal in this repository is to accelerate and improve the quality of a literature review. We aim to do this with a workflow we define here and specialized agents that we define in the [agents/](agents/) directory.

## Expectations for this workflow and agent definition

1. We expect this literature review guidance to change as we get deeper into the literature. If you see a gap or error in the guidance, alert me.
2. We expect substantial Socratic interaction with the AI via the command line using these definitions.

## Directory layout
- [papers/](papers/) contains PDF downloads of the papers. This is not version controlled because the material may be copyrighted, and we may version this repo in a public origin.
- [summaries/](summaries/) contains AI-generated summaries of each paper and any supplemental material. We expect these summaries to change over time as we refine what we are looking for.
- [reviews/](reviews/) contains review outputs. Each reviewed paper gets its own subdirectory named with the BibTeX citation key.
- [literature_review_outline.md](literature_review_outline.md) contains the simple human-facing outline of the review.
- [literature_review_state.md](literature_review_state.md) tracks current evidence, gaps, and priorities relative to the outline.
- [bibliography/](bibliography/) contains the BibTeX of the complete set of references. We expect this to be a strict superset of what we actually reference in our papers.
- [ml_resources/](ml_resources/) contains practical educational resource guides for humans learning the core ML, NLP, EHR prediction, validation, and implementation technologies behind the review.
- [agents/](agents/) contains agent definitions for the literature-review workflow.

## Workflow
Agents are specified in the [agents/](agents/) directory. Again, we expect CLI interaction between human and bot here, so we do not have a single fixed workflow. Instead, assume that if the human wants to invoke the evolving set of agents, the first agent used is the `planner` agent, defined in [agents/planner.md](agents/planner.md).

The default paper workflow is layered:

1. The [bibliographer](agents/bibliographer.md) records the BibTeX metadata and citation key.
2. The [downloader](agents/downloader.md) retrieves the best lawful source document.
3. The [shelver](agents/shelver.md) stores the downloaded file using the citation key as the filename base.
4. The [summarizer](agents/summarizer.md) creates a neutral, reusable summary in [summaries/](summaries/).
5. The [primary reviewer](agents/reviewer.md) extracts review-relevant evidence and maps it to the [problem statement](problem_statement.md), writing to `reviews/citation_key/primary_review.md`.
6. Unless the human directs otherwise, every specialist reviewer in [agents/specialist_reviewers/](agents/specialist_reviewers/) runs and writes its own file under `reviews/citation_key/`.
7. The [review consolidator](agents/review_consolidator.md) integrates the primary and specialist reviews for that single paper, writing to `reviews/citation_key/consolidated_review.md`.

When processing multiple papers, complete this full lifecycle for one citation key before moving to the next citation key. Do not batch by workflow stage across papers unless the human explicitly requests that alternate traversal. In other words, avoid doing all summaries first, then all primary reviews, then all specialist reviews. The default traversal is paper-by-paper: summary, primary review, all specialist reviews, consolidation, then the next paper.

The summarizer and primary reviewer are intentionally separate. The summarizer describes the paper without judging it. The primary reviewer interprets how the paper contributes to this literature review. Specialist reviewers assess bounded dimensions such as clinical relevance, EHR schema implications, NLP/modeling, causal bias, validation quality, target-trial design, and skeptical review.

Cross-paper synthesis is handled by the [synthesizer](agents/synthesizer.md). The synthesizer looks across reviewed papers to identify major ideas, gaps, tensions, and implications for the review and study design. It is separate from the review consolidator, which works on one paper at a time.

The [literature review state manager](agents/literature_review_state_manager.md) maintains [literature_review_state.md](literature_review_state.md) relative to [literature_review_outline.md](literature_review_outline.md). Keep the outline simple; put evidence status, gaps, and priorities in the state file.

The [searcher](agents/searcher.md) uses the outline and state file to find candidate papers online that fill gaps, support claims, or challenge claims. Candidate papers selected by the human still enter the default paper workflow through the bibliographer, downloader, shelver, summarizer, reviewers, consolidator, and state manager.

The [ML resource curator](agents/ml_resource_curator.md) maintains practical learning guides in [ml_resources/](ml_resources/). These guides are for team education and implementation orientation, not evidence for manuscript claims. Prefer secondary explanatory resources, tutorials, textbooks, lectures, and official documentation; include original papers only when they are unusually instructive or directly tied to methods in the review.
