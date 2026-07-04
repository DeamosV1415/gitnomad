# Getting started

This guide takes you from zero to your first synced edit. It takes about five
minutes.

## What you'll need

- An **Android phone**.
- A **computer** with [Visual Studio Code](https://code.visualstudio.com/)
  installed and **git** available.
- A **GitHub or Google account** to sign in with.
- A **git project** on your computer that you want to work on.

> On the free plan, your computer does the real work — so it needs to be **on and
> connected** while you sync from your phone.

## Step 1 — Install the app and sign in

1. Install **GitNomad** from
   [Google Play](https://play.google.com/store/apps/details?id=dev.gitnomad.app).
2. Open it and tap **Continue with GitHub** or **Continue with Google**.
3. Approve the sign-in in the browser sheet that opens. You'll land on your home
   screen, which will be empty until you connect a computer.

Every repo you sync is tied to your account, so signing in is required.

## Step 2 — Install the VS Code extension

1. On your computer, open VS Code.
2. Go to the **Extensions** panel and search for **GitNomad Desktop** (or install
   it from the
   [Marketplace](https://marketplace.visualstudio.com/items?itemName=gitnomad.gitnomad-desktop)).
3. Once installed, you'll see a **GitNomad icon** in the activity bar (the strip
   of icons on the left). Click it to open the GitNomad panel.

## Step 3 — Link your computer to your account

The extension needs to know it belongs to *you*. You prove that with a short code
from the app.

1. On your **phone**: go to **Profile → Link desktop**. You'll see a 6-digit code.
2. In VS Code's **GitNomad panel**, click **Link to my account** and enter that
   code.
3. The panel will switch to a connected state. Done — your computer is now bound
   to your account.

The code is single-use and expires after a few minutes. If it runs out, just
tap **New code** on the phone.

More detail and fixes: [Linking your desktop](linking-desktop.md).

## Step 4 — Choose which repos to share

By default, GitNomad exposes the git project(s) open in your VS Code window. To
add a specific folder, use **Add a repo** in the GitNomad panel and pick a folder
that's a git repository.

Within a few seconds, those repos appear in the app on the **Repos** tab.

## Step 5 — Make your first sync

1. On the phone, tap a repo, then tap a file to open it.
2. Change something and tap **Save** (and **Push** if prompted).
3. Look at the file in VS Code on your computer — your edit is there, as a commit.

Now try the other direction: edit and save the same file in VS Code. Within a few
seconds the phone shows your change (even before you commit — see
[live drafts](syncing.md#live-drafts)).

## What next?

- [Run a command on your computer from your phone](running-code.md)
- [Understand how syncing works](syncing.md)
- Something not working? → [Troubleshooting](troubleshooting.md)
