Personal fork of [AzizStark/talis](https://github.com/AzizStark/talis), for niri.

Changes:
- The layer-shell layer is chosen at build time with `TALIS_LAYER`
  (`src/desktop/wayland.rs`). The Arch package uses `background`; set
  `TALIS_LAYER=bottom` for the original behaviour.
- Only the 1080p scenes are required and packaged (`src/resources.rs`).
- `packaging/arch-fork/PKGBUILD` builds a Wayland-only package from this checkout:
  `cd packaging/arch-fork && makepkg -f && sudo pacman -U talis-fork-*.pkg.tar.zst`

All credit for Talis goes to AzizStark.
