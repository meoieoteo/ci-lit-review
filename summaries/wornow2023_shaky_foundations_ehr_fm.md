---
citation_key: wornow2023_shaky_foundations_ehr_fm
title: "The Shaky Foundations of Large Language Models and Foundation Models for Electronic Health Records"
summary_status: complete
source_status: full_text_pdf
publication_status: peer_reviewed
paper_type: narrative_review
---

# Summary: wornow2023_shaky_foundations_ehr_fm

## Publication and Source Status

This is a peer-reviewed narrative review published in npj Digital Medicine in 2023. The downloaded source is the full-text PDF.

## Purpose

The paper reviews foundation models trained on non-imaging electronic medical record data and critiques how these models are evaluated. It distinguishes clinical language models, which operate on clinical or biomedical text, from foundation models for electronic medical records, which operate on structured longitudinal patient histories.

## Scope

The authors reviewed 84 clinical foundation models published before March 1, 2023: 50 clinical language models and 34 foundation models for electronic medical records. The review excludes imaging, genetics, and wearables.

The search and curation are explicitly narrative rather than systematic. The authors state that they followed citations and manually curated representative work to capture general field direction.

## Main Findings

The paper argues that clinical foundation models are often evaluated on tasks that do not establish their usefulness to health systems. Clinical language models are frequently trained on MIMIC-III and PubMed, and many are evaluated on traditional NLP tasks such as named entity recognition, relation extraction, and document classification. Foundation models for structured EMRs are often trained on small public datasets or single private health-system datasets, and few have public model weights.

The authors conclude that most evaluations demonstrate only improved predictive accuracy. Other claimed advantages of foundation models, such as sample efficiency, cheaper deployment, emergent clinical applications, multimodality, and novel human-AI interfaces, are much less often tested.

## Proposed Evaluation Framework

The review recommends evaluations that map to clinical value rather than generic benchmark performance. Suggested directions include top-K or ranking-based metrics under workflow capacity constraints, calibration and subgroup fairness, human evaluation for generated clinical content, explicit measurement of performance at small labeled sample sizes, cost/resource measures for deployment, multimodal evaluation tasks, and usability studies for prompt-based interfaces.

## Limitations

The paper is a narrative review, not a systematic review. It does not evaluate dementia-specific models, cardiology workflows, or specific patient-outcome interventions. Its findings are best used as methodological context for evaluating claims about clinical foundation models.

## Relevance to Review

This paper is useful for Section 8 on modeling strategy. It supports a cautious stance toward LLM and foundation-model claims in EHR prediction: performance metrics alone are insufficient, benchmark tasks may not align with clinical action, and complex models should be evaluated against simpler alternatives, local workflow constraints, calibration, subgroup performance, and transportability.
