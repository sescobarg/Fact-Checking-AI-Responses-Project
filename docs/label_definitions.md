# Label Definitions

## Verdict Labels

Use exactly one verdict label per evaluated claim.

| Label | Definition | Use When |
| --- | --- | --- |
| `supported` | Reliable evidence supports the claim. | The claim is accurate and directly backed by evidence. |
| `refuted` | Reliable evidence contradicts the claim. | The claim is false or materially wrong. |
| `unsupported` | Evidence is missing, insufficient, or not specific enough. | The claim may be plausible, but the available evidence does not support it. |
| `partially_supported` | Part of the claim is supported, but part is missing, overstated, or inaccurate. | The response mixes correct information with unsupported detail or missing nuance. |
| `outdated` | The claim may have been true before but is no longer current. | The information changed over time, such as product capabilities, laws, prices, leadership, or policies. |
| `unclear` | The claim is too ambiguous to evaluate confidently. | The wording is vague, lacks context, or can be interpreted in multiple ways. |

## Severity Levels

Use severity to describe the practical impact of an error or unsupported claim.

| Severity | Definition | Example Impact |
| --- | --- | --- |
| `low` | Minor issue that does not meaningfully change the answer. | Small wording issue, minor missing context, or harmless imprecision. |
| `medium` | Noticeable issue that could mislead the user. | Incorrect supporting detail, incomplete explanation, or unsupported generalization. |
| `high` | Important issue affecting a central claim or conclusion. | Wrong date, wrong entity, unsupported statistic, or materially misleading recommendation. |
| `critical` | Error could cause serious harm or major misunderstanding, especially in sensitive domains. | Unsafe medical, legal, financial, security, or emergency-related claim. |

## Labeling Guidelines

- Use `supported` only when evidence directly backs the claim.
- Use `refuted` when evidence clearly contradicts the claim.
- Use `unsupported` when the claim lacks evidence, even if it sounds plausible.
- Use `partially_supported` when the claim combines correct and incorrect or incomplete elements.
- Use `outdated` for time-sensitive claims that are no longer accurate.
- Use `unclear` when the claim must be rewritten before it can be checked.

## Sensitive Domains

Claims in health, law, finance, public safety, or security require extra caution. Unsupported or incorrect claims in these domains should usually receive higher severity because user harm is more likely.

## Correction Rules

Corrections should:

- Remove unsupported details.
- Add necessary context or limitations.
- Preserve useful supported information.
- Avoid making stronger claims than the evidence allows.
- Use cautious wording when evidence is limited or time-sensitive.
