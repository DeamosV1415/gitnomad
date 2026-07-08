# Changelog

All notable changes to GitNomad are documented here. Dates use YYYY-MM-DD.

## Terminal update

Improvements to running commands from your phone.

### Added

- **Terminal tabs** — open several terminals per repo, each with its own
  scrollback and working directory, remembered across restarts.
- **Working-directory navigation** — `cd` into subfolders (and `clear`); commands
  run where you are, not only at the repo root.
- **Interactive input** — answer prompts (like Python's `input()`) by typing in
  the terminal while a command runs.
- **Shell picker** — choose which shell runs your commands on the desktop (OS
  default, PowerShell, pwsh, cmd, or bash), with the active shell shown in the app.
- **Command history** — recall recent commands from chips above the prompt.

### Fixed

- Commands run in a subfolder no longer hang and can be stopped reliably (desktop
  extension 0.1.2).
- Output streams live instead of appearing only when the command finishes.

---

## [1.0.0] — first release

The first public release of GitNomad.

### Highlights

- **Mobile code editor** for Android with syntax highlighting for many languages.
- **Two-way sync** between your phone and your computer through a secure cloud
  sync service.
- **Live drafts** — see your computer's unsaved edits on your phone within
  seconds.
- **Run on desktop** — trigger a command on your computer and watch the output
  stream back to your phone.
- **Green/red merge review** — resolve overlapping edits without raw git conflict
  markers.
- **Sign in with GitHub or Google.**
- **VS Code extension** to expose your repos and link a computer to your account.
- **Full control of your data** — remove a repo or delete your account from within
  the app at any time.

---

_Older pre-release history is not published._
