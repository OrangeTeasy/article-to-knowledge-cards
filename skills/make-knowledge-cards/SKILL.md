---
name: make-knowledge-cards
description: Convert pasted articles or local Markdown/TXT files into 5-8 concise, non-redundant knowledge cards. Use when a user wants the most important source-grounded ideas turned into study or review cards; do not use for web fetching, PDFs, Anki exports, or graphical interfaces.
---

# Make Knowledge Cards

Turn the supplied source into a small set of cards that preserve its most useful knowledge without adding outside facts.

## Accept the source

- Work from article text pasted in the conversation, or read a local `.md` or `.txt` file named by the user.
- Treat the supplied text as the sole factual source. Do not browse for context, fill gaps from memory, or silently reinterpret unsupported claims as facts.
- If a local path is missing, unreadable, or not Markdown/TXT, explain the limitation and ask for supported input. Do not process web pages, PDFs, Anki packages, or GUI workflows.

## Select the knowledge

Identify the article's central claim and the few ideas needed to understand or apply it. Prefer definitions, mechanisms, causal relationships, methods, distinctions, and conclusions that the source emphasizes or supports. Deprioritize scene-setting, rhetoric, repeated examples, incidental details, and claims that cannot stand alone.

Aim for 5-8 cards, but use fewer when the source contains fewer distinct, well-supported ideas. Never split one idea merely to reach the target count.

Before writing, consolidate candidates that teach the same point. Treat recap or summary sentences as confirmation of earlier material, not as new knowledge. Keep a claim together with a qualifier or rationale that is necessary to understand it; do not split tightly coupled material merely to increase the count. Each final card must:

- cover exactly one knowledge point;
- add material value beyond the other cards;
- be understandable without reproducing the whole article; and
- remain traceable to the supplied source.

## Write the cards

Use the source's language unless the user requests another language. Preserve important qualifications, uncertainty, scope, and causal direction. Paraphrase faithfully rather than copying long passages.

Return the cards as numbered Markdown headings. Give every card these four components, localizing the field labels to the output language:

```markdown
### 1. <title>

- **Core knowledge:** <one-sentence takeaway>
- **Brief explanation:** <what it means and why it matters according to the source>
- **Example or self-check:** <a source-grounded example, or a question answerable from this card>
```

Use an example only when the source supplies or directly supports it. Otherwise write a self-check question that tests the stated knowledge without introducing new factual premises. Do not present invented scenarios, statistics, quotations, people, mechanisms, or conclusions as source content.

## Final check

Verify that every factual statement is supported by the input, neighboring cards do not overlap, and each title names a specific idea. Remove any weak card rather than padding the set. If fewer than five cards remain, briefly state after the cards that the source did not support more distinct knowledge points.
