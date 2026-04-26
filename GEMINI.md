# Personal OS — Gemini CLI Context

This folder is an Obsidian vault and personal operating system for a knowledge worker. It is not a software project.

## What this is

A structured system for aligning daily work with long-term goals. Your job is to help the user run workflows — reflecting, processing meeting notes, synthesizing patterns, drafting communications — all grounded in the user's personal context files.

## Key files to always read before any workflow

- `context/mental-model.md` — who the user is, their goals, writing style, org context
- `context/taxonomy.md` — tag and linking conventions for this vault
- `Goals.md` — annual and quarterly goals

## Vault structure

```
context/          The user's context — read this before generating anything
prompts/          Copy-paste prompts for Claude or Gemini (manual workflow)
Templates/        Obsidian note templates
setup/            One-time onboarding files
examples/         Anonymized role examples (developer, manager, ic-qa)
reference/        Reference documentation
Meeting Notes/    Processed meeting notes
Reflections/      Daily, weekly, monthly, annual reflections
Docs/             Processed documents, feedback, performance reviews
My Team/          Hub pages for direct reports
Stakeholders/     Hub pages for partners and stakeholders
Programs/         Hub pages for initiatives
Handoffs/         Session continuity notes
Goals.md          Annual and quarterly goals
Tasks.md          Central task list
```

## Available slash commands

| Command | What it does |
|---|---|
| `/reflect` | Daily strategic reflection — reads Goals.md + Tasks.md, writes to Reflections/Daily/ |
| `/meeting` | Process raw meeting notes — writes structured note to Meeting Notes/ |
| `/handoff` | Session continuity — writes to Handoffs/ |
| `/resume` | Pick up from last handoff — reads most recent Handoffs/ file |
| `/weekly-report` | Weekly synthesis — reads this week's daily reflections, writes to Reflections/Weekly/ |
| `/monthly-synthesis` | Monthly pattern analysis — reads this month's weekly reports, writes to Reflections/Monthly/ |
| `/doc` | Process a document — adds metadata and extracts insights, writes to Docs/ |
| `/follow-up-email` | Draft meeting recap email — reads meeting note, outputs draft to chat |
| `/follow-up-meeting` | Draft calendar invite for next meeting — reads meeting note, outputs draft to chat |
| `/review-doc` | Structured feedback on a document — writes to Docs/feedback-[title].md |
| `/coaching-prep` | 1:1 readiness cheat sheet — reads person's hub page and recent meeting notes |
| `/forte` | Performance review generator — reads notes from review period, writes to Docs/ |
| `/annual-review` | Annual review — reads this year's monthly syntheses, writes to Reflections/Annual/ |

## Conventions

- Link person and program names with `[[double brackets]]` in Obsidian
- YAML frontmatter on every note (type, date, tags)
- Status tags: `#status/active` `#status/blocked` `#status/done` `#status/someday`
- Type tags: `#type/meeting` `#type/reflection` `#type/doc` `#type/hub` `#type/handoff`
- Personal content (Meeting Notes, Reflections, My Team, etc.) is gitignored

## Tone and output style

Match the user's writing style as described in `context/mental-model.md`. Default to direct, specific, and concise. Avoid corporate language and vague statements.
