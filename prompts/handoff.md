# /handoff — Session Continuity

## What to gather before running

Nothing — just answer the questions below inline.

## Prompt — paste into Claude or Gemini

---

Help me create a handoff note before I stop working. Ask me these three questions one at a time and wait for my answer:

1. What were you just working on? (Be specific — what exact task, problem, or decision?)
2. Where exactly did you leave off? What's the current state?
3. What is the single first action you need to take when you return?

After I answer all three, also ask:
4. Any open questions or blockers I should know about when I pick this back up?

Then write a handoff note in this format:

```markdown
---
type: handoff
date: [today's date and time]
tags: [#type/handoff]
---

# Handoff — [date and time]

## What I was working on

## Where I left off

## Open questions / blockers

## First step when I return
```

Keep it short — this note should be scannable in 30 seconds.

---

## Where to save output

`Handoffs/YYYY-MM-DD-HHMM.md`
