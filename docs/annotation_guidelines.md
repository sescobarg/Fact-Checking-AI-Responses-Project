# Annotation Guidelines

## Purpose

These guidelines define how to create consistent fact-checking examples for AI-generated responses. The project is designed for AI Evaluation, Fact Checking, and Data Annotation, not machine learning model training.

## Annotation Workflow

1. Read the user prompt and the full AI response.
2. Extract factual claims that can be checked against evidence.
3. Write each claim as a clear standalone statement.
4. Search for reliable evidence using the source policy.
5. Assign one verdict label and one severity level per claim.
6. Write a concise evidence summary and evaluator note in English.
7. Add a corrected claim or corrected response when the original wording is false, unsupported, outdated, or misleading.
8. Mark the row with the appropriate `quality_check` status.

## Claim Extraction Rules

- Extract only claims that can be verified or meaningfully checked.
- Split compound statements into separate claims when each part may need a different verdict.
- Do not create rows for opinions, style preferences, or generic advice unless they contain factual assertions.
- Preserve the meaning of the original response, but rewrite the claim into a clear standalone sentence when needed.
- Use stable IDs such as `FC001-C01`, `FC001-C02`, and so on.

## Verdict Decision Rules

- Use `supported` when reliable evidence directly backs the claim.
- Use `refuted` when reliable evidence clearly contradicts the claim.
- Use `unsupported` when the claim lacks adequate evidence or the response provides a claim that cannot be verified from reliable sources.
- Use `partially_supported` when the claim mixes accurate information with missing context, overstatement, or a partially wrong detail.
- Use `outdated` when the claim may have been accurate before but is no longer current.
- Use `unclear` when the claim is too vague or ambiguous to evaluate confidently.

## Evidence Summary Rules

- Summarize what the source shows, not just that a source exists.
- Keep the summary concise and specific to the claim.
- Mention uncertainty, date sensitivity, or scope limits when relevant.
- Do not overstate evidence. If the source only supports part of the claim, use `partially_supported`.

## Source URL Rules

- Prefer primary or authoritative sources for the domain.
- Use sources that directly support or contradict the exact claim.
- Avoid relying on AI-generated responses, unsourced blog posts, or low-quality aggregators.
- For time-sensitive claims, use current sources and note the date context in the evidence summary when useful.

## Correction Rules

- Corrected claims should be factual, precise, and aligned with the evidence.
- Remove unsupported details instead of replacing them with another unsupported claim.
- Use cautious wording for uncertain or time-sensitive information.
- Avoid causal language unless the source clearly supports causality.

## Evaluator Notes

Write `evaluator_note_en` in clear professional English. The note should connect:

- the verdict,
- the evidence,
- the issue in the original claim,
- and the reason for any correction.

Avoid vague notes such as "wrong" or "bad answer."

## Quality Check Status

Use:

- `pending` when the row is drafted but not fully reviewed.
- `reviewed` when the claim, evidence, labels, and corrections have been checked.
- `needs_revision` when the row has missing evidence, unclear wording, inconsistent labels, or unresolved review questions.
