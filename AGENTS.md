# OpenCode Activity Monitor

Python overlay application with shared code in `src/` and platform implementations in `macos/`, `omarchy/`, and `windows/`.

## Boundaries

- Keep cross-platform session discovery and configuration behavior in `src/`; put platform UI and installer behavior in its platform directory.
- Preserve config compatibility: user configuration overrides defaults, and TOML loading supports both Python 3.11+ and older supported Python via `tomli`.
- Linux overlay support targets Hyprland/wlroots with GTK4 layer shell. macOS uses PyObjC/AppKit. Keep platform-specific dependencies out of shared code.
- When changing config, update `DEFAULT_CONFIG`, `config.toml`, and user-facing README documentation together.

README contains current run, install, and platform dependency instructions.
