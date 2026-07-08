---
layout: default
title: "Running code"
---

# Running code

GitNomad gives you a **terminal** on your phone that runs commands on your
computer and streams the output back — so you can run a script, your tests, or a
build from anywhere.

## Opening the terminal

On the phone, open a repo and tap the **terminal** button on the file list. You
get a prompt, just like a shell on your computer.

## Running a command

1. Type a command — for example `python main.py`, `npm test`, or `git status`.
2. Send it. It runs **on your computer**, and the output streams in live.
3. A status line shows **running**, **done (exit 0)**, an **exit code**,
   **stopped**, or **error**.

## Tabs

The terminal has **tabs**, like an IDE:

- Tap **+** to open another terminal; tap **✕** on a tab to close it.
- Each tab keeps its own scrollback and its own working directory.
- Tabs are remembered — close the app and reopen it, and they're still there.

## Moving around with `cd`

Each tab has a **working directory**, shown in the prompt. Commands run **there**,
not just at the repo root:

- `cd sub/folder` moves into a subfolder, `cd ..` goes up, and `cd` on its own
  returns to the repo root. The location sticks for the next commands and across
  restarts.
- `clear` wipes the tab's screen.
- You can't leave the repo — the terminal stays inside the folder you shared.

## Answering prompts (interactive input)

If a command pauses to read input — like Python's `input()` — the terminal stays
ready for you. Type your answer and send it; it goes to the running command, and
the command continues. You can send several lines this way.

> Input travels through the sync service, so expect about a second of lag per
> line — great for prompts, not a full interactive REPL.

## Choosing the shell

Commands run in a shell on your computer. Pick which one in the **GitNomad panel**
in VS Code (or the **GitNomad: Choose terminal shell…** command): the OS default,
**PowerShell**, **pwsh**, **cmd**, or **bash** (Git Bash / WSL). The app shows the
active shell as a badge, so you know whether you're typing PowerShell, bash, etc.

## What you need for it to work

Running uses your computer, so on the free plan it must be **on**, with **VS Code
open** and the **GitNomad extension running and linked**. If your computer is
offline, the command stays queued and starts when it reconnects.

> **Cloud run** — running when your PC is **off**, on GitNomad's own machines — is
> a planned Pro feature. Today, running happens on your computer.

## It's your machine

Commands run under your own user account and permissions — the same as typing them
in a terminal on your computer. You're responsible for what you run.

## Tips

- Recall a recent command from the **history chips** above the prompt.
- Keep output reasonable — a mobile screen isn't the place for a 200-line build
  log. Long output is trimmed to keep the phone responsive.
- **Stop** ends a running command and reliably terminates the whole process.

Problems running? → [Troubleshooting → Running code](troubleshooting.md#running-code-doesnt-work).
