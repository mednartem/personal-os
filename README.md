# Personal OS

A personal operating system built on Obsidian for knowledge workers — developers, QA engineers, managers, ICs, PMs. Helps you align daily work with long-term goals, surface patterns over time, and build institutional memory.

Works with **Claude and Gemini**. No special tools required beyond Obsidian.

---

## What This Is

Not a productivity hack. Not a note-taking template. A system that creates a feedback loop between your daily actions and your long-term goals.

- **Monitor time allocation** — are you working on what matters, or getting pulled into fires?
- **Develop personally** — surface your blind spots regularly, not just at review time
- **Elevate meeting quality** — skip the catch-up phase, go straight to substance
- **See patterns across time** — daily → weekly → monthly synthesis reveals what's invisible day-to-day
- **Build institutional memory** — decisions, context, coaching history — retrievable when you need it

---

## Prerequisites

- [Obsidian](https://obsidian.md) (free)
- Obsidian community plugin: **Templater**
- Claude or Gemini (any tier works)

---

## Quickstart

1. Clone or download this repo
2. Open the folder as a vault in Obsidian (File → Open Folder as Vault)
3. Install the Templater plugin (Settings → Community Plugins → Browse → search "Templater")
4. Configure Templater to use the `Templates/` folder (Settings → Templater → Template folder location)
5. Open `setup/interview-prompt.md`, paste into Claude or Gemini, follow the interview
6. After the interview, save the generated files: `context/mental-model.md`, `context/taxonomy.md`, `Goals.md`, and any hub pages to `My Team/`, `Stakeholders/`, `Programs/`
7. Run `/reflect` at the end of your first day

Full setup guide: [SETUP.md](SETUP.md)

---

## Vault Structure

```
├── context/               # What tells the AI about you
│   ├── mental-model.md    # Your goals, principles, writing style, org context
│   └── taxonomy.md        # Tag and linking conventions
├── prompts/               # Copy-paste prompts for Claude or Gemini
├── .claude/commands/      # Claude Code slash commands
├── .gemini/commands/      # Gemini CLI slash commands
├── setup/                 # One-time onboarding
│   └── interview-prompt.md
├── Templates/             # Obsidian note templates
├── examples/              # Filled examples by role (developer / manager / ic-qa)
├── reference/             # Reference documentation
├── Meeting Notes/         # Processed meeting notes
├── Reflections/           # Daily, weekly, monthly, annual
├── Docs/                  # Processed documents, feedback, performance reviews
├── My Team/               # Hub pages for direct reports
├── Stakeholders/          # Hub pages for partners and stakeholders
├── Programs/              # Hub pages for initiatives
├── Handoffs/              # Session continuity notes
├── Goals.md
└── Tasks.md
```

---

## Workflows

| Prompt | Purpose | Frequency |
|---|---|---|
| `/reflect` | Daily strategic reflection — align priorities to goals | Daily |
| `/meeting` | Process raw meeting notes into structured format | After every meeting |
| `/handoff` | Capture session state before stopping work | Daily |
| `/resume` | Pick up where you left off | Start of session |
| `/weekly-report` | Weekly synthesis and progress check | Friday |
| `/monthly-synthesis` | Monthly pattern analysis | End of month |
| `/doc` | Standardize document metadata and extract insights | As needed |
| `/follow-up-email` | Draft meeting recap email | After meetings |
| `/follow-up-meeting` | Draft calendar invite for next steps | After meetings |
| `/review-doc` | Structured feedback on a document | As needed |
| `/coaching-prep` | 1:1 readiness cheat sheet | Before 1:1s |
| `/forte` | Performance review generator | Review season |
| `/annual-review` | Annual review and next-year planning | End of year |

Each workflow has a prompt file in `prompts/` (paste into Claude or Gemini) and a Claude Code command in `.claude/commands/` (run directly if using Claude Code).

Full reference: [reference/workflow-reference.md](reference/workflow-reference.md)

---

## How to Use a Workflow

### With Claude or Gemini (any device)

1. Open the relevant file in `prompts/` (e.g., `prompts/reflect.md`)
2. Follow the "What to gather" instructions — copy the relevant vault files
3. Paste the prompt + your context into Claude or Gemini
4. Save the output to the location specified at the bottom of the prompt file

### With Claude Code or Gemini CLI

If you have [Claude Code](https://claude.ai/code) or [Gemini CLI](https://github.com/google-gemini/gemini-cli) installed with this folder open as the workspace, slash commands work directly — no copy-paste needed:

```
/reflect
/meeting
/handoff
/resume
/weekly-report
```

Commands for both tools live in `.claude/commands/` and `.gemini/commands/`. Project context is automatically loaded from `CLAUDE.md` / `GEMINI.md`.

---

## Examples

See `examples/` for filled mental-model.md and goals.md for three role archetypes:

- `examples/developer/` — Senior SWE focused on shipping a major service migration
- `examples/manager/` — Engineering manager growing a team and delivering a roadmap
- `examples/ic-qa/` — Quality engineer building automation culture

---

## Who This Is For

Works best for anyone whose success depends on strategic alignment, not just task completion:

- Senior ICs with complex stakeholder landscapes and long-term initiatives
- Managers with direct reports to develop and programs to oversee
- Anyone who wants to be deliberate about where their time goes

Requires: willingness to reflect honestly, 10-15 minutes daily, patience (value compounds over weeks).

---

## Sync Between Devices

Put your vault in iCloud Drive (Mac) or use Obsidian Sync. Details: [reference/vault-sync.md](reference/vault-sync.md)

---

## Privacy

This vault will contain personal reflections, performance notes, and candid assessments. Keep it in a personal, secure location. Personal content (Meeting Notes, Reflections, etc.) is gitignored — it won't be committed if you fork this repo.
