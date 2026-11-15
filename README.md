# Tome of Heroes

A Windows app for D&D 5e (2014 rules) characters that calculates your numbers and automates leveling up: subclass
picks, class and racial features, feature choices (invocations, maneuvers, metamagic, fighting styles…), spells and
spell slots. One file, `TomeOfHeroes.exe`; your characters stay on your PC.

This repo only holds the releases. Download the latest `TomeOfHeroes.exe` from
[Releases](https://github.com/martijnakkerman/tome-of-heroes-releases/releases/latest).

## Please read

- **Built largely with AI assistance (Claude).** The code and the rules automation can contain mistakes — check
  important numbers against your books.
- **Unofficial fan project.** Not affiliated with or endorsed by Wizards of the Coast. Dungeons & Dragons is their
  trademark.
- **No game content is included.** The app needs a content file from whoever shared it with you; it's built from a
  fan wiki for personal use. Don't redistribute it, and don't post it here.
- **The exe isn't code-signed**, so Windows SmartScreen may warn the first time you run it and after updates
  ("More info → Run anyway").

## Getting started

1. Download `TomeOfHeroes.exe` from the latest release and put it in a folder of your choice.
2. Run it. The first time, it asks for your **content file** (`tome-content-….json`): click **Import content file…**
   and pick it.
3. Your characters are stored in `%APPDATA%\TomeOfHeroes\characters.db` (with a backup copy refreshed on every
   start). **Export** saves a character as a `.json` file; **Import** brings one back.

## Updates

New versions are offered inside the app: **Settings** (the gear in the toolbar) → **Check for updates**, or the quiet
check once a day on start (you can turn it off), which puts a badge on the gear. **Update now** downloads the new
version from this repo, checks it against the published `TomeOfHeroes.exe.sha256`, and restarts the app. Your
characters are kept.

To check a download yourself: `Get-FileHash TomeOfHeroes.exe -Algorithm SHA256` in PowerShell should match the
release's `.sha256` file.
