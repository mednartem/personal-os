# /meeting — Process Meeting Notes

## What to gather before running

1. Copy your `context/mental-model.md` (full file)
2. Copy the raw meeting notes you want to process (the messy version — bullet points, fragments, whatever you typed)

## Prompt — paste into Claude or Gemini

---

**CONTEXT — Mental Model:**
[paste context/mental-model.md here]

**RAW MEETING NOTES:**
[paste your raw notes here]

---

Process these raw meeting notes into structured institutional memory. Use the context above to understand the participants, programs, and priorities involved.

Produce a note in this exact format:

```markdown
---
type: meeting
date: [extract from notes or ask me]
participants: [list names]
program: [which program/initiative this relates to]
tags: [#type/meeting, relevant #topic/ tags]
---

# Meeting: [descriptive title]

## Summary
[2-3 sentences: what was this meeting about and why did it matter]

## Key Decisions
[bullet list — be specific, include who decided]

## Action Items
- [ ] [Owner] — [specific action] — [due date if mentioned]

## Context / Backstory
[what someone needs to know to understand why this meeting happened]

## Open Questions
[anything unresolved that needs follow-up]
```

Rules:
- Extract decisions and action items even if they were implicit in the notes
- Attribute action items to specific owners — if unclear, note "(owner TBD)"
- Link program names using [[double brackets]] for Obsidian
- If a date, decision, or owner is missing and important, flag it with [MISSING: ...]

---

## Where to save output

`Meeting Notes/YYYY-MM-DD [Title].md`
