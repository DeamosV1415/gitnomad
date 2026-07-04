# Reviewing merges

Sometimes you and your computer change the **same lines** of the same file before
they've had a chance to sync. That's a divergence. Instead of showing you raw git
conflict markers, GitNomad gives you a simple **green/red review**.

## When a review appears

You'll see a **"Changes to review"** card at the top of a repo's file list when:

- you edited and pushed a file from the phone, **and**
- your computer committed a change to an **overlapping** part of the same file,
- before either side synced.

Changes that **don't** overlap — different files, or different regions of the same
file — are merged automatically and silently. You only review true conflicts.

## How to resolve

1. Tap the **Changes to review** card.
2. You'll see:
   - a summary of files that merged automatically, and
   - one card per real conflict.
3. For each conflicting chunk, pick which version to keep:
   - **Phone** (green) — your phone's version,
   - **Desktop** (blue) — your computer's version, or
   - **Both** — keep both, one after the other.
   - For a file one side deleted and the other changed: choose **Keep** or
     **Delete**.
4. Tap **Apply**.

GitNomad then creates a single **merge commit** that combines both sides. Your
phone and your computer both move to that merged result, so you're back in sync
with nothing lost.

## Good to know

- Nothing is discarded until you tap **Apply** — reviewing is safe.
- The merge is a normal 2-parent git commit, so your history honestly records that
  both sides contributed.
- Overlapping edits are uncommon in practice, because your computer is usually
  idle (or off) while you're editing from your phone.

Stuck on a review? → [Troubleshooting → A review won't go away](troubleshooting.md#a-review-wont-go-away).
