# Data

This project will use a small, manually created dataset of AI response evaluation examples in later phases.

## Planned Data Structure

Future data files may include:

- Raw seed prompts under `data/raw/`.
- Annotated fact-checking samples under `data/processed/`.

The main planned dataset will contain prompts, AI responses, extracted claims, verdict labels, severity levels, evidence summaries, source URLs, evaluator notes, and corrected responses.

## Data Policy

Do not commit:

- Raw data.
- Generated processed data.
- Private prompts or sensitive examples.
- Credentials or source access tokens.
- Large binary artifacts.

Only `.gitkeep` placeholders and documentation should be committed at this setup stage.

## Current Status

No dataset has been created in Phase 02. Dataset schema and annotation rules will be defined in Phase 03.
