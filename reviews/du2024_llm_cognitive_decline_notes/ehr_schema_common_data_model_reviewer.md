# EHR Schema / Common Data Model Review: du2024_llm_cognitive_decline_notes

## Review Status

Complete.

## Data Model

Local MGB EHR note-section datasets. No common data model is central to the study.

## Structured Data Elements

Structured data are used for cohort anchoring through MCI diagnosis code G31.84.

## Unstructured Data Elements

Clinical note sections are the modeling unit. The paper also extracts LLM-reported keywords as interpretability artifacts.

## Temporal Structure

Four-year lookback before initial MCI diagnosis. No cardiology index encounter is defined.

## Portability Concerns

Model performance may vary with note style, prompt, LLM version, cloud configuration, and local annotation conventions.

## Use in Review

Use to discuss operational requirements for LLM use on EHR notes, including secure deployment and local evaluation.
