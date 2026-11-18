# Claude Starter Kit

**Start using Claude the right way, from zero.** One install gives Claude a set of instructions about you, a simple project system, four commands and a 7-lesson training. After that, every project opens with its own rules, to-do list, memory and history, and Claude keeps them up to date.

No coding. You don't have to read the rest of this repo. It's written for Claude.

## Install (Claude Code)

Open Claude Code and paste this:

```
Set me up with the Claude Starter Kit: https://github.com/999Ineff/claude-starter-kit
Follow its SETUP.md.
```

Claude explains what it will do, asks you 5 quick questions and installs everything. If you already have a `CLAUDE.md`, it backs it up first and keeps it. Then start a new session and type **`/starter-tour`**.

## What you get

**Your commands**

| Type | What happens |
|---|---|
| `/new-project` | Claude asks 6 questions and builds a ready-to-use project folder |
| `/pick-up` | Start of a session: "here's where we stopped and what's next" |
| `/wrap-up` | End of a session: tasks, notes and log updated, handoff written |
| `/starter-tour` | 7 one-minute lessons on working with AI |

**Every project looks like this**

```
AI-Projects/
└── Vendor-Bills/
    ├── CLAUDE.md   ← the rules: what this project is and how to work on it
    ├── TASKS.md    ← to do → in progress → done (done = checked)
    ├── NOTES.md    ← the memory: preferences, quirks, where we stopped
    ├── LOG.md      ← the history: what changed, before → after, approved, checked
    └── files/      ← your documents
```

**How it's laid out.** Your four commands and your global instructions live in `~/.claude/`, so they work in every project. Each project is its own folder. Open one (`cd` into it, or pick it in the app), and Claude reads that project's `CLAUDE.md` plus your global one. Projects never see each other. `AI-Projects` is just a box that holds them; you can choose any folder.

**Your global instructions** (`~/.claude/CLAUDE.md`). Who you are, plus a simple work standard Claude follows everywhere:

> Understand first → give options → check facts at the source → small batches → **done means checked** → report clearly. And never send, pay, delete or post without your "yes".

## The daily rhythm

1. Open your project folder → **`/pick-up`**
2. Work. One task per chat. Claude keeps the task list and log current as it goes.
3. **`/wrap-up`** → new chat next time. Nothing is lost, because the memory lives in the files, not in the chat.

## The 7 lessons (`/starter-tour`)

1. What happens when you hit send (and why long chats get worse)
2. Where Claude's instructions live
3. How to ask: expectations + an example
4. Done means checked
5. Projects and your four commands
6. Teach it once
7. Stay safe

## Using Cowork or the Claude app

Add the kit as a plugin: **Customize → Plugins → Add marketplace → `999Ineff/claude-starter-kit`**, then install **starter-kit**. The commands appear as `/starter-kit:new-project` and so on.

In Cowork, start every session with **`/starter-kit:pick-up`**. It reads the project's files on purpose, so the project's rules and memory load even if the app doesn't read `CLAUDE.md` by itself.

In Claude Code you can also install it as a plugin:

```
/plugin marketplace add 999Ineff/claude-starter-kit
/plugin install starter-kit@ineffable
```

The plugin gives you the commands only. For the global instructions, use the paste-this install above.

## Uninstall

Tell Claude: *"Uninstall the Claude Starter Kit. Follow the Uninstall section of its SETUP.md."* Your projects are never touched.

## FAQ

**Will it overwrite my existing CLAUDE.md?** No. It backs it up, then adds its own clearly marked section at the end.

**Is my data sent anywhere?** No. Everything is plain text files on your computer.

**Can I change the rules?** Yes, and you should. They're plain text. Edit `~/.claude/CLAUDE.md`, or a project's `CLAUDE.md`, or just tell Claude "add that to my preferences".

---

Made by [Luis Aviles · Ineffable Solutions](https://ineffablesolutions.net). This is the beginner version of the system I run every day on 30+ production builds. If it helps you, a ⭐ helps others find it.

MIT License.
