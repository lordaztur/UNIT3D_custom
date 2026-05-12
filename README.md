# UNIT3D_custom — Catppuccin Mocha Theme Override

A custom theme override for UNIT3D-based trackers. Builds on the official Material Design v3 Dark theme and applies a yellow-dominant Catppuccin Mocha-inspired pastel palette over warm charcoal surfaces, with Outfit typography and softer radii/shadows.

## Files

- `catppuccin-mocha-overrides.css` — the theme override (the only file you need to deploy).
- `material-design-v3-dark.css` — UNIT3D's base theme, included here as the reference target (do not deploy this file unless you're missing it upstream).
- `cbr.css` / `main-6Vf30Upt.css` — reference artifacts used during design (not deployed).
- `test/verify.html` — open in a browser to confirm the override took effect (computed-style assertions).
- `test/preview.html` — visual showcase of representative UNIT3D components with the override applied.

## Install

1. Copy `catppuccin-mocha-overrides.css` into your UNIT3D fork's public CSS directory (typically `public/css/`).
2. In the main layout template (typically `resources/views/layout.blade.php` or wherever the theme `<link>` lives), add the override **after** the base theme:

   ```html
   <link rel="stylesheet" href="/css/material-design-v3-dark.css">
   <link rel="stylesheet" href="/css/catppuccin-mocha-overrides.css">
   ```

3. Hard-refresh. Verify via `test/verify.html` (should report all assertions passing).

To roll back, remove the single `<link>` line.

## Palette

| Role | Hex |
|------|-----|
| Primary (brand) | `#f9e2af` Mocha Yellow |
| Secondary | `#fab387` Mocha Peach |
| Tertiary | `#f5e0dc` Mocha Rosewater |
| Surfaces | `#161412` / `#0e0d0c` / `#221f1c` / `#2f2b27` (warm charcoal ramp) |
| Text | `#cdd6f4` / `#a6adc8` / `#6c7086` |
| Success / Seeders | `#a6e3a1` Mocha Green |
| Danger / Leechers | `#f38ba8` Mocha Red |
| Info / Links | `#89b4fa` Mocha Blue |
| Accent (premium) | `#cba6f7` Mocha Mauve |
| Accent (cool) | `#94e2d5` Mocha Teal |

## License

The override file (`catppuccin-mocha-overrides.css`) is released as-is, free to fork and modify. The bundled `material-design-v3-dark.css` and `main-6Vf30Upt.css` belong to the upstream UNIT3D project and retain their original UNIT3D license.
