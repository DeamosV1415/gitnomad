<div align="center">

# GitNomad

### Code from your pocket.

Open your real desktop project on your phone, edit it, sync every change back to
your computer, and run it — wherever you are.

[**Documentation**](docs/README.md) · [**Report a bug**](https://github.com/DeamosV1415/gitnomad/issues/new/choose) · [**Discussions**](https://github.com/DeamosV1415/gitnomad/discussions) · [**Privacy**](legal/privacy.md) · [**Terms**](legal/terms.md)

</div>

---

## What is GitNomad?

GitNomad is a mobile code editor that stays in sync with your real desktop
project. You edit a file on your phone; the change lands on your computer as a
git commit. You edit on your computer; it shows up on your phone. When you want
to run something, GitNomad runs it on your machine and streams the output back
to your pocket.

It's built for solo developers who get ideas away from their desk — on the bus,
on the couch, in a queue — and want to act on them without opening a laptop.

> **This repository** is GitNomad's public home: documentation, issue tracking,
> and legal pages. The app itself is a separate product — grab it from the links
> below.

## Get GitNomad

| Where | What | Link |
|-------|------|------|
| 📱 **Android app** | The mobile editor | [Google Play](https://play.google.com/store/apps/details?id=dev.gitnomad.app) *(live at launch)* |
| 🖥️ **VS Code extension** | Connects your desktop | [Marketplace](https://marketplace.visualstudio.com/items?itemName=gitnomad.gitnomad-desktop) *(live at launch)* |

## Features

- **Edit anywhere** — open any file in your synced repos with real syntax
  highlighting for dozens of languages.
- **Two-way sync** — changes flow both directions. Your phone edits become
  commits on your desktop; your desktop edits (even unsaved ones) appear on your
  phone within seconds.
- **Run your code** — trigger a command from your phone and watch the live output
  stream back from your computer.
- **Safe merges** — if you and your desktop both change the same lines, GitNomad
  shows a simple green/red review instead of raw git conflict markers.
- **Your code stays yours** — your local git repository on your computer is always
  the source of truth. Nothing is published to GitHub unless you ask.

## How it works (in 30 seconds)

1. You install the **VS Code extension** on your computer and link it to your
   account.
2. The extension exposes the repos you choose to GitNomad's sync service.
3. The **phone app** shows those repos. You browse, edit, and run.
4. Every change is carried between your phone and your computer by the sync
   service — safely, and by commit, so your history stays intact.

Your computer (with VS Code and the extension running) does the real work on the
free plan, so keep it on and connected while you're syncing. Cloud execution for
when your PC is **off** is on the roadmap.

## Quick start

1. **Install the app** and sign in with GitHub or Google.
2. **Install the VS Code extension**, open your project, and open the GitNomad
   panel in the sidebar.
3. On the phone: **Profile → Link desktop** to get a code. Enter it in the
   extension's **Link to my account**.
4. Your repo appears on the phone. Open a file, edit, save — it's on your
   computer.

Full walkthrough: [**Getting started**](docs/getting-started.md).

## Documentation

Having trouble or want to go deeper? The docs cover everything:

- [Getting started](docs/getting-started.md)
- [Linking your desktop](docs/linking-desktop.md)
- [How syncing works](docs/syncing.md)
- [Running code](docs/running-code.md)
- [Reviewing merges](docs/merge-review.md)
- [Account & your data](docs/account-and-data.md)
- [**Troubleshooting**](docs/troubleshooting.md) — fixes for common problems
- [FAQ](docs/faq.md)

## Support & feedback

- 🐛 **Found a bug?** [Open an issue](https://github.com/DeamosV1415/gitnomad/issues/new/choose).
- 💡 **Have an idea?** [Start a discussion](https://github.com/DeamosV1415/gitnomad/discussions)
  or open a feature request.
- 📧 **Something private?** Email **_[support@gitnomad.dev]_**.

Please check [Troubleshooting](docs/troubleshooting.md) and existing issues first —
your problem may already have an answer.

## Roadmap

- ✅ Two-way sync, live drafts, merge review, run-on-desktop
- ✅ Sign in with GitHub / Google
- 🔜 Interactive terminal
- 🔜 **Cloud run** — execute when your PC is off (Pro)
- 🔜 iOS

---

<div align="center">
<sub>© 2026 GitNomad. The GitNomad app and extension are proprietary. This
repository (documentation, issues, and legal pages) is public for the community.</sub>
</div>
