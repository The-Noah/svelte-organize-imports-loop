# Svelte Organize Imports Loop

This is a minimal reproduction of a bug causing "organize imports" to loop forever.

[Discord thread](https://discord.com/channels/457912077277855764/1028066996341968936) - [Diff from starter template](https://github.com/The-Noah/svelte-organize-imports-loop/commit/bc386d0efac5a4541efc2b42e4adb2f7accdbd33)

## Steps to reproduce

1. Clone this repo `git@github.com:The-Noah/svelte-organize-imports-loop.git`
2. Run `npm install`
3. Open `src/App.svelte` in VS Code
4. Run `Organize Imports` command

To break out of the loop, open `.vscode/settings.json`.

> 💡 This seems to only happen when `source.organizeImports` is set to `true` in `settings.json`. It is then triggered by the `Organize Imports` command or saving.

### Steps taken to create this repo

1. Add `source.organizeImports` to `.vscode/settings.json`
2. Install Svelte for VS Code extension

## Environment

Below is my environment, I have not tested this on other environments.

- Svelte for VS Code v106.2.0
- VS Code 1.73.0-insider
- Windows 11
