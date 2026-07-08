---
layout: default
title: "Troubleshooting"
---

# Troubleshooting

Most GitNomad problems come down to one of three things:

1. Your **computer is offline** (or VS Code / the extension isn't running).
2. Your **sign-in** or **link** needs refreshing.
3. A **network** hiccup between your phone and the sync service.

This page walks through the common symptoms and their fixes, from most to least
common. If nothing here helps,
[open an issue](https://github.com/DeamosV1415/gitnomad/issues/new/choose) with the
details listed at the [bottom of this page](#still-stuck-how-to-report-it).

> **The one check that fixes most issues:** make sure your computer is **on**, VS
> Code is **open**, and the **GitNomad panel shows a linked/connected state**. On
> the free plan your computer does the real work — if it's asleep or the extension
> isn't running, sync and run won't happen.

---

## Sign-in

### I can't sign in / the browser closes and nothing happens

- Make sure you finished the sign-in in the browser sheet (approve the GitHub or
  Google prompt). Closing it early cancels sign-in.
- Check your internet connection and try again.
- If you were signed in before and it suddenly fails, your session may have
  expired — sign in again.
- Corporate or school networks sometimes block sign-in pop-ups. Try mobile data
  or a different network.

### It signed me in but my repos are empty

That's expected until you connect a computer. Repos come from your **desktop**, so
you need to [install and link the VS Code extension](linking-desktop.md). If
you've already linked, see [My repos aren't showing up](#my-repos-arent-showing-up).

---

## Linking and connection

### The link code doesn't work

- Codes are **single-use** and expire after a few minutes. Tap **New code** on the
  phone (**Profile → Link desktop**) and enter the fresh one.
- Make sure you're typing it into the **GitNomad extension** in VS Code, not
  somewhere else.
- Double-check the digits — it's a 6-digit code.

### The extension says "Cannot connect"

- Confirm your computer is **online**.
- Make sure you actually **linked** the extension (Profile → Link desktop → enter
  code in the extension). An unlinked extension can't sync.
- Click **Re-link** in the GitNomad panel and enter a new code from the phone.
- Restart syncing: use **Stop syncing** then start again, or reload the VS Code
  window.

### I linked, but the phone shows "desktop offline"

- Your computer hasn't checked in recently. Make sure VS Code is open and the
  GitNomad panel is running (not stopped).
- If your computer went to sleep, wake it — sync resumes automatically.
- Reload the VS Code window to restart the extension.

---

## Syncing

### My repos aren't showing up

1. In VS Code, open the folder you want to share — it must be a **git repository**
   (it has a `.git` folder / VS Code shows source control for it).
2. In the GitNomad panel, use **Add a repo** and select that folder, or make sure
   it's listed.
3. Confirm the extension is **linked** and the computer is **online**.
4. On the phone, pull down on the **Repos** list to refresh.

### My phone edit didn't reach my computer

- Check the repo's status badge. **N pending** means the edit is queued because
  your computer is offline or paused — bring the computer online and it will
  deliver.
- Make sure you **saved** (and pushed if prompted) on the phone.
- Give it a few seconds — sync polls every few seconds, it isn't instant.
- If it stays pending with the computer clearly online, reload the VS Code window
  to restart the extension.

### It's stuck on "N pending" and says "action on desktop"

This happens when **both** sides changed the **same file** and your computer has
**unsaved-to-git (uncommitted) changes** to it. Git won't let your phone's version
overwrite work you haven't committed, so your phone's edits wait — and the repo
shows an **"action on desktop"** badge. On the phone's file list you'll see a
banner naming the file(s), like:

> *Your desktop has uncommitted changes to `index.html`. Commit or discard them on
> your desktop to finish syncing.*

**On your computer**, do one of these for the named file(s):

- **Keep both sides (recommended):** commit your computer's change, then let sync
  continue — you'll get a **"Changes to review"** card on the phone to merge the two
  versions.
  ```sh
  git add -A
  git commit -m "my desktop edits"
  ```
- **Keep the phone's version:** discard your computer's uncommitted change so the
  phone's edit applies cleanly.
  ```sh
  git checkout -- index.html      # or: git restore index.html
  ```

Within a few seconds the badge clears and your phone's changes land. (You can do
this from the VS Code Source Control panel too — commit or discard the file.)

### My computer's changes aren't on the phone

- Save the file in VS Code — unsaved-but-saved-to-disk changes appear as
  [live drafts](syncing.md#live-drafts) within a few seconds.
- Pull down to refresh the file list or reopen the file.
- Confirm the repo isn't showing **desktop offline**.

### A file shows old content / seems frozen

- Pull down to refresh, or close and reopen the file.
- If a big sync (like a divergence resolution) just happened, wait a few seconds
  and refresh — the phone re-reads once the computer settles.

---

## A review won't go away

If a **"Changes to review"** card keeps appearing:

- Open it and complete the review — pick a side for **every** conflicting chunk,
  then tap **Apply**. A review only clears once it's applied.
- Make sure your computer is **online** so it can fast-forward to the merged
  result after you apply.
- If it reappears immediately after applying, your computer may have committed
  again on the same lines — resolve once more; it will settle.

See [Reviewing merges](merge-review.md) for how the review works.

---

## Running code doesn't work

### Nothing happens when I run a command

- Running uses your computer — it must be **on**, with VS Code open and the
  extension **linked and running**. Check the repo isn't **desktop offline**.
- Make sure you typed a command and sent it.

### The command runs but errors

- The error is from **your command on your machine**, exactly as if you'd typed it
  in a terminal there. Check the command, the terminal's **working directory**
  (shown in the prompt — use `cd` to change it), and that any tools it needs are
  installed on your computer.

### A command in a subfolder hangs, or Stop won't end it

- Update the **desktop extension to 0.1.2 or newer**. Older versions had a bug
  where a command run in a subfolder (after `cd`) never started and couldn't be
  stopped. Check the version on the extension's Marketplace / Open VSX page, or
  reinstall the latest.

### My program is waiting for input

- Some commands pause to read input (like Python's `input()`). The terminal stays
  ready — type your answer and send it, and the command continues. You can send
  more than one line.

### A command seems stuck

- If it's waiting for input, see above. Otherwise tap **Stop** to end it. If your
  computer went offline mid-run, the run pauses until it's back; stop it and try
  again once you're connected.

---

## Account and data

### How do I delete my account?

**Profile → Delete account.** This permanently removes your synced repos and
unlinks your desktops. Your local code on your own computer is **not** affected.
See [Account & your data](account-and-data.md).

### I removed a repo but it came back

Removing a repo from the phone deletes the **cloud copy**. If your computer's
extension is still exposing that folder, it can reappear on the next sync. To make
removal permanent, **remove it in the extension** too.

---

## General

### Is it slow / not instant?

Sync is designed to be safe and durable, not real-time. Expect a few seconds for
changes to appear. Pull to refresh to check immediately.

### Things are behaving strangely after an update

- Force-close and reopen the app.
- Reload the VS Code window to restart the extension.
- As a last resort, sign out and back in on the phone (your repos are safe on your
  computer).

---

## Still stuck? How to report it

[Open an issue](https://github.com/DeamosV1415/gitnomad/issues/new/choose) and
include:

- **What you did** and **what you expected** vs **what happened**.
- Your **phone model** and **Android version**.
- Your **computer's OS** and **VS Code version**.
- Whether the repo showed **synced / pending / desktop offline** at the time.
- Any error message text (a screenshot helps).

The more detail you give, the faster it gets fixed. Thanks for helping make
GitNomad better!
