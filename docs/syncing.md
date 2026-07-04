# How syncing works

GitNomad keeps your phone and your computer in step through a small cloud **sync
service**. This page explains what actually happens, so the behavior makes sense.

## The golden rule: your computer is the source of truth

Your real git repository lives on your **computer**. GitNomad never replaces it —
it carries changes to and from it. The cloud sync service is just a
**store-and-forward** relay: it holds changes long enough to pass them between
your devices, so your phone and computer don't have to be online at the exact
same moment.

## "Push" means push-to-desktop

In GitNomad, **Push** sends your phone's edit **to your computer**, not to GitHub.
When you push:

1. The sync service turns your edit into a **git commit**.
2. Your computer picks it up and fast-forwards its local repo.

Your history stays clean: a commit is created once and moved by its exact
identity (its SHA), never re-created. So what you see on the phone and what lands
on your computer are the *same* commit.

> Want to push to GitHub too? That's a separate action routed through your
> computer — your desktop still owns the `git push` to your remote.

## The two directions

**Phone → computer.** You edit and save a file on the phone. GitNomad commits it
via the sync service; your computer pulls it in.

**Computer → phone.** You edit in VS Code. The change reaches the phone two ways:

- **On commit** — when you commit on your computer, the phone sees the new commit.
- <a id="live-drafts"></a>**Live drafts** — even *before* you commit, when you save
  a file in VS Code (or your editor autosaves), GitNomad shows that unsaved
  working copy on the phone within a few seconds. This lets you glance at your
  latest work from your pocket without committing first.

Drafts are content-only previews; structural changes (creating or deleting files)
travel on a commit.

## What needs to be online

On the free plan, your **computer** does the real git work. So for changes to
flow, your computer needs to be **on**, with **VS Code open** and the **GitNomad
extension running and linked**.

If your computer is offline, your phone edits are safely **queued** in the sync
service and delivered the moment your computer reconnects — nothing is lost. The
phone shows a **pending** badge until then.

## When both sides change the same thing

If you edit a file on the phone *and* your computer commits a change to the same
lines before syncing, that's a genuine divergence. GitNomad doesn't dump raw git
conflict markers on you — it shows a simple **green/red review**. See
[Reviewing merges](merge-review.md).

Non-overlapping changes (different files, or different parts of a file) merge
automatically and silently.

## Polling and timing

The phone checks for updates every few seconds while a repo is open, so expect
changes to appear within roughly 2–4 seconds, not instantly. Pull down on a list
to refresh immediately.

---

Next: [Running code](running-code.md) · [Reviewing merges](merge-review.md) ·
[Troubleshooting](troubleshooting.md)
