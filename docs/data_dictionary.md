# Data Dictionary

## Dataset Purpose

`data/processed/ai_fact_checking_response_samples.csv` is the main annotation file for this project. Each row represents one verifiable claim extracted from an AI-generated response.

When a single AI response contains multiple factual claims, repeat the shared `sample_id`, `domain`, `user_prompt`, and `ai_response` fields and assign a unique `claim_id` to each claim.

## Columns

| Column | Required | Description | Expected Values or Format |
| --- | --- | --- | --- |
| `sample_id` | Yes | Unique identifier for the prompt and AI response being evaluated. | `FC001`, `FC002`, etc. |
| `domain` | Yes | Topic area of the prompt. | Examples: `health`, `finance`, `history`, `technology`, `science`, `travel`, `law`, `culture` |
| `user_prompt` | Yes | Original user prompt that produced the AI response. | Plain text |
| `ai_response` | Yes | AI-generated response being reviewed. | Plain text |
| `claim_id` | Yes | Unique identifier for the claim within the sample. | `FC001-C01`, `FC001-C02`, etc. |
| `claim_text` | Yes | Verifiable factual claim extracted from the AI response. | One clear claim per row |
| `verdict` | Yes | Fact-checking decision for the claim. | `supported`, `refuted`, `unsupported`, `partially_supported`, `outdated`, `unclear` |
| `error_type` | Conditional | Type of factual or support issue found. | Examples: `none`, `fabricated_claim`, `wrong_date`, `unsupported_number`, `missing_context`, `outdated_information`, `misleading_wording`, `ambiguous_claim`, `safety_risk` |
| `severity` | Yes | Practical impact of the issue. | `low`, `medium`, `high`, `critical` |
| `evidence_summary` | Yes | Brief summary of what the evidence shows. | 1-3 concise sentences |
| `source_url` | Conditional | Source used to verify the claim. | URL; use multiple URLs only when necessary |
| `corrected_claim` | Conditional | Corrected version of the claim. | Required for `refuted`, `partially_supported`, `outdated`, and high-impact `unsupported` claims |
| `corrected_response` | Conditional | Corrected answer or corrected response fragment. | Required when the original response needs broader rewriting |
| `evaluator_note_en` | Yes | Reviewer note explaining the decision in English. | Concise professional English |
| `quality_check` | Yes | Review status for the row. | `pending`, `reviewed`, `needs_revision` |

## Label Rules

- Use only the verdict labels defined in `docs/label_definitions.md`.
- Use only the severity levels defined in `docs/label_definitions.md`.
- Use `error_type` as a short category, not a full explanation.
- Use `quality_check = pending` for newly drafted rows, `reviewed` for completed rows, and `needs_revision` when the row requires another pass.

## Data Handling Notes

- The CSV currently contains the official header row only.
- Real annotated examples will be added in later phases.
- Do not include credentials, private information, or heavy generated artifacts in the dataset.
