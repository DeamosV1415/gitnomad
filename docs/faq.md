---
layout: default
title: "FAQ"
---

# FAQ

### Is GitNomad free?

Yes — the core experience (edit, two-way sync, run on your own computer) is free.
A **Pro** plan is planned for cloud features like running your code when your
computer is **off**.

### Does GitNomad work when my computer is off?

Not on the free plan. Today your computer does the real work, so it needs to be
on and connected. **Cloud run** (for when your PC is off) is on the roadmap as a
Pro feature. Your phone edits made while the computer is off are safely queued and
delivered when it comes back.

### Does "Push" send my code to GitHub?

No. In GitNomad, **Push** sends your change **to your own computer**, as a git
commit. Pushing to a GitHub remote is a separate action routed through your
computer. See [How syncing works](syncing.md).

### Is my code safe? Who can see it?

Your repos are private to your account. To sync between devices, the code you
choose to share passes through and is temporarily stored on GitNomad's sync
service — we don't read, analyze, or share it. Your local repository on your
computer is always the source of truth. See the
[Privacy Policy](../legal/privacy.md) and [Account & your data](account-and-data.md).

### What platforms are supported?

The app is **Android** today; iOS is planned. The desktop side is a **VS Code**
extension, which also works in VS Code–compatible editors.

### Which languages does the editor highlight?

Many — including Python, JavaScript/TypeScript, JSON, HTML, CSS, Markdown, Rust,
C/C++, Java, Go, SQL, PHP, YAML, and more. Unknown file types open as plain text.

### Do I need Android Studio or any developer tools on my phone?

No. You just install the app from Google Play.

### Can I use more than one computer?

Yes. Link each computer once with its own code (**Profile → Link desktop**). They
all share your account's repos.

### Can I self-host?

The app points at GitNomad's hosted sync service by default, and most people never
need to change that. Advanced users can point it at their own service in Settings.

### How do I delete my account and data?

**Profile → Delete account** — it permanently removes your synced repos and
unlinks your desktops. Your local code isn't touched. See
[Account & your data](account-and-data.md).

### I have another question / found a bug.

Check [Troubleshooting](troubleshooting.md) first, then
[open an issue](https://github.com/DeamosV1415/gitnomad/issues/new/choose) or
[start a discussion](https://github.com/DeamosV1415/gitnomad/discussions).
