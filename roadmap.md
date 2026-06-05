# Fact-Checking AI Responses Project Roadmap

## Project Definition

This repository is a portfolio project focused on AI Evaluation, Fact Checking, and Data Annotation. The goal is to document a reproducible human evaluation workflow for reviewing AI-generated responses, identifying factual claims, checking evidence, assigning verdict labels, and writing clear corrections.

This is not a machine learning system. The project does not train a model, deploy an application, or automate fact checking in the initial scope.

## Phase 01 - Project Definition and Quality Criteria

Status: complete

Deliverables:

- Define the project objective and scope.
- Create an evaluation rubric.
- Define allowed verdict labels.
- Define severity levels.
- Keep the project positioned as AI response evaluation and fact-checking.

Completion criteria:

- The rubric is clear enough to evaluate a response consistently.
- Label definitions reduce ambiguity.
- Severity levels explain the practical impact of errors.

## Planned Phases

| Phase | Focus | Status |
| --- | --- | --- |
| 01 | Project definition and quality criteria | Complete |
| 02 | Initial repository setup | Complete |
| 03 | Dataset schema and annotation guidelines | Complete |
| 04 | Initial examples and claim extraction | Complete |
| 05 | Evidence review and labeling | In progress - Phase 05B complete |
| 06 | Corrected responses | Pending |
| 07 | Dataset validation and quality checks | Pending |
| 08 | Final documentation and portfolio publication | Pending |

## Scope

Included:

- Manual evaluation of AI-generated responses.
- Claim-level fact checking.
- Evidence-based verdict labels.
- Severity classification.
- Corrected claims or corrected response text.
- Professional documentation suitable for GitHub portfolio review.

Not included in the initial version:

- Machine learning model training.
- Automated evidence retrieval.
- Production deployment.
- API, dashboard, authentication, or user management.
- Professional legal, medical, financial, or safety advice.

## Portfolio Positioning

This project demonstrates:

- AI response evaluation.
- Factual accuracy review.
- Evidence-based annotation.
- Data labeling consistency.
- Technical writing.
- Critical thinking and quality judgment.

It should not be described as:

- A production fact-checking system.
- A machine learning model.
- An automated misinformation detector.
- A replacement for professional domain review.

## Phase 02 - Initial Repository Setup

Status: complete

Deliverables:

- Create a concise README for the portfolio project.
- Add `.gitignore` rules for local context, data, virtual environments, caches, credentials, and generated artifacts.
- Add a minimal `requirements.txt` for future validation scripts.
- Create the initial folder structure with `.gitkeep` placeholders.
- Document the data handling policy in `data/README.md`.

Completion criteria:

- The repository has a clean structure before dataset creation.
- Local roadmap context remains untracked.
- No raw data, processed data, generated artifacts, credentials, binaries, or heavy files are committed.

## Phase 03 - Dataset Schema and Annotation Guidelines

Status: complete

Deliverables:

- Create the official data dictionary for the annotation CSV.
- Create annotation guidelines for claim extraction, verdict decisions, evidence summaries, corrections, and reviewer notes.
- Create a source policy for reliable evidence selection.
- Add the header-only dataset template at `data/processed/ai_fact_checking_response_samples.csv`.

Completion criteria:

- The CSV schema is documented and matches the header row.
- Allowed verdict labels and severity levels are consistent with the rubric.
- A future evaluator can add new examples without needing undocumented assumptions.

## Phase 04A - Pilot Cases and Claim Extraction

Status: complete

Deliverables:

- Create five pilot fact-checking cases across technology, history, science, travel/geography, and culture/entertainment.
- Add one Markdown file per sample under `examples/`.
- Extract at least two clear, verifiable claims per sample.
- Keep claims unverified for now; no verdict labels, evidence summaries, source URLs, or corrections are assigned in this phase.

Completion criteria:

- Five pilot sample files exist.
- Each sample includes `sample_id`, `domain`, `user_prompt`, `ai_response_to_evaluate`, `extracted_claims`, and `notes_for_future_verification`.
- Claim IDs are unique and ready for future verification.

## Phase 04B - Second Batch of Pilot Cases

Status: complete

Deliverables:

- Create five additional pilot cases across health/general information, finance/general concepts, law/general information, environment/climate, and education/careers.
- Add one Markdown file per new sample under `examples/`.
- Extract a smaller focused set of 3-4 high-quality verifiable claims per sample.
- Keep claims unverified for now; no verdict labels, evidence summaries, source URLs, or corrections are assigned in this phase.

Completion criteria:

- Ten total pilot sample files exist.
- New samples each contain 3-4 extracted claims.
- Claim IDs remain unique across samples `FC001` through `FC010`.
- The CSV remains header-only until full verification fields are ready.

## Phase 04C - Third Batch of Pilot Cases

Status: complete

Deliverables:

- Create five additional pilot cases across public policy/civics, sports history, space/astronomy, consumer technology, and food/nutrition general information.
- Add one Markdown file per new sample under `examples/`.
- Extract exactly three important verifiable claims per new sample.
- Keep claims unverified for now; no verdict labels, evidence summaries, source URLs, or corrections are assigned in this phase.

Completion criteria:

- Fifteen total pilot sample files exist.
- New samples each contain exactly three extracted claims.
- Claim IDs remain unique across samples `FC001` through `FC015`.
- The CSV remains header-only until full verification fields are ready.

## Phase 04D - Final Draft Sample Batch

Status: complete

Deliverables:

- Create five final draft cases across transportation/urban mobility, economics/labor market, energy/sustainability, digital privacy/cybersecurity, and international organizations/global affairs.
- Add one Markdown file per new sample under `examples/`.
- Extract exactly three important verifiable claims per new sample.
- Keep claims unverified for now; no verdict labels, evidence summaries, source URLs, or corrections are assigned in this phase.

Completion criteria:

- Twenty total draft sample files exist.
- New samples each contain exactly three extracted claims.
- Claim IDs remain unique across samples `FC001` through `FC020`.
- The CSV remains header-only until full verification fields are ready.

## Phase 05A - First Evidence Review and Labeling Batch

Status: complete

Deliverables:

- Verify all extracted claims from `examples/sample_001.md` and `examples/sample_002.md`.
- Add completed CSV rows for claims `FC001-C01` through `FC002-C06`.
- Assign allowed verdict labels and severity levels.
- Add evidence summaries, source URLs, corrected claims or corrected responses when needed, evaluator notes, and `quality_check = reviewed`.

Completion criteria:

- Only claims from samples `FC001` and `FC002` are added to the CSV.
- CSV headers remain unchanged.
- All added rows use allowed verdict and severity values.
- Source URLs are present for all added rows.

## Phase 05B - Second Evidence Review and Labeling Batch

Status: complete

Deliverables:

- Verify all extracted claims from `examples/sample_003.md` and `examples/sample_004.md`.
- Append completed CSV rows for claims `FC003-C01` through `FC004-C07`.
- Assign allowed verdict labels and severity levels.
- Add evidence summaries, source URLs, corrected claims or corrected responses when needed, evaluator notes, and `quality_check = reviewed`.

Completion criteria:

- Phase 05A rows remain present and unchanged.
- Only claims from samples `FC003` and `FC004` are newly added to the CSV.
- CSV headers remain unchanged.
- All added rows use allowed verdict and severity values.
- Source URLs are present for all added rows.
