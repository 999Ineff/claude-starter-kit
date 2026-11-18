---
name: wrap-up
description: >-
  End a work session cleanly. Update TASKS.md, NOTES.md and LOG.md in the current project and write a short handoff so the next chat can pick up where this one stopped. Use when the user types /wrap-up or says "wrap up", "let's stop here", "save where we are", "I'll continue tomorrow", or when the chat has become long.
---

# /wrap-up

1. **Find the project.** Look for `CLAUDE.md` and `TASKS.md` in the current folder. If they aren't there, say this folder isn't a project yet and offer `/new-project`. Stop.
2. **Tasks.** Update `TASKS.md`:
   - Finished AND checked → **Done**, with the date and how it was checked.
   - Started but not finished → stays in **In progress**, with one line about where it stopped.
   - New things that came up → **To do**.
3. **Log.** Make sure every change made in this session has a row in `LOG.md`, with "Checked" filled in. If something was changed but never checked, mark it `NOT CHECKED`. Don't hide it.
4. **Notes.** Add any new preference, quirk or mistake-not-to-repeat to `NOTES.md` (one short line each). Then replace the **Last session** section with 3–5 lines:
   - Date
   - What we did
   - Where we stopped
   - The very next step
   - Anything waiting on someone
5. **Report** to the user in 5 lines or fewer: what you updated, the next step, and:
   "Next time, start a new chat in this folder and say **'pick up where we left off'**."

Don't change `CLAUDE.md` during a wrap-up. If you think it should change, suggest the exact line and let the user decide.
