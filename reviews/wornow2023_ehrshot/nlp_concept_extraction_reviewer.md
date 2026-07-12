# NLP / Concept Extraction Review: wornow2023_ehrshot

## Review Status

Complete.

## NLP Task

No clinical-note NLP task is modeled directly. Chest-X-ray findings labels are derived with the CheXpert NLP labeler, but EHRSHOT does not release the underlying text and CLMBR-T-base does not process text.

## NLP Methods

Not applicable to the main model. CLMBR-T-base treats structured medical codes as tokens for autoregressive next-code prediction.

## Concept Handling

The model represents structured medical codes and events, not extracted note concepts.

## Strengths

The paper is useful as a contrast case: strong structured-EHR sequence modeling can be evaluated without notes, but this limits applicability to dementia settings where cognitive concerns are often documented in narrative text.

## Limitations

No note-section handling, negation detection, temporality extraction from text, cognitive-concern concept extraction, or dementia-specific NLP.

## Use in Review

Use to distinguish structured-code foundation models from note-based NLP models.
