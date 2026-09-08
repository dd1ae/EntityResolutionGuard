# Case study: spec-git vs Spec Kit

## Trigger

User: «Ты слышал spec-git?»

Bad response: «Да. Spec-Git — это подход для spec-driven разработки…»

## Failure chain

1. Entity Resolution Error: unfamiliar spelling is silently mapped to a familiar entity.
2. Premature Assumption: the mapping is treated as established user intent.
3. Hallucination: an unsupported description is confidently attributed to the original name.

## Expected behavior

Resolve: preserve spec-git; consider GitHub Spec Kit as one possible candidate.
Verify: the [official github/spec-kit repository](https://github.com/github/spec-kit), consulted on 2026-09-08, identifies Spec Kit as a toolkit for spec-driven development.
Disambiguate: that source establishes the candidate, not what the user meant.
Answer: «Возможно, ты имеешь в виду GitHub Spec Kit? Если именно Spec-Git — уточни или дай ссылку».

If the user confirms github/spec-kit, answer from its documentation.
If the user rejects it, stop attributing Spec Kit properties to Spec-Git.
If browsing is unavailable, do not say the repository was checked.

## Regression links

See TYP-001, FALSE-001, REG-001 and REG-002 in tests/.
The project does not claim that every use of spec-git is a typo or that no separate Spec-Git exists.
