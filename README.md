# Fact-Checking AI Responses Project

Portfolio project focused on AI Evaluation, Fact Checking, and Data Annotation.

## Project Overview

This project documents a structured workflow for evaluating AI-generated responses. The goal is to identify factual claims, compare them against evidence, assign verdict labels, classify severity, and propose corrected wording when needed.

This is not a machine learning system. The first version focuses on human evaluation quality, annotation consistency, clear documentation, and simple future validation checks.

## Business and Professional Context

AI-generated answers can sound fluent while still containing unsupported claims, incorrect dates, outdated details, or missing context. This repository is designed to show a practical review process for detecting those issues and documenting corrections in a reproducible way.

The project is relevant to:

- AI response evaluation.
- Fact checking.
- Data annotation.
- Prompt and response review.
- Evidence-based quality assessment.

## Current Status

Phase 03 is complete. The repository now includes the dataset schema, annotation guidelines, source policy, and an empty CSV template for future fact-checking examples. Sample cases and validation scripts will be added in later phases.

## Repository Structure

```text
fact-checking-ai-responses-project/
|-- data/
|   |-- raw/
|   |-- processed/
|   |-- README.md
|-- docs/
|   |-- annotation_guidelines.md
|   |-- data_dictionary.md
|   |-- evaluation_rubric.md
|   |-- label_definitions.md
|   |-- source_policy.md
|-- examples/
|-- notebooks/
|-- reports/
|   |-- figures/
|-- src/
|-- tests/
|-- README.md
|-- requirements.txt
|-- roadmap.md
```

## Documentation

- `roadmap.md`: project phases and scope.
- `docs/annotation_guidelines.md`: process for extracting claims, assigning verdicts, and writing evaluator notes.
- `docs/data_dictionary.md`: official dataset columns and expected values.
- `docs/evaluation_rubric.md`: quality criteria for factual evaluation.
- `docs/label_definitions.md`: allowed verdict labels and severity levels.
- `docs/source_policy.md`: rules for choosing reliable sources.
- `data/README.md`: data handling policy and expected future dataset location.

## Data Policy

Raw data, generated reports, credentials, binaries, and heavy artifacts should not be committed. The header-only dataset template at `data/processed/ai_fact_checking_response_samples.csv` is tracked so future annotations follow a consistent schema.

## Planned Next Work

Phase 04 will add the first sample cases and extract verifiable claims using the Phase 03 annotation structure.
