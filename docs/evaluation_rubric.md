# Evaluation Rubric

## Purpose

This rubric defines how AI-generated responses should be evaluated for factual quality, evidence support, usefulness, and risk. It is designed for manual AI Evaluation, Fact Checking, and Data Annotation workflows.

Each evaluated response should be reviewed at the claim level when possible. A claim is a statement that can be checked against evidence.

## Quality Criteria

### Factual Accuracy

Checks whether a claim is true, false, outdated, or unverifiable based on reliable evidence.

Questions to ask:

- Is the claim factually correct?
- Does it include correct names, dates, numbers, locations, and relationships?
- Does it avoid fabricated or exaggerated details?

### Evidence Support

Checks whether the response is supported by credible and relevant sources.

Questions to ask:

- Is there enough evidence to support the claim?
- Is the source reliable for the domain?
- Does the evidence directly support the exact wording of the claim?

### Completeness

Checks whether the response omits important context needed to understand the answer accurately.

Questions to ask:

- Is the answer missing a key limitation, condition, timeframe, or exception?
- Does the response oversimplify a complex issue?
- Would the user leave with an incomplete understanding?

### Relevance

Checks whether the response answers the user prompt without drifting into unsupported or unnecessary content.

Questions to ask:

- Does the response address the prompt?
- Are all major claims relevant to the user request?
- Does the answer avoid unrelated filler?

### Clarity

Checks whether the response is understandable, precise, and not misleading.

Questions to ask:

- Is the wording clear?
- Are ambiguous statements clarified?
- Does the response separate facts from uncertainty or interpretation?

### Safety and Caution

Checks whether the response handles sensitive topics responsibly.

Questions to ask:

- Does the response avoid unsupported medical, legal, financial, or safety advice?
- Does it include appropriate caution when evidence is uncertain or time-sensitive?
- Could a factual error cause practical harm?

## Review Expectations

For each evaluated claim, the reviewer should record:

- The claim text.
- The verdict label.
- The severity level.
- A short evidence summary.
- A source URL when evidence is available.
- A concise evaluator note in English.
- A corrected claim or response when needed.

Evaluator notes should connect the verdict, evidence, and correction. Avoid vague notes such as "bad answer" or "wrong." Use specific explanations.
