# EHR Schema / Common Data Model Review: wornow2023_ehrshot

## Review Status

Complete.

## Data Model

The benchmark uses structured Stanford Medicine EHR data processed with FEMR. The paper notes that the preprocessing pipeline can ingest EHRSHOT and datasets following the OMOP Common Data Model.

## Structured Data Elements

Data include demographics, diagnoses, procedures, laboratory results, medications, and other structured clinical events. The released benchmark contains 41.6 million events across 921,499 encounters.

## Unstructured Data Elements

Clinical text and images are excluded from the released benchmark. Chest-X-ray labels are derived from radiology text, but the text is not released.

## Temporal Structure

Strong. Patient records are longitudinal event sequences, and tasks define prediction times and horizons.

## Portability Concerns

The benchmark is single-institution and uses access-controlled Stanford data. The authors acknowledge unknown performance at other institutions.

## Use in Review

Useful for discussing longitudinal structured-EHR schemas and why a cognitive-risk model should define index time, lookback, horizon, and allowed feature modalities explicitly.
