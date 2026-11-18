# SETUP: instructions for Claude

> **This file is written for Claude, not for people.** A person installs the kit by telling Claude:
> *"Set me up with the Claude Starter Kit: https://github.com/999Ineff/claude-starter-kit. Follow its SETUP.md."*
>
> **Claude:** follow these steps in order. Talk to the user in plain, friendly language. They may be brand new to AI. Never skip the backup step, and never overwrite anything without saying so first.

## What gets installed

| What | Where | Why |
|---|---|---|
| A global instructions block | `~/.claude/CLAUDE.md` (added between `claude-starter-kit:start` / `end` markers) | So Claude knows who they are and how to work, in every chat |
| 4 skills: `new-project`, `pick-up`, `wrap-up`, `starter-tour` | `~/.claude/skills/<name>/` | Their commands |
| A projects folder | `~/AI-Projects` (or the folder they choose) | Where their projects live |

`~` is the user's home folder (`C:\Users\<name>` on Windows, `/Users/<name>` on Mac).

## Step 0. Check where you're running
- If you are **Claude Code** (you can run shell commands and read and write files in the home folder), continue.
- If you are **Cowork or the Claude app**, stop here. Tell the user to install the kit as a plugin instead: **Customize → Plugins → Add marketplace → `999Ineff/claude-starter-kit`**, then install **starter-kit**. Point them to the "Using Cowork or the Claude app" section of the README.

## Step 1. Explain and get a yes
Tell the user, in 4–5 lines, what will be installed (the table above), and that any existing `~/.claude/CLAUDE.md` gets **backed up first and kept**: the kit adds a section, it doesn't replace theirs. Ask: "OK to go ahead?" Wait for a yes.

## Step 2. Get the files
- If this repo is already on disk (you were pointed at a local folder), use that.
- Otherwise clone it into a temporary folder: `git clone --depth 1 https://github.com/999Ineff/claude-starter-kit <temp>/claude-starter-kit`.
- If `git` isn't installed, download `https://github.com/999Ineff/claude-starter-kit/archive/refs/heads/main.zip` and unzip it.

## Step 3. Five quick questions (one message, numbered)
1. What's your name?
2. What's your role? (e.g. "AP supervisor", "office manager", "owner")
3. Company or team? (optional)
4. What do you mostly want to use AI for? (a few words)
5. Where should your projects live? Suggest `~/AI-Projects` (one folder that just holds your projects) with the real full path, and say "just say OK to use this". Your home folder itself is fine too. Each project is its own folder either way.

## Step 4. Install the global instructions
1. Make sure `~/.claude/` exists.
2. If `~/.claude/CLAUDE.md` exists, **copy it first** to `~/.claude/CLAUDE.md.backup-YYYY-MM-DD` and tell the user the backup path.
3. Take `global/CLAUDE.md` from the kit and fill in: `{{NAME}}`, `{{ROLE}}`, `{{COMPANY}}`, `{{USES}}`, `{{PROJECTS_FOLDER}}` (the full path), and set `{{TOUR_DONE}}` to `not yet`.
4. Then:
   - **No existing file:** write the filled block as `~/.claude/CLAUDE.md`.
   - **The existing file already has the `claude-starter-kit:start` … `end` markers** (an earlier install): replace only what's between the markers. Keep the user's "About me" and "My preferences" lines from the old block.
   - **The existing file has other content:** add the block at the end, after one blank line. Don't change anything above it. If their existing instructions clearly contradict the kit's (for example, a different projects folder), point it out and ask which one wins.

## Step 5. Install the skills
For each folder in the kit's `skills/` (`new-project`, `pick-up`, `wrap-up`, `starter-tour`): copy it, with everything inside it, to `~/.claude/skills/<same name>/`. If a folder with that name already exists and wasn't installed by this kit, ask before replacing it.

## Step 6. Make the projects folder
Create the projects folder from Step 3 if it doesn't exist.

## Step 7. Check your work
- Read `~/.claude/CLAUDE.md` back. Confirm the block is there once, and that no `{{` placeholders are left.
- Confirm each of the 4 skills has a `SKILL.md`, and that `new-project/template/` holds `CLAUDE.md`, `TASKS.md`, `NOTES.md`, `LOG.md` and `files/README.txt`.
- Confirm the projects folder exists.
- If anything failed, say exactly what and fix it. Don't report success you didn't check.

## Step 8. Finish
Tell the user:
- What was installed and where (3–4 lines, with the backup path if one was made).
- **"Close this session and start a new one** (type `exit`, then `claude` again) so the new instructions and commands load."
- Then, in the new session: **`/starter-tour`** for the 7 short lessons, or **`/new-project`** to make a first project.
- Ask: "Want to take the quick tour when you're back?"

You can delete the temporary clone if you made one.

---

## Uninstall (when the user asks)
1. Remove everything between the `claude-starter-kit:start` and `end` markers (including the markers) from `~/.claude/CLAUDE.md`. Or restore the `CLAUDE.md.backup-…` file if they prefer.
2. Delete `~/.claude/skills/new-project`, `pick-up`, `wrap-up` and `starter-tour`.
3. **Never delete their projects folder or projects.** Those are their work.

## Update (when the user asks)
Repeat Steps 2, 4 (the "already has markers" path) and 5. Keep their answers and preferences.
