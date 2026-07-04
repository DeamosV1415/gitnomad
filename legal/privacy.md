---
layout: default
title: "GitNomad — Privacy Policy"
---

# GitNomad — Privacy Policy

**Effective date:** _[set on publish, e.g. 2026-07-04]_

> This is a plain-language starting template that describes how GitNomad
> actually works today. It is **not legal advice** — review it (and adapt the
> contact details, jurisdiction, and any future analytics/payment providers)
> before you publish it as your official policy.

GitNomad ("we", "the app") lets you open, edit, and sync your own code
repositories from your phone to your desktop. This policy explains what we
collect, why, and the control you have over it.

## Who we are

GitNomad is operated by _[your name / entity]_. Contact us about privacy at
**_[your contact email — e.g. privacy@gitnomad.dev]_**.

## What we collect

We only collect what the app needs to function. We do **not** sell your data,
show ads, or use third-party advertising or analytics trackers.

- **Account identity.** When you sign in with GitHub or Google, our
  authentication provider (Supabase) gives us your email address, a provider
  user id, and basic profile fields (such as your name or username). We use
  this to identify your account and scope your data to you.
- **Your repository content.** To sync between your phone and desktop, the code
  you choose to expose — files, commits, and unsaved edits — is transmitted to
  and temporarily stored on our relay server so your devices can exchange it.
  This is the core of what the app does. We do not read, analyze, or share the
  contents of your repositories.
- **Device links.** When you link a desktop, we store an opaque device token that
  associates that computer with your account.
- **Run output.** If you run a command on your desktop from the app, its output
  is passed through the relay so it can stream back to your phone.

We do not collect your location, contacts, photos, or advertising identifiers.

## How your data is handled

- **In transit:** connections between the app, our relay, and the auth provider
  use HTTPS/TLS.
- **Access control:** the relay verifies your signed-in identity on every request
  and isolates each account's repositories from every other account's.
- **Where it lives:** account identity is held by our authentication provider
  (Supabase); repository content and device links live on our relay server.

## How long we keep it

- Repository content stays on the relay until you **remove that repo** in the app
  (or the desktop stops exposing it), or until you delete your account.
- Account identity and device links are kept while your account exists.

## Deleting your data

You are in control:

- **Remove a repo** from the app to delete the relay's copy of it. Your local
  git repository on your own computer is never touched.
- **Delete your account** from **Profile → Delete account**. This permanently
  removes your synced repositories, unlinks your desktops, and deletes your
  sign-in record. This cannot be undone.

## Third parties we rely on

- **Supabase** — authentication and identity (processes your email and OAuth
  profile).
- **GitHub / Google** — only the OAuth sign-in you choose; we receive the profile
  fields above, nothing more.

We do not share your data with anyone else except as required to operate these
services or to comply with the law.

## Children

GitNomad is not directed at children under 13, and we do not knowingly collect
their data.

## Changes

If we change this policy, we will update the effective date above and, for
material changes, surface a notice in the app.

## Contact

Questions or requests: **_[your contact email]_**.
