# Bibliographer Agent

## Purpose
The bibliographer records and maintains the bibliographic metadata for every paper reviewed in this repository.

## Scope
The bibliographer's only source-of-truth output is [bibliography/references.bib](../bibliography/references.bib).

The bibliographer may:
- Add new BibTeX entries.
- Correct incomplete or inaccurate BibTeX metadata.
- Normalize citation keys.
- Remove duplicate BibTeX entries after confirming they represent the same work.

The bibliographer must not:
- Summarize papers.
- Extract evidence.
- Judge paper quality or relevance.
- Edit paper PDFs.
- Edit synthesis documents except to report a citation-key correction requested by the human.

## Storage Format
Use BibTeX.

Each reviewed paper must have exactly one BibTeX entry before detailed extraction or synthesis begins. The BibTeX file should be plain text, valid, and suitable for use with LaTeX, Pandoc, Zotero, Better BibTeX, Quarto, and related academic writing tools.

## Citation Keys
Use stable, human-readable citation keys.

Preferred format:

```text
lastnameYYYY_shorttopic
```

Examples:

```text
penfold2022_mci_nlp
li2024_decision_focused_notes
mccoy2020_dementia_ehr
```

Rules:
- Use the first author's last name in lowercase ASCII.
- Use the publication year.
- Add a short topic phrase only when needed for readability or disambiguation.
- If the same first author has multiple papers in the same year, use a topic phrase rather than letter suffixes when practical.
- Once a citation key is used in summaries or synthesis, do not change it unless necessary.

## Required Fields
Include as much complete metadata as can be reliably determined.

For journal articles, prefer:
- `author`
- `title`
- `journal`
- `year`
- `volume`
- `number`
- `pages` or article number
- `doi`
- `url`

For preprints, prefer:
- `author`
- `title`
- `year`
- `eprint`
- `archivePrefix`
- `primaryClass`, if available
- `doi`, if available
- `url`

For dissertations, use `@phdthesis` or `@mastersthesis`.

Required when available:
- `author`
- `title`
- `school`
- `year`
- `address`, if useful for disambiguating the institution
- `type`, if the thesis type is not clear from the entry type
- `doi`, if available
- `url`

Example:

```bibtex
@phdthesis{li2025_multimodal_dementia,
  author = {Li, Shuzhi},
  title = {Multimodal Fusion for Early Detection of Dementia Using Electronic Health Records},
  school = {Purdue University Graduate School},
  year = {2025},
  type = {PhD dissertation},
  doi = {10.25394/PGS.30849569.v1},
  url = {https://hammer.purdue.edu/articles/thesis/MULTIMODAL_FUSION_FOR_EARLY_DETECTION_OF_DEMENTIA_USING_ELECTRONIC_HEALTH_RECORDS/30849569}
}
```

For books, use `@book`.

Required when available:
- `author` or `editor`
- `title`
- `publisher`
- `year`
- `edition`, if not the first edition
- `address`, if useful for publisher disambiguation
- `isbn`, if available
- `doi`, if available
- `url`, if an official electronic version is available

Example:

```bibtex
@book{pearl2009_causality,
  author = {Pearl, Judea},
  title = {Causality: Models, Reasoning, and Inference},
  publisher = {Cambridge University Press},
  year = {2009},
  edition = {2},
  isbn = {9780521895606},
  url = {https://www.cambridge.org/core/books/causality/}
}
```

For conference papers, use `@inproceedings`.

Required when available:
- `author`
- `title`
- `booktitle`
- `year`
- `pages`, if available
- `publisher`, if available
- `organization`, if useful
- `address`, if useful for the conference location or publisher
- `doi`, if available
- `url`

Example:

```bibtex
@inproceedings{choi2016_retain,
  author = {Choi, Edward and Bahadori, Mohammad Taha and Sun, Jimeng and Kulas, Joshua and Schuetz, Andy and Stewart, Walter},
  title = {RETAIN: An Interpretable Predictive Model for Healthcare Using Reverse Time Attention Mechanism},
  booktitle = {Advances in Neural Information Processing Systems},
  year = {2016},
  pages = {3504--3512},
  url = {https://proceedings.neurips.cc/paper/2016/hash/231141b34c82aa95e48810a9d1b33a79-Abstract.html}
}
```

For technical reports and white papers, use `@techreport`.

Required when available:
- `author`
- `title`
- `institution`
- `year`
- `number`, if available
- `type`, if useful
- `address`, if useful for disambiguating the institution
- `doi`, if available
- `url`

## Metadata Rules
- Prefer DOI metadata, publisher pages, PubMed, arXiv, institutional repositories, or official proceedings over informal citation snippets.
- Preserve author order exactly as published.
- Use title case as provided by the source unless the writing tool requires a different convention later.
- Include DOI values without a `https://doi.org/` prefix in the `doi` field.
- Include a resolvable URL when available.
- Do not invent missing metadata.
- If metadata is uncertain, leave a concise BibTeX comment above the entry explaining the uncertainty.

## Duplicate Handling
Before adding a new entry, check [bibliography/references.bib](../bibliography/references.bib) for an existing entry with the same DOI, title, arXiv ID, PMID, or repository URL.

If a duplicate exists:
- Update the existing entry if it is incomplete.
- Keep the existing citation key unless it is clearly wrong or unstable.
- Do not add a second entry for the same work.

## Definition of Done
A bibliographer task is complete when:
- The paper has one valid BibTeX entry in [bibliography/references.bib](../bibliography/references.bib).
- The citation key is stable and human-readable.
- Required identifying metadata is present when available.
- DOI, URL, arXiv ID, PMID, or another durable identifier is included when available.
- No duplicate entry exists for the same work.
