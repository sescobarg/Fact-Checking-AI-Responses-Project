# Data

This project will use a small, manually created dataset of AI response evaluation examples.

## Planned Data Structure

Data files may include:

- Raw seed prompts under `data/raw/`.
- Annotated fact-checking samples under `data/processed/ai_fact_checking_response_samples.csv`.

The main dataset schema contains prompts, AI responses, extracted claims, verdict labels, severity levels, evidence summaries, source URLs, evaluator notes, and corrected responses.

## Data Policy

Do not commit:

- Raw data.
- Generated processed data.
- Private prompts or sensitive examples.
- Credentials or source access tokens.
- Large binary artifacts.

Only `.gitkeep` placeholders, documentation, and reviewed annotation rows should be committed at this stage.

## Current Status

Phase 05B added reviewed CSV rows for samples `FC001` through `FC004`. Remaining draft samples will be verified in later phases.
