# /forte — Performance Review Generator

## What to gather before running

1. Copy your `context/mental-model.md` and `Goals.md`
2. Copy a representative sample of notes from the review period:
   - 3-5 weekly reports from `Reflections/Weekly/`
   - 3-5 significant meeting notes from `Meeting Notes/`
   - Any key docs from `Docs/`
3. If you have the performance review template or criteria your company uses, paste that too

## Prompt — paste into Claude or Gemini

---

**CONTEXT — Mental Model:**
[paste context/mental-model.md here]

**GOALS:**
[paste Goals.md here]

**NOTES FROM REVIEW PERIOD:**
[paste weekly reports, meeting notes, key docs here]

**REVIEW TEMPLATE / CRITERIA (if applicable):**
[paste company review template or leave blank]

---

Help me write a high-quality performance self-assessment based on this evidence. This should be grounded in specific examples from the notes, not generic claims.

Produce a draft self-assessment:

**Impact**
[What did I accomplish? Use specific dates, outcomes, and metrics where available. Link to goals.]

**How I Work**
[How did I approach problems, collaborate, and lead? Cite specific examples from the notes.]

**Growth**
[What did I get better at this period? What evidence shows it? Be honest about gaps too.]

**Next Period Goals**
[Based on my goals and what I learned, what should I focus on next?]

Rules:
- Every claim should be traceable to a specific example from the notes
- Use concrete language: dates, names, outcomes
- Don't inflate — reviewers can tell. Specificity is more compelling than superlatives
- If the notes reveal a gap between my goals and my actual work, flag it honestly

---

## Where to save output

`Docs/forte-[YYYY].md`
