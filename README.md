# moller-malt

Personal theme mono-repo.

## sddm/

Custom SDDM login theme based on [sddm-astronaut-theme](https://github.com/Keyitdev/sddm-astronaut-theme).

### Structure

```
sddm/
├── Assets/          # SVG icons (power, user, password, etc.)
├── Backgrounds/     # Background images
├── Components/      # QML UI components
├── Fonts/           # Bundled fonts
├── Main.qml         # Theme entry point
├── metadata.desktop # SDDM theme metadata
└── theme.conf       # Theme configuration
```

### NixOS Integration

The theme is packaged via `overrideAttrs` in `modules/desktop/hyprland.nix` in the [nixos config](https://github.com/chadmoller/nixos).
