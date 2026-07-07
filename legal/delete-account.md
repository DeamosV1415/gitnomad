---
layout: default
title: "GitNomad — Account & Data Deletion"
---

# GitNomad — Account & Data Deletion

**Effective date:** 2026-07-07

This page explains how to delete your GitNomad account and the data associated
with it. It applies to the GitNomad mobile app (package `dev.gitnomad.app`).

## Delete your account from the app (fastest)

1. Open GitNomad and sign in.
2. Go to **Profile → Delete account**.
3. Confirm.

This permanently and immediately:

- deletes your synced **repository content** (files, commits, unsaved edits, and
  any command-run output) from our relay server,
- **unlinks all your desktops** (their device tokens are revoked), and
- removes your **sign-in record** (email and OAuth profile) from our
  authentication provider.

This cannot be undone. Your **local git repositories on your own computer are
never touched** — only the cloud copy used for syncing is removed.

You can also remove a single repository without deleting your account: use
**Remove repo** in the app to delete just that repo's relay copy.

## Request deletion without the app

If you can no longer access the app, email **gitnomad.app@gmail.com** from the
email address you signed in with and ask us to delete your account. We will
verify ownership and delete your account and its data within **30 days**.

## What is deleted vs. retained

- **Deleted:** email address, OAuth user id and basic profile fields, device
  link tokens, all synced repository content, and command-run output.
- **Retained:** nothing tied to your identity after deletion completes. We keep
  no backups of your repository content beyond what is needed to operate the
  service, and transient logs (if any) are purged on our normal rotation
  schedule. We may retain minimal records only where required by law.

## Contact

Questions about deletion: **gitnomad.app@gmail.com**.
