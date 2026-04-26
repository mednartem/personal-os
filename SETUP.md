# Setup Guide

---

## Step 1: Install Obsidian

1. Download from [obsidian.md](https://obsidian.md) — free
2. Install and open it
3. Choose "Open folder as vault" and select this repo folder

---

## Step 2: Install Templater Plugin

1. In Obsidian: Settings (gear icon) → Community Plugins
2. Turn off Safe Mode if prompted
3. Click Browse → search "Templater" → Install → Enable
4. Go to Settings → Templater → set "Template folder location" to `Templates`

That's the only required plugin.

---

## Step 3: Set Up Vault Sync (if using two devices)

See [reference/vault-sync.md](reference/vault-sync.md) for options.

**Quickest path (Mac to Mac):** Move the vault folder into iCloud Drive. It will appear on your second Mac automatically.

---

## Step 4: Run the Setup Interview

This is the most important step. The quality of your context files determines the quality of every AI workflow.

1. Open `setup/interview-prompt.md`
2. Copy everything below the `---` line
3. Paste into a **new** Claude or Gemini conversation
4. Follow the interview — answer honestly and in depth
5. The AI will generate your `context/mental-model.md` and `context/taxonomy.md` at the end
6. Save the output into those files

**Time investment:** 1-2 hours. This is worth it. Shallow input → shallow system.

**Pausing:** If you need to stop, say "let's pause" to the AI. When you return, say "let's continue" — the AI reads the draft files in `setup/` to restore context.

**Examples:** See `examples/` for what filled context files look like for different roles.

---

## Step 5: Populate Goals.md

After the interview, the AI will generate a `Goals.md` for you. Save it to the root of the vault. Review and adjust — this is your source of truth for every reflection and weekly report.

---

## Step 6: Create Your First Notes

Create a hub page for each key person and program the AI identified during the interview:

1. In Obsidian, create a new note in `My Team/` or `Stakeholders/` for each person
2. Use the Hub Person template: click the Templater icon → select "Hub Person"
3. Do the same in `Programs/` for each initiative

You don't need perfect hub pages — stubs are fine. They grow as you use the system.

---

## Step 7: First Week Ritual

**Day 1:**
- Run `/reflect` at the end of the day (use `prompts/reflect.md`)
- Run `/handoff` before stopping

**After every meeting:**
- Take raw notes in a new note using the Meeting template
- Run `/meeting` within 1 hour while context is fresh

**Friday:**
- Run `/weekly-report`

**After 2-3 weeks:**
- Review your `context/mental-model.md` — does it still reflect how you actually work?
- Update it based on what the AI gets wrong or right

---

## Using Workflows

### Copy-paste method (works with Claude or Gemini, any device)

1. Open the relevant file in `prompts/` (e.g., `prompts/reflect.md`)
2. Follow the "What to gather" section — copy the vault files it asks for
3. Paste the prompt + gathered context into a Claude or Gemini chat
4. Save the output to the location at the bottom of the prompt file

### Claude Code / Gemini CLI method

If you use [Claude Code](https://claude.ai/code) or [Gemini CLI](https://github.com/google-gemini/gemini-cli) with this folder open as the workspace, slash commands work directly:

```
/reflect
/meeting
/handoff
/resume
/weekly-report
```

The AI reads your vault files automatically — no copy-paste needed. Commands are in `.claude/commands/` (Claude Code) and `.gemini/commands/` (Gemini CLI). Project context is loaded automatically from `CLAUDE.md` / `GEMINI.md`.

---

## Frequently Asked Questions

**Do I need to use every workflow?**
No. Start with `/reflect`, `/meeting`, and `/handoff`. Add others when you feel the need.

**What if the AI output doesn't match my voice?**
Update the Writing Style section in `context/mental-model.md`. Be more specific about what you want and don't want.

**How often should I update my mental-model.md?**
When something significant changes: new goals, new role, major feedback from a review. At minimum, review it monthly.

**Can I use this with other AI tools?**
Yes. The prompts are plain text — they work with any AI that accepts text input.

**What goes in Tasks.md vs. hub pages vs. meeting notes?**
- `Tasks.md` — your active personal to-do list (short)
- Hub pages — ongoing context for a person or program (accumulated)
- Meeting notes — specific meetings (timestamped, linked from hub pages)
