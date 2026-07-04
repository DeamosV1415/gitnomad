---
layout: default
title: "Linking your desktop"
---

# Linking your desktop

Your phone and your computer need to know they belong to the same account. This
is a one-time setup per computer, done with a short code.

## Why linking exists

Every repo in GitNomad is private to your account. The phone proves who you are
by signing in. Your computer proves it's yours by **redeeming a link code** that
only your signed-in phone can create. After that, the computer holds a secure
device token and stays linked — you won't need to do this again unless you
unlink or reinstall.

## How to link

1. **On the phone:** open **Profile → Link desktop**. A 6-digit code appears,
   along with the command form for advanced users. The code is **single-use** and
   expires in a few minutes.
2. **On the computer:** open the **GitNomad panel** in VS Code's sidebar and click
   **Link to my account**. Paste or type the code.
3. The panel switches to **linked**. Your repos start syncing.

If the code expires before you use it, tap **New code** on the phone for a fresh
one.

## Choosing which repos to share

- Open the folder you want to work on in VS Code — if it's a git repo, GitNomad
  can expose it.
- Use **Add a repo** in the panel to pick a specific folder.
- Each shared repo shows up on the phone's **Repos** tab with a live status badge.

## Sync status badges

In both the extension and the app you'll see a per-repo status:

| Badge | Meaning |
|-------|---------|
| **synced** | Everything is up to date. |
| **N pending** | The phone has changes your computer hasn't picked up yet (usually because it's offline or paused). |
| **desktop offline** | Your computer hasn't checked in recently — start VS Code / the extension. |

## Unlinking or removing

- **Remove a repo** from the phone (trash icon) deletes the cloud copy of it. Your
  local files on your computer are untouched. If the extension is still exposing
  that folder, it can reappear — remove it in the extension to make it permanent.
- **Remove a repo** in the extension (✕ on the card) stops exposing that folder
  and deletes the cloud copy.
- To unlink a computer entirely, delete its GitNomad device entry (re-link later
  with a new code).

## Trouble linking?

See [Troubleshooting → Linking and connection](troubleshooting.md#linking-and-connection).
Common causes: an expired code, the extension not running, or the computer being
offline.
