# /review-doc — Structured Feedback on a Document

## What to gather before running

1. Copy your `context/mental-model.md`
2. Copy the document you're reviewing

## Prompt — paste into Claude or Gemini

---

**CONTEXT — Mental Model:**
[paste context/mental-model.md here]

**DOCUMENT TO REVIEW:**
[paste the document here]

---

Help me provide high-quality, structured feedback on this document. Use my context to ensure the feedback aligns with my priorities, technical standards, and leadership principles.

Produce feedback in this format:

**Strengths**
[What works well? Be specific — name what the author did right and why it matters]

**Critical Gaps**
[What is missing, unclear, or wrong? These are things that must be addressed before this document is ready]

**Suggestions**
[Improvements that would make this stronger, but aren't blockers — specific and actionable]

**Key Question**
[The one question I should ask the author that gets to the heart of what this document is really deciding]

Rules:
- Be direct and specific — vague feedback is useless
- Distinguish between "this is wrong" and "this is a style preference"
- Match the feedback depth to the document's importance
- If I have relevant context from my mental model (e.g., this touches a program I own), bring it in

---

## Where to save output

`Docs/feedback-[doc-title].md`
