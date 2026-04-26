Read context/mental-model.md from this vault.

Ask me to paste the raw meeting notes I want to process.

After I paste them, process the notes into a structured meeting note and write it to Meeting Notes/[date] [title].md in this format:

```markdown
---
type: meeting
date: [extract from notes]
participants: [list names]
program: [which program this relates to]
tags: [#type/meeting]
---

# Meeting: [descriptive title]

## Summary
[2-3 sentences: what was this meeting about and why it mattered]

## Key Decisions
[bullet list with owners]

## Action Items
- [ ] [Owner] — [action] — [due date if mentioned]

## Context / Backstory
[what someone needs to understand why this meeting happened]

## Open Questions
[unresolved items needing follow-up]
```

Rules:
- Extract implicit decisions and action items, not just explicit ones
- Attribute action items to specific owners — flag "(owner TBD)" if unclear
- Use [[double brackets]] for program and person names
- Flag missing info with [MISSING: ...]
