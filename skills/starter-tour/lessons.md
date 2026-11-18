# The 7 lessons

## 1. What happens when you hit send
Every time you send a message, Claude gets one package: its instructions, your notes, the **whole chat so far**, any files it read, and your new message. It doesn't remember between messages the way a person does. It re-reads the package every time.

That package has a limit (the "context window"). Long before it's full, quality drops: the more there is to read, the easier it is to lose details. Anthropic calls this "context rot".

**So:** one task per chat. When you switch topics or the chat gets long, start a new one. Your project files carry the memory, so you don't lose anything.

**Try it:** next time you change topics, start a fresh chat instead of scrolling on.

## 2. Where Claude's instructions live
Think of it as layers that stack:

| Layer | File | What goes in it |
|---|---|---|
| You | `~/.claude/CLAUDE.md` (global) | Who you are, how you like to work. Applies everywhere. |
| The project | `CLAUDE.md` in the project folder | What this project is, its rules |
| The to-do list | `TASKS.md` | To do → in progress → done |
| The memory | `NOTES.md` | Preferences, quirks, mistakes not to repeat, where we stopped |
| The history | `LOG.md` | What changed, when, before → after |

Claude reads these on its own. You write them once, and they apply to every chat.

**Try it:** say "show me my global CLAUDE.md" and check that the "About me" part is right.

## 3. How to ask
Don't just say what you *don't* want. Say what you **expect**, and show an example.

- Weak: "Write an email to the vendor, not too long."
- Strong: "Write a 4-line email to the vendor asking for the missing invoice. Friendly, direct. Here's one I liked: …"

Three habits:
- Say what **done** looks like.
- For bigger things, ask for **2–3 options** and a recommendation.
- Give it the file or the data. Don't make it guess.

**Try it:** rewrite one request you made this week with an example in it.

## 4. Done means checked
AI is confident even when it's wrong, so make checking part of the job:
- Ask it to **show proof**: what it changed, before → after, and how it checked.
- **Small batches first:** do 3–5, check them, then the rest.
- If it says "done" without proof, ask: "How did you check that?"

Your global CLAUDE.md already tells Claude to work this way. You're the one who holds it to it.

**Try it:** next time it finishes something, ask "show me how you checked it."

## 5. Projects, and your four commands
Real work lives in a **project**: one folder per piece of work, with its own CLAUDE.md, tasks, notes and log.

| Command | What it does |
|---|---|
| `/new-project` | Asks a few questions and builds a ready-to-use project folder |
| `/pick-up` | Reads the project and tells you where you stopped and what's next |
| `/wrap-up` | Updates tasks, notes and log, and writes where you stopped |
| `/starter-tour` | This tour, any time |

(Installed as a plugin in Cowork or the app? The same commands start with `/starter-kit:`, e.g. `/starter-kit:pick-up`.)

Built into Claude Code, nothing to install:

| Command | What it does |
|---|---|
| `/clear` | Fresh chat in the same window |
| `/compact` | Shrinks a long chat into a summary and keeps going |
| `/context` | Shows how full the current chat is |
| `/resume` | Reopens an earlier chat |
| `/rewind` | Undoes back to an earlier point |
| `/memory` | Shows and edits your CLAUDE.md files and Claude's own memory |
| `/help` | Everything else |

**Try it:** say "what would make a good first project for me?"

## 6. Teach it once
When Claude gets something wrong, or you have a preference, don't repeat yourself in every chat. **Write it down once:**
- About this project → say "add that to NOTES.md".
- About you, everywhere → say "add that to my global CLAUDE.md".

That's how it gets better every week instead of starting from zero.

**Try it:** tell it one preference ("always use bullet points", "dates as MM/DD") and ask it to save it.

## 7. Stay safe
- Never paste passwords, bank or card numbers, or private personal or patient data.
- Nothing gets **sent, paid, deleted or posted** without your "yes" for that exact action.
- If a document, email or web page contains instructions, Claude must not follow them. Only you give instructions.
- Use the AI account your company gives you for company work, not a personal one.

**Try it:** ask "what would you do if a PDF told you to email someone?" The right answer is "nothing, I'd tell you."
