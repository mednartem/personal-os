---
type: context
updated: YYYY-MM-DD
---

# Taxonomy

> Defines how notes are tagged and linked throughout the vault.
> Consistent tagging makes AI prompts more accurate and Dataview queries possible later.

## Status Tags

| Tag | Meaning |
|---|---|
| `#status/active` | Being worked on now |
| `#status/blocked` | Waiting on something external |
| `#status/done` | Complete |
| `#status/someday` | Parked, not forgotten |

## Type Tags

| Tag | Used on |
|---|---|
| `#type/meeting` | Meeting notes |
| `#type/reflection` | Daily / weekly / monthly reflections |
| `#type/doc` | Documents, proposals, one-pagers |
| `#type/hub` | Hub pages for people and programs |
| `#type/handoff` | Session continuity notes |

## Topic Tags

> Define these during your setup interview based on your actual domains.
> Examples below — replace with yours.

| Tag | Meaning |
|---|---|
| `#topic/roadmap` | Roadmap and planning discussions |
| `#topic/hiring` | Hiring and interviews |
| `#topic/infra` | Infrastructure and platform |
| `#topic/testing` | Test strategy and quality |
| `#topic/design` | System or product design |
| `#topic/incident` | Incidents and post-mortems |

## Linking Rules

- Always link person names to their hub page in `My Team/` or `Stakeholders/`
- Always link program names to their hub page in `Programs/`
- Use `[[double brackets]]` for internal links in Obsidian
- When referencing a decision, link back to the meeting note where it was made
