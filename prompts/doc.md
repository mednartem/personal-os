# /doc — Process a Document

## What to gather before running

1. Copy your `context/mental-model.md`
2. Copy the document you want to process (proposal, one-pager, design doc, etc.)

## Prompt — paste into Claude or Gemini

---

**CONTEXT — Mental Model:**
[paste context/mental-model.md here]

**DOCUMENT:**
[paste the document here]

---

Process this document to add standardized metadata and extract key insights.

Produce the document with a YAML header and a tl;dr block prepended:

```markdown
---
type: doc
date: [date — extract from doc or use today]
author: [author if mentioned]
status: #status/active
program: [which program this relates to]
tags: [#type/doc, relevant #topic/ tags]
---

## tl;dr
[3-5 bullet points: what is this, what problem it solves, what decision it supports, what action it requires]

---

[original document content below]
```

After adding the header, answer these questions in your response:
1. What is the core argument or proposal?
2. What decision does this document require from me or others?
3. Are there gaps, missing context, or weak assumptions worth flagging?

---

## Where to save output

`Docs/[descriptive-title].md`
