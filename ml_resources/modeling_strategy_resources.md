# ML Resources: Modeling Strategy

## Purpose
This guide gives the human team practical resources for understanding the core technologies behind the modeling ladder in [literature_review_outline.md](../literature_review_outline.md), Section 8.

This is an educational resource guide, not evidence for manuscript claims. Use the paper reviews and synthesis files for scientific evidence.

## How to Use This Guide
- Start with the recommended reading path rather than reading every resource.
- Use secondary explanations, textbooks, tutorials, and official documentation before original method papers.
- Use original papers only when they are unusually instructive or directly tied to methods already reviewed.
- Match the resource to the audience: MDs need conceptual orientation, data managers need data-shape and workflow implications, and modelers need implementation details.

## Recommended Reading Path

1. General predictive modeling: [An Introduction to Statistical Learning with Python](https://www.statlearning.com/) and the [scikit-learn User Guide](https://scikit-learn.org/stable/user_guide.html).
2. Clinical prediction workflow: [OHDSI PatientLevelPrediction](https://ohdsi.github.io/PatientLevelPrediction/) for OMOP-based patient-level prediction design.
3. Structured-data baselines: scikit-learn tree models, [XGBoost](https://xgboost.readthedocs.io/en/stable/), and [LightGBM](https://lightgbm.readthedocs.io/en/stable/).
4. NLP foundations: [Speech and Language Processing](https://web.stanford.edu/~jurafsky/slp3/) for tokens, embeddings, text classification, transformers, and language-model concepts.
5. Transformer implementation: [Hugging Face course/documentation](https://huggingface.co/learn/llm-course/chapter1/1), [Dive into Deep Learning](https://d2l.ai/), and [PyTorch tutorials](https://docs.pytorch.org/tutorials/).
6. Interpretability: Christoph Molnar's [Interpretable Machine Learning](https://christophm.github.io/interpretable-ml-book/), [SHAP documentation](https://shap.readthedocs.io/en/latest/), and [InterpretML documentation](https://interpret.ml/).
7. Clinical NLP implementation: [medspaCy](https://github.com/medspacy/medspacy) or similar clinical NLP tooling if sectioning, negation, temporality, and assertion detection become part of the pipeline.

## Resource Table

| Topic | Resource | Type | Audience | Stack | Why It Matters |
| --- | --- | --- | --- | --- | --- |
| General statistical learning | [An Introduction to Statistical Learning with Python](https://www.statlearning.com/) | textbook | mixed_team | Python | Best starting point for supervised learning, classification, resampling, regularization, tree methods, survival analysis, and Python labs. |
| Python ML implementation | [scikit-learn User Guide](https://scikit-learn.org/stable/user_guide.html) | official_documentation | modelers | Python, scikit-learn | Core library documentation for baselines, preprocessing, pipelines, cross-validation, metrics, thresholding, calibration, and model inspection. |
| Clinical prediction workflow | [OHDSI PatientLevelPrediction](https://ohdsi.github.io/PatientLevelPrediction/) | software_documentation | data_managers, modelers | R, OMOP/OHDSI | Useful design reference for reproducible EHR prediction in OMOP, even though it is not Python-first. |
| Structured-data boosting | [XGBoost documentation](https://xgboost.readthedocs.io/en/stable/) | official_documentation | modelers | Python, XGBoost | Strong baseline candidate for structured EHR features and note-derived concepts. |
| Structured-data boosting | [LightGBM documentation](https://lightgbm.readthedocs.io/en/stable/) | official_documentation | modelers | Python, LightGBM | Alternative gradient-boosting implementation for tabular structured-data baselines. |
| NLP foundations | [Speech and Language Processing](https://web.stanford.edu/~jurafsky/slp3/) | textbook | mixed_team | language-neutral | Clear explanations of tokens, embeddings, text classification, transformers, language models, and NLP evaluation. |
| Transformer/LLM implementation | [Hugging Face course/documentation](https://huggingface.co/learn/llm-course/chapter1/1) | course, official_documentation | modelers | Python, Hugging Face | Practical path for transformer models, tokenizers, fine-tuning, and model use. |
| Deep learning foundations | [Dive into Deep Learning](https://d2l.ai/) | textbook, tutorial | modelers | Python, PyTorch | Runnable explanations of neural networks, sequence models, attention, transformers, BERT, fine-tuning, and optimization. |
| PyTorch basics | [PyTorch tutorials](https://docs.pytorch.org/tutorials/) | official_documentation, tutorial | modelers | Python, PyTorch | Implementation foundation if custom neural models or transformer fine-tuning are used. |
| Interpretable ML | [Interpretable Machine Learning](https://christophm.github.io/interpretable-ml-book/) | textbook | mixed_team | language-neutral | Accessible overview of feature importance, partial dependence, SHAP, local explanations, and interpretation cautions. |
| Explanation tooling | [SHAP documentation](https://shap.readthedocs.io/en/latest/) | software_documentation | modelers | Python | Practical documentation for Shapley-style model explanations, including tabular and text examples. |
| Interpretable model tooling | [InterpretML documentation](https://interpret.ml/) | software_documentation | modelers | Python | Useful for glass-box models such as Explainable Boosting Machines and explanation workflows. |
| Clinical NLP implementation | [medspaCy](https://github.com/medspacy/medspacy) | software_documentation | modelers, data_managers | Python, spaCy/medspaCy | Candidate tooling for clinical note sectioning, context, and rule-based clinical NLP pipelines. |

## Topic Notes

### Structured Baseline Model
Start with scikit-learn and ISL. The team should understand logistic regression, penalized regression, random forests, gradient boosting, cross-validation, calibration, thresholding, and why simple baselines matter.

### Structured Data Plus Note-Derived Concepts
The relevant technology is often tabular modeling plus careful concept extraction. The team needs both clinical NLP resources and structured-data modeling resources.

### Structured Data Plus Note Embeddings
Use Speech and Language Processing, Hugging Face, Dive into Deep Learning, and PyTorch before reading original BERT-family papers.

### Longitudinal Sequence Model
Use Dive into Deep Learning for sequence models and transformers. Read RETAIN, BEHRT, and Med-BERT only after the team understands the basic sequence-model vocabulary.

### LLM-Assisted Extraction or Augmentation
Use Hugging Face and current official model/tool documentation for implementation basics. Keep the project distinction clear: LLM-assisted extraction is not the same as end-to-end risk scoring.

### Interpretable and Explainable ML
Use Molnar for concepts and SHAP/InterpretML for tooling. Treat explanations as aids for auditing and communication, not as proof that a model has learned the intended clinical construct.

## Original Papers Worth Reading
- `vaswani2017_attention_is_all_you_need`: read only after a secondary transformer explanation.
- BERT, ClinicalBERT, BioBERT, and GatorTron papers: useful after transformer basics, mainly to understand pretraining and domain adaptation.
- RETAIN, BEHRT, and Med-BERT papers: concrete EHR sequence-model examples.
- SHAP and Explainable Boosting Machine papers: useful after a general interpretability overview.

## Resources to Avoid or Treat Cautiously
- Vendor marketing pages that describe AI capabilities without methods, validation, or reproducible examples.
- Blog posts that lack dates, code, or clear authorship.
- Tutorials that skip validation, leakage, calibration, and thresholding.
- LLM demos that do not address protected health information, local validation, or clinical workflow.

## Gaps to Fill
- A concise clinical NLP guide focused specifically on sectioning, negation, temporality, assertion status, and annotation for EHR notes.
- A guide for Epic-to-OMOP or Epic-to-model-ready data transformation resources.
- A validation/calibration resource guide aimed at MDs and data managers.

## Maintenance Notes
- Check software documentation links before relying on them because library APIs and course pages change.
- Keep this guide secondary-resource-first.
- Promote highly project-specific resource collections into separate files under `ml_resources/` when this file becomes too broad.
