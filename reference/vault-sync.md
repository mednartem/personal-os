# Vault Sync Between Devices

Your vault is just a folder of markdown files. Sync it however you sync files.

---

## Option 1: iCloud Drive (Recommended for Mac users)

**Cost:** Free  
**Setup time:** 5 minutes  
**Best for:** Two Mac laptops, both signed into the same Apple ID

### Setup

1. Move your vault folder into iCloud Drive:
   - Open Finder → iCloud Drive
   - Create a folder called `Personal OS` (or whatever you named your vault)
   - Move all vault files there

2. On your second Mac:
   - Open Finder → iCloud Drive
   - The `Personal OS` folder will appear automatically after syncing
   - Open Obsidian → Open folder as vault → select the iCloud folder

3. iCloud syncs automatically in the background.

### Caveats

- Sync is not instant — allow 30-60 seconds between devices
- If you edit on both devices simultaneously, iCloud may create conflict copies (filenames with "(conflict)") — resolve manually
- iCloud must be enabled and have enough storage on both machines

---

## Option 2: Obsidian Sync

**Cost:** $8/month  
**Setup time:** 10 minutes  
**Best for:** Cross-platform (Mac + Windows + iOS), or if you want end-to-end encryption

### Setup

1. Subscribe at obsidian.md
2. In Obsidian: Settings → Sync → Enable
3. Create a remote vault and connect both devices to it
4. Sync is automatic and encrypted

### Advantages over iCloud

- Works on any OS (not just Mac)
- End-to-end encrypted
- Built-in version history (30 days)
- Handles conflicts more gracefully

---

## Option 3: Git (Private Repository)

**Cost:** Free (GitHub private repo)  
**Setup time:** 30 minutes  
**Best for:** Technical users who want full version history and don't mind manual sync

### Setup

1. Create a private repo on GitHub
2. Clone into your vault folder
3. Install the **Obsidian Git** plugin (community plugins)
4. Configure auto-commit and auto-push intervals (e.g., every 10 minutes)

### Caveats

- Not seamless — requires commits and pushes
- Conflicts in markdown files are manageable but annoying
- `.gitignore` in this repo already excludes personal content — adjust if needed

---

## Which should I use?

| Situation | Recommendation |
|---|---|
| Both laptops are Mac | iCloud Drive |
| Mac + Windows, or want encryption | Obsidian Sync |
| Want version history, comfortable with git | Git |
| Both laptops are work-managed (iCloud disabled) | Obsidian Sync or Git |
