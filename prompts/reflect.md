# /reflect — Daily Strategic Reflection

## What to gather before running

1. Copy your `context/mental-model.md` (full file)
2. Copy your `Goals.md` (full file)
3. Copy today's calendar — paste it as plain text (meeting titles + times is enough)
4. Copy your `Tasks.md` (full file)

## Prompt — paste into Claude or Gemini

---

**CONTEXT — Mental Model:**
[paste context/mental-model.md here]

**CONTEXT — Goals:**
[paste Goals.md here]

**TODAY'S CALENDAR:**
[paste today's meetings/blocks here]

**TASKS:**
[paste Tasks.md here]

---

You are helping me with my daily strategic reflection. Using the context above, guide me through the following:

1. **Time allocation check** — Based on my calendar today, which of my annual goals did this work advance? Which goals got no attention? Flag if a goal is being consistently starved.

2. **Alignment question** — Was today's work strategic or reactive? Be direct.

3. **Observations prompt** — Ask me: "What did you observe or learn today that's worth capturing?" (Wait for my answer before continuing.)

4. **Blockers** — Ask me: "What friction or blockers came up today?" (Wait for my answer.)

5. **Tomorrow's focus** — Based on my goals and what I shared, suggest the single most important thing I should work on tomorrow. Explain why.

6. **Output** — Write a clean daily reflection note in this format:

```markdown
---
type: reflection
horizon: daily
date: [today's date]
tags: [#type/reflection]
---

# Daily Reflection — [date]

## What I worked on

## Alignment with goals
[honest assessment]

## Observations / Learnings

## Blockers

## Tomorrow's priority
```

---

## Where to save output

`Reflections/Daily/YYYY-MM-DD.md`
