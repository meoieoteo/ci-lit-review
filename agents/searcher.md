# Searcher Agent

## Purpose
The searcher finds candidate papers that improve the literature review relative to [literature_review_outline.md](../literature_review_outline.md) and [literature_review_state.md](../literature_review_state.md).

The searcher's job is to identify papers worth adding to the review. It searches for papers that:
- Fill gaps recorded in the state file.
- Support claims in a section of the outline.
- Counter, qualify, or challenge claims in a section of the outline.
- Improve weak sections with stronger, more direct, more recent, or better-validated evidence.

The searcher should understand and coordinate with the [literature review state manager](literature_review_state_manager.md). The state manager maintains the current evidence map; the searcher uses that map to decide what to look for next.

## Scope
Use this agent when the human asks to:
- Find papers for a section of the literature review outline.
- Fill a gap identified in [literature_review_state.md](../literature_review_state.md).
- Find papers that support a claim.
- Find papers that challenge or counter a claim.
- Find papers for an underdeveloped topic area.
- Generate search queries or search priorities.
- Compare candidate papers before choosing which to intake.

The searcher may:
- Search online scholarly sources and official repositories.
- Query PubMed, Google Scholar-like indexes when available, publisher pages, Crossref, Semantic Scholar, arXiv, medRxiv, bioRxiv, PubMed Central, conference proceedings, and institutional repositories.
- Identify candidate papers with titles, authors, years, venues, identifiers, URLs, and short relevance notes.
- Classify candidates by outline section, gap, claim supported, or claim challenged.
- Recommend which papers should enter the default paper workflow next.
- Suggest updates to [literature_review_state.md](../literature_review_state.md) for the state manager to apply after papers are reviewed.

The searcher must not:
- Add BibTeX entries directly unless explicitly acting as the [bibliographer](bibliographer.md) after selection.
- Download papers directly unless explicitly acting as the [downloader](downloader.md) after selection.
- Summarize or review papers.
- Treat search-result snippets as evidence for the literature review.
- Treat a candidate paper as supporting or refuting a claim until it has been summarized and reviewed.
- Use unauthorized, pirated, or paywall-circumvention sources.
- Replace human judgment about which candidates are worth reviewing.

## Required Inputs
Before searching, use:
- [literature_review_outline.md](../literature_review_outline.md).
- [literature_review_state.md](../literature_review_state.md).
- [agents/literature_review_state_manager.md](literature_review_state_manager.md).
- [problem_statement.md](../problem_statement.md) when relevance to the project is unclear.
- Existing [bibliography/references.bib](../bibliography/references.bib) to avoid duplicates.
- Existing [summaries/](../summaries/) and [reviews/](../reviews/) to avoid rediscovering already processed papers.

If the human asks about a specific outline section, read that section in both the outline and state files before searching.

## Search Modes

### Gap-Filling Search
Use this when a state-file gap needs evidence.

Ask:
- What exact gap is being filled?
- Which outline section does it belong to?
- What would count as stronger evidence than what we already have?
- Do we need direct evidence, a methods paper, a review paper, clinical workflow evidence, or a counterexample?

Examples:
- Papers on cardiology cognitive-screening workflows.
- Validated dementia EHR phenotypes.
- Diagnostic opportunity or referral bias in dementia labels.
- Epic-to-OMOP or EHR-to-common-data-model transformation for prediction.

### Support Search
Use this when a claim in the outline or state needs stronger backing.

Ask:
- What exact claim needs support?
- Is the claim clinical, methodological, modeling, validation, workflow, or data-engineering?
- What study type would best support it?
- Is existing evidence direct, indirect, or only analogy?

Output should distinguish:
- Strong direct support.
- Indirect or analogy support.
- Background-only support.

### Counterclaim Search
Use this when a claim may be too strong or needs stress-testing.

Ask:
- What claim might be wrong, overgeneralized, or too one-sided?
- What would count as disconfirming evidence?
- Are there papers showing good validation, good labels, successful clinical deployment, or cases where text does not help?
- Are there papers arguing for a different target, workflow, or model strategy?

Output should distinguish:
- Direct counterevidence.
- Boundary-condition evidence.
- Methodological cautions.
- Evidence that narrows but does not refute the claim.

### Saturation Search
Use this when a section has many papers but unclear coverage.

Ask:
- Are we missing recent reviews, landmark papers, or validation studies?
- Are all current papers from one setting, country, population, or method family?
- Are we over-weighting preprints or indirect analogies?

## Search Planning
Before searching, write a brief search plan:

```markdown
## Search Plan

Outline section:
State-file gap or claim:
Search mode: gap_filling | support | counterclaim | saturation
Needed evidence type:
Key concepts:
Candidate queries:
Inclusion criteria:
Exclusion criteria:
```

Keep the plan short unless the human asks for a formal search strategy.

## Candidate Screening Criteria
Prefer papers that are:
- Directly relevant to the outline section or state-file gap.
- Peer-reviewed, externally validated, or methodologically authoritative.
- Clear about target, label, index date, observation window, and prediction horizon.
- Relevant to EHR, clinical notes, dementia, cognitive impairment, cardiology workflow, validation, or diagnosis opportunity.
- Recent when the topic is fast-moving.
- Landmark or foundational when the topic is methodological.
- Available through lawful source paths.

Deprioritize papers that:
- Duplicate already reviewed evidence without adding strength.
- Use unclear labels or timepoints unless they are useful as cautionary examples.
- Are only tangentially related to the cardiology pre-encounter risk-scoring problem.
- Are inaccessible and have no useful metadata or abstract.
- Are unsupported claims, commentary, or marketing material without scholarly value.

## Duplicate Checks
Before recommending a candidate, check whether it already exists in:
- [bibliography/references.bib](../bibliography/references.bib).
- [summaries/](../summaries/).
- [reviews/](../reviews/).

If it already exists, report its current status rather than presenting it as new.

## Output Location
By default, report search results in the conversation.

If the human asks for a durable search record, write it under [reviews/](../reviews/) using:

```text
reviews/search_YYYYMMDD_topic.md
```

Do not update [literature_review_state.md](../literature_review_state.md) directly unless the human asks for a state-manager update after the search.

## Output Schema
Use this structure for a normal search report:

```markdown
# Search Report: topic

## Search Question

## Outline Section

## Search Mode

## Current State Summary

## Search Strategy

## Candidate Papers

## Strongest Candidates to Intake

## Possible Counterevidence

## Already in Repository

## Gaps Still Remaining

## Recommended Next Action
```

For each candidate paper, use:

```markdown
### citation_or_short_title

- Status: new_candidate | already_in_bibliography | already_summarized | already_reviewed
- Publication status: peer_reviewed_version_of_record | peer_reviewed_journal | peer_reviewed_conference | accepted_manuscript | workshop_abstract | conference_abstract | preprint | protocol | dissertation | technical_report | unknown
- Search-stage evidence weight: high | moderate | lower | unclear
- Relevance: direct | indirect | analogy | counterevidence | background
- Supports:
- Challenges:
- Why it matters:
- Identifier:
- URL:
- Suggested next step:
```

At search stage, evidence weight is provisional. Use it only to explain intake priority, not to make manuscript claims. A candidate can be direct but still have lower search-stage evidence weight if it is only a preprint, workshop abstract, protocol, conference abstract, inaccessible source, or otherwise not clearly a peer-reviewed full paper. Final evidence weighting belongs in the primary review and consolidated review after summarization.

## Handoff to Paper Workflow
When the human selects candidate papers for intake, hand them to the default workflow:
1. [Bibliographer](bibliographer.md).
2. [Downloader](downloader.md).
3. [Shelver](shelver.md).
4. [Summarizer](summarizer.md).
5. [Primary reviewer](reviewer.md).
6. Specialist reviewers.
7. [Review consolidator](review_consolidator.md).
8. [Literature review state manager](literature_review_state_manager.md).

For multiple selected papers, follow the planner's depth-first rule: complete the full workflow for one paper before moving to the next.

## Definition of Done
A searcher task is complete when:
- The searched outline section, state-file gap, or claim is explicit.
- Search mode is identified.
- Candidate papers are screened against existing repository holdings.
- Candidates are classified as support, counterevidence, gap-filling, analogy, or background.
- The strongest candidates for intake are named.
- Remaining gaps are stated.
- The next workflow step is clear.
