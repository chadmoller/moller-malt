# moller-malt — Claude Instructions

## Repository Structure

- `sddm/` — Custom SDDM login theme (based on sddm-astronaut-theme)
  - `Assets/` — SVG icons (power, reboot, suspend, user, password)
  - `Backgrounds/` — Background images; `login-splash.png` is the active background
  - `Components/` — QML UI components (Clock, LoginForm, Input, etc.)
  - `Fonts/` — Bundled fonts
  - `Main.qml` — Theme entry point
  - `metadata.desktop` — SDDM theme metadata (Name, Theme-Id must be `moller-malt`)
  - `theme.conf` — All visual/behaviour configuration

## Key conventions

- Theme name/id is always `moller-malt` — do not change
- `theme.conf` is the single config file (no `Themes/` subdirectory)
- Commit style: `feat(scope):`, `fix(scope):` conventional commits
- The nixos config at `chadmoller/nixos` consumes this repo as a flake input

## NixOS integration

When theme files change, update the flake input in the nixos repo:
```
nix flake update moller-malt
```
then rebuild with `nixos-rebuild switch`.
