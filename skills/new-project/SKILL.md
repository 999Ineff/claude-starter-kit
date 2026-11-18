---
name: new-project
description: >-
  Create a new project folder with CLAUDE.md, TASKS.md, NOTES.md, LOG.md and files/, after a short interview. Use when the user types /new-project or says "start a new project", "make a project for X", "set up a folder for X".
---

# /new-project

You are setting up a new project for someone who may be new to AI. Keep it friendly, short and plain. No jargon.

## Step 1. Where projects live
- Read the user's global CLAUDE.md (`~/.claude/CLAUDE.md`) and look for the line `Projects folder:`. Use that folder.
- If it isn't there, use `~/AI-Projects` (on Windows: `C:\Users\<name>\AI-Projects`). Tell the user that's where it will go.

## Step 2. Interview (one message, all questions, numbered)
If a project name was given (`$ARGUMENTS`), use it and skip question 1.

Ask:
1. What should we call this project? (a short name, e.g. "Vendor bills" or "Website refresh")
2. In one sentence, what is it for?
3. What does "done" look like? (how will you know it worked)
4. Which tools or systems will it touch? (e.g. QuickBooks, Excel, email, Google Drive, none)
5. Anything I should always keep in mind? (rules, deadlines, people, things that went wrong before)
6. What are the first 1–3 things you want to get done?

Tell them "skip" is fine for any question. Wait for the answers.

## Step 3. Build the folder
1. Make a folder name from the project name: letters, numbers and dashes only (e.g. `Vendor-Bills`). If it already exists, ask before using it. Never overwrite existing files.
2. Copy everything from this skill's `template/` folder into the new folder (`CLAUDE.md`, `TASKS.md`, `NOTES.md`, `LOG.md`, `files/README.txt`).
3. Fill in the placeholders in every file:
   - `{{PROJECT_NAME}}`: the name
   - `{{PURPOSE}}`, `{{DONE_LOOKS_LIKE}}`, `{{SYSTEMS}}`, `{{ALWAYS_KNOW}}`: their answers (write "(not set yet)" if they skipped)
   - `{{OWNER}}`: the user's name from the global CLAUDE.md, or ask
   - `{{CREATED}}`: today's date, YYYY-MM-DD
   - `{{FIRST_TASKS}}`: one `- [ ] task` line per first task (or `- [ ] (add your first task)`)
4. Check your work: open each file and confirm that no `{{` placeholders are left. Fix any you find.

## Step 4. Hand it over
Tell them, in plain words:
- Where the folder is (full path).
- What's inside, one line per file (use the table in the project's CLAUDE.md).
- **How to open it next time:**
  - Claude Code in a terminal: `cd` into the folder, then run `claude`.
  - Claude desktop app: choose that folder as the working folder.
- The daily rhythm: start with `/pick-up`, finish with `/wrap-up`. (If the commands were installed as a plugin, they're named `/starter-kit:pick-up` and `/starter-kit:wrap-up`. Use whichever form this session shows.)
- That from now on, in that folder, you'll read the notes and tasks first, keep the task list and log updated, and suggest `/wrap-up` at the end.

Then ask: "Want to start on the first task now?" If the session is already in a different folder, say they'll get the best results by opening the new folder, so its CLAUDE.md loads.
