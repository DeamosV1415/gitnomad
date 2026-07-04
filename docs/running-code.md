---
layout: default
title: "Running code"
---

# Running code

GitNomad can run a command on your computer and stream the output back to your
phone — so you can test a change from anywhere.

## How it works

1. On the phone, open a repo and tap the **Run** button (the ▶ button on the file
   list).
2. Type a command — for example `python main.py`, `npm test`, or `ls -la` — or tap
   one of the preset chips.
3. Tap **Run**. The command executes **on your computer**, inside that repo's
   folder, and its output streams live into the phone's terminal view.
4. Tap **Stop** to end a running command.

## What you need for it to work

Running uses your computer, so on the free plan it must be:

- **on**, with **VS Code open**, and
- the **GitNomad extension running and linked**.

If your computer is offline, the run stays queued and starts when the computer
comes back — or you can stop it.

> **Cloud run** — running when your PC is **off**, on GitNomad's own machines — is
> a planned Pro feature. Today, running happens on your computer.

## Where it runs

Commands run in the **root of the selected repo**, using your computer's shell,
under your own user account and permissions. It's your machine — the same as if
you'd typed the command in a terminal there. You're responsible for what you run.

## Reading the output

- Output appears line by line as it's produced.
- A status badge shows **running**, **exited** (with the exit code), **stopped**, or
  **error**.
- Long output is trimmed to keep the phone responsive; run more specific commands
  if you need to see a particular part.

## Tips

- Keep commands quick and specific — a mobile terminal view isn't the place for a
  200-line build log.
- Use preset chips for the commands you run most.
- If a command seems stuck, check that your computer is still online (the repo's
  status badge should not say **desktop offline**).

Problems running? → [Troubleshooting → Running code](troubleshooting.md#running-code-doesnt-work).
