# Workflow Reference

Each workflow has a corresponding prompt file in `prompts/`, a Claude Code command in `.claude/commands/`, and a Gemini CLI command in `.gemini/commands/`.

---

## /reflect — Daily Strategic Reflection

**Purpose:** End each workday with a short structured check — did today's work actually move your goals forward?

**When to use:** At the end of the workday. Takes 10-15 minutes.

**What to paste in:** Today's calendar + Tasks.md + mental-model.md + Goals.md

**Output:** `Reflections/Daily/YYYY-MM-DD.md`

**Sections:** What I worked on / Alignment with goals / Observations / Blockers / Tomorrow's priority

---

## /meeting — Process Meeting Notes

**Purpose:** Turn raw, messy notes into structured institutional memory with clear decisions and action items.

**When to use:** Within 1 hour of a meeting ending, while context is fresh.

**What to paste in:** Raw meeting notes + mental-model.md

**Output:** `Meeting Notes/YYYY-MM-DD [Title].md`

**Sections:** Summary / Key Decisions / Action Items / Context / Open Questions

---

## /doc — Process a Document

**Purpose:** Add standardized metadata and extract key insights from a document.

**When to use:** When you receive or write a proposal, one-pager, or design doc.

**What to paste in:** Document text + mental-model.md

**Output:** `Docs/[title].md` with YAML header and tl;dr prepended

---

## /handoff — Session Continuity

**Purpose:** Capture your brain state before stopping work so you can resume without ramp-up time.

**When to use:** Before ending a work session — daily, or whenever switching contexts.

**What to paste in:** Nothing — just answer 4 questions inline.

**Output:** `Handoffs/YYYY-MM-DD-HHMM.md`

---

## /resume — Pick Up Where You Left Off

**Purpose:** Minimize ramp-up time when returning to work.

**When to use:** At the start of a work session.

**What to paste in:** Most recent file from `Handoffs/`

**Output:** Read in chat — context summary + immediate next action.

---

## /weekly-report — Weekly Synthesis

**Purpose:** Surface patterns and assess the week's progress against goals.

**When to use:** Friday afternoon.

**What to paste in:** All daily reflections from the week + Goals.md

**Output:** `Reflections/Weekly/YYYY-Wnn.md`

**Sections:** Highlights / Progress vs Goals / Patterns / Blockers / Next Week's Priority

---

## /monthly-synthesis — Monthly Pattern Analysis

**Purpose:** Find patterns invisible week-to-week. Adjust course for the next month.

**When to use:** Last workday of the month.

**What to paste in:** All weekly reports from the month + Goals.md

**Output:** `Reflections/Monthly/YYYY-MM.md`

**Sections:** Month in one sentence / Progress vs annual goals / Themes / Time allocation check / What needs to change

---

## /follow-up-email — Meeting Recap Email

**Purpose:** Send a professional, accurate recap to meeting participants immediately after.

**When to use:** Within 2 hours of a meeting.

**What to paste in:** Processed meeting note + mental-model.md (writing style section)

**Output:** Draft email — copy from chat into your email client.

---

## /follow-up-meeting — Draft Calendar Invite

**Purpose:** Maintain momentum by booking the next touchpoint with a proper agenda.

**When to use:** After a meeting that clearly needs a follow-up.

**What to paste in:** Processed meeting note + your availability

**Output:** Draft calendar invite — copy from chat into your calendar.

---

## /review-doc — Structured Feedback

**Purpose:** Provide high-quality, consistent feedback on others' work.

**When to use:** When asked to review a proposal, design doc, or one-pager.

**What to paste in:** Document to review + mental-model.md

**Output:** `Docs/feedback-[title].md` with Strengths / Critical Gaps / Suggestions / Key Question

---

## /coaching-prep — 1:1 Readiness

**Purpose:** Enter coaching or 1:1 conversations with full context — skip the catch-up phase.

**When to use:** 10-15 minutes before a 1:1 or coaching conversation.

**What to paste in:** Person's hub page + recent meeting notes involving them + mental-model.md

**Output:** Read in chat — cheat sheet with context, open items, suggested questions.

---

## /forte — Performance Review Generator

**Purpose:** Write a high-quality self-assessment grounded in real evidence, not memory.

**When to use:** Before performance review season. Run it once, refine from there.

**What to paste in:** mental-model.md + Goals.md + representative notes from the review period (weekly reports, key meeting notes, key docs)

**Output:** `Docs/forte-YYYY.md` — draft self-assessment ready to adapt to your company's template.

---

## /annual-review — Annual Review

**Purpose:** Reflect on the full year — what worked, what didn't, what to carry forward.

**When to use:** Last week of December or first week of January.

**What to paste in:** All monthly syntheses from the year + Goals.md

**Output:** `Reflections/Annual/YYYY.md`

**Sections:** Year in one sentence / Progress vs annual goals / Themes / What grew / What didn't work / What I'd do differently / Heading into next year
