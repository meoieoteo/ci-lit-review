# EHR Schema / Common Data Model Review: wornow2023_shaky_foundations_ehr_fm

## Review Status

Complete.

## Data Model

The review covers models trained on heterogeneous EHR data sources. It notes that structured EHR foundation models face interoperability and model-sharing barriers.

## Structured Data Elements

Foundation models for EMRs commonly ingest sequences of structured codes, labs, medications, claims, and other temporally ordered events.

## Unstructured Data Elements

Clinical language models ingest clinical or biomedical text. The review notes heavy reliance on MIMIC-III and PubMed for many such models.

## Temporal Structure

Structured EHR foundation models represent patient histories as longitudinal event sequences, but the review emphasizes that evaluation tasks often do not demonstrate clinically useful temporal reasoning.

## Portability Concerns

Major concerns include private training data, lack of public weights for many FEMRs, different coding systems, and EHR-schema heterogeneity across health systems.

## Use in Review

Use to justify explicitly designing portable feature schemas and separating structured EHR, note-derived, and multimodal modeling claims.
