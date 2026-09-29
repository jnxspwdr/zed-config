# zed-config

My Zed setup: `settings.json`, `keymap.json`, `AGENTS.md` (commit-message prompt).
This repo IS the Zed config directory (`%APPDATA%\Zed` on Windows).

## Set up a new machine

Close Zed first, then in a terminal:

```powershell
cd $env:APPDATA\Zed
git init
git remote add origin https://github.com/jnxspwdr/zed-config.git
git fetch origin
git checkout -f -B main origin/main
```

`-f` overwrites the default `settings.json`/`keymap.json` Zed created on first launch.
Extensions in `auto_install_extensions` install on the next launch.

## Machine-specific bits to check

- `wsl_connections` in `settings.json` names the `archlinux` WSL distro. Delete or edit it if the
  machine has no such distro.
- Fonts: `buffer_font_family` is Geist Mono; install it or change the setting.
- Some keybinds (e.g. the `space w` surround chords) are untested sketches; see comments in
  `keymap.json`.
