. # Setup Guide

---

## Overview

Two things need to happen before the system is useful:

1. **Install the tools** — Obsidian + Templater plugin (15 minutes)
2. **Run the setup interview** — fills in your personal context files (1-2 hours)

After that, the system runs itself through daily habits.

---

## Part 1 — Install the Tools

### Step 1: Install Obsidian

Download from [obsidian.md](https://obsidian.md) — free.

Open Obsidian → choose **Open folder as vault** → select this repo folder.

### Step 2: Install the Templater Plugin

Templater lets you create notes from templates with auto-filled dates.

1. In Obsidian: **Settings → Community Plugins**
2. Disable Safe Mode if prompted
3. Click **Browse** → search "Templater" → Install → Enable
4. Go to **Settings → Templater** → set "Template folder location" to `Templates`

That is the only required plugin. Everything else is optional.

---

## Part 2 — Run the Setup Interview

This is the most important step. The interview generates your personal context files — without them, every AI workflow produces generic output.

### How to run it

1. Open `setup/interview-prompt.md` in Obsidian or any text editor
2. Copy everything below the `---` line
3. Paste into a **new** Claude or Gemini conversation
4. Follow the interview — answer honestly and in depth

**Time:** 1-2 hours. This investment pays back in every workflow you run after.

**Pausing:** If you need to stop, say "let's pause" — the AI saves draft files. When you return, say "let's continue" and it will pick up from where you left off.

### What the interview generates

At the end, the AI will produce:

| File | Where to save it |
|---|---|
| `mental-model.md` | `context/mental-model.md` |
| `taxonomy.md` | `context/taxonomy.md` |
| `Goals.md` | `Goals.md` (root) |
| Hub pages for your team | `My Team/[Name].md` |
| Hub pages for stakeholders | `Stakeholders/[Name].md` |
| Hub pages for programs | `Programs/[Name].md` |

Copy each generated file and paste it into the corresponding location in your vault.

**Examples:** See `examples/` for what filled context files look like for three roles — developer, manager, and QA engineer.

---

## Part 3 — First Week

### Day 1

- Run `/reflect` at the end of the day (or use `prompts/reflect.md`)
- Run `/handoff` before you stop working

### After every meeting

- Take rough notes in a new note using the Meeting template (Templater icon → Meeting)
- Run `/meeting` within 1 hour while the context is still fresh

### Friday

- Run `/weekly-report`

### After 2-3 weeks

Review `context/mental-model.md`. Update anything the AI has been getting wrong. The system improves as the context improves.

---

## Part 4 — Two-Laptop Setup

The vault has two separate layers that sync differently:

| Layer | What it contains | How it syncs |
|---|---|---|
| **Scaffold** | Commands, templates, prompts, examples | Git (`git pull`) |
| **Personal content** | Reflections, Meeting Notes, Goals, Docs, etc. | iCloud or Obsidian Sync |

### Setting up the second laptop

1. Clone the repo:
   ```
   git clone git@github.com:mednartem/personal-os.git
   ```
2. Open the folder as a vault in Obsidian
3. Install Templater (same as Step 2 above)
4. Set up iCloud or Obsidian Sync to bring over your personal content (see below)

You do **not** need to run the setup interview again — your context files sync from the first laptop.

### Syncing personal content between laptops

**Option 1: iCloud Drive (recommended for Mac-to-Mac)**

Move your vault folder into iCloud Drive. It appears on your second Mac automatically. Free, no extra software.

Caveat: sync is not instant — allow 30-60 seconds. If you edit on both machines simultaneously, iCloud may create conflict copies — resolve manually.

**Option 2: Obsidian Sync**

$8/month. Works cross-platform, end-to-end encrypted, handles conflicts better than iCloud. Worth it if you use Windows, iOS, or need version history.

**Option 3: Git (private repo)**

Fork this repo to a private GitHub repository. Track your personal content by removing the gitignore entries for the files you want to version. Use the Obsidian Git plugin to auto-commit and push.

Full comparison: [reference/vault-sync.md](reference/vault-sync.md)

---

## Part 5 — Using Workflows

Every workflow is available two ways:

### With Claude Code or Gemini CLI (recommended)

If you have [Claude Code](https://claude.ai/code) or [Gemini CLI](https://github.com/google-gemini/gemini-cli) installed and this folder open as your workspace, slash commands work directly — no copy-paste:

```
/reflect
/meeting
/weekly-report
```

The AI reads your vault files automatically. Commands are in `.claude/commands/` and `.gemini/commands/`.

### With Claude or Gemini (copy-paste, works anywhere)

1. Open the relevant file in `prompts/` (e.g., `prompts/reflect.md`)
2. Follow the "What to gather" section — copy the vault files it asks for
3. Paste the prompt + your context into a new Claude or Gemini chat
4. Save the output to the location shown at the bottom of the prompt file

---

## Workflow Quick Reference

| Command | When to use | Output |
|---|---|---|
| `/reflect` | End of every workday | `Reflections/Daily/` |
| `/meeting` | Within 1 hour of a meeting | `Meeting Notes/` |
| `/handoff` | Before stopping work | `Handoffs/` |
| `/resume` | Start of a work session | Chat |
| `/weekly-report` | Friday | `Reflections/Weekly/` |
| `/monthly-synthesis` | Last day of the month | `Reflections/Monthly/` |
| `/annual-review` | End of year | `Reflections/Annual/` |
| `/doc` | When you receive a proposal or design doc | `Docs/` |
| `/follow-up-email` | Within 2 hours of a meeting | Chat (copy to email) |
| `/follow-up-meeting` | After a meeting that needs a follow-up | Chat (copy to calendar) |
| `/review-doc` | When asked to review someone's document | `Docs/` |
| `/coaching-prep` | 10-15 min before a 1:1 | Chat |
| `/forte` | Before performance review season | `Docs/` |

---

## FAQ

**Do I need to use every workflow?**
No. Start with `/reflect`, `/meeting`, and `/handoff`. Add others when you feel the need.

**What if the AI output doesn't match my voice?**
Update the Writing Style section in `context/mental-model.md`. Be specific about what you want and don't want.

**How often should I update my mental-model.md?**
When something significant changes: new role, new goals, major feedback from a review. At minimum, review it monthly.

**What goes in Tasks.md vs. hub pages vs. meeting notes?**
- `Tasks.md` — your short active to-do list (keep it under one screen)
- Hub pages — ongoing context for a person or program (grows over time)
- Meeting notes — specific meetings, timestamped, linked from hub pages

**Can I use this with ChatGPT or other AI tools?**
Yes. The prompts in `prompts/` are plain text and work with any AI that accepts text input. The slash commands (`.claude/commands/`, `.gemini/commands/`) are specific to Claude Code and Gemini CLI.

**The AI keeps getting something wrong about me.**
That means `context/mental-model.md` needs updating. The AI only knows what's in that file — it has no memory between sessions.
