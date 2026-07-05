AGENTS.md

## Objective
We are conducting a literature review of papers relevant to our [problem statement](problem_statement.md). Our goal in this repository is to accelerate and improve the quality of a literature review. We aim to do this with a workflow we define here and specialized agents that we define in the [agents/](agents/) directory.

## Expectations for this workflow and agent definition

1. We expect this literature review guidance to change as we get deeper into the literature. If you see a gap or error in the guidance, alert me.
2. We expect substantial Socratic interaction with the AI via the command line using these definitions.

## Directory layout
- [papers/](papers/) contains PDF downloads of the papers. This is not version controlled because the material may be copyrighted, and we may version this repo in a public origin.
- [summaries/](summaries/) contains AI-generated summaries of each paper and any supplemental material. We expect these summaries to change over time as we refine what we are looking for.
- [bibliography/](bibliography/) contains the BibTeX of the complete set of references. We expect this to be a strict superset of what we actually reference in our papers.

## Workflow
Agents are specified in the [agents/](agents/) directory. Again, we expect CLI interaction between human and bot here, so we do not have a single fixed workflow. Instead, assume that if the human wants to invoke the evolving set of agents, the first agent used is the `planner` agent, defined in [agents/planner.md](agents/planner.md).
