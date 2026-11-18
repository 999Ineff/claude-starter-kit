---
name: pick-up
description: >-
  Start a work session in a project. Read the project's CLAUDE.md, NOTES.md and TASKS.md, then say what's in progress, what's next and what's blocked. Use when the user types /pick-up or says "pick up where we left off", "where were we", "continue", "what's next", or opens a project folder and starts working.
---

# /pick-up

1. **Find the project.** Look in the current folder for `CLAUDE.md`, `NOTES.md` and `TASKS.md`.
   - If they're missing, ask which project they mean. Projects usually live in the folder named on the `Projects folder:` line of the global CLAUDE.md, or in `~/AI-Projects`. List the folders there that contain a `TASKS.md` and let them pick.
   - If there are no projects at all, offer `/new-project`.
2. **Read, in this order:** `CLAUDE.md` (the rules for this project, so follow them for the whole session), then `NOTES.md` (especially **Last session**), then `TASKS.md`.
3. **Report in 5 lines or fewer:**
   - Project name and what it's for (one line)
   - Where we stopped last time
   - What's in progress
   - The next step you suggest
   - Anything blocked or waiting on someone
4. Ask: "Shall we do the next step, or something else?"

Don't change any files during pick-up. Just read and report.
