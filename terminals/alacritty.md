# Alacritty

GPU-accelerated terminal emulator focused on performance and simplicity.

## Overview

- **Website:** https://alacritty.org
- **Repository:** https://github.com/alacritty/alacritty
- **License:** Apache-2.0 / MIT (dual-licensed)
- **Language:** Rust (96%)
- **First Release:** January 6, 2017
- **Latest Version:** 0.16.1 (October 20, 2025)
- **Status:** Beta-level readiness, actively maintained and widely used

## Platform Support

| Platform | Support | Installation |
|----------|---------|--------------|
| macOS | ✅ Full (x86_64 + ARM64) | `brew install --cask alacritty` or DMG |
| Linux | ✅ Full (X11 + Wayland) | Package managers or `cargo install alacritty` |
| Windows | ✅ Full (Windows 10 1809+) | MSI installer, Chocolatey, or portable executable |
| BSD | ✅ FreeBSD, OpenBSD | Build from source with cargo |

### Installation Methods

**macOS:**
- DMG installer from GitHub releases
- Homebrew: `brew install --cask alacritty`
- Build: `make app` or `make app-universal` (universal binary)

**Linux:**
- Cargo: `cargo install alacritty`
- Package managers in all major distributions
- Build from source: `cargo build --release`
- Backend selection: Wayland-only, X11-only, or both

**Windows:**
- MSI installer from GitHub releases
- Chocolatey: `choco install alacritty`
- Portable executable

**Dependencies (Linux):**
cmake, pkg-config, libfontconfig, libxcb, libxkbcommon, Python 3

## Features

### Rendering & Graphics
- **GPU Acceleration:** ✅ Yes
  - Technology: OpenGL / OpenGL ES
  - GLSL3 renderer (modern OpenGL with GLSL 3.3+)
  - GLES2 renderer (OpenGL ES 2.0 for compatibility)
  - Minimum: OpenGL ES 2.0 support
- **Font Ligatures:** ❌ Not supported (deliberate performance decision)
- **True Color (24-bit):** ✅ Full support out-of-the-box

### Window Management
- **Tabs:** ❌ Not supported (by design - delegates to tmux/screen/zellij)
- **Splits/Panes:** ❌ Not supported (by design - delegates to multiplexers)
- **Multi-Window:** ✅ Single process manages multiple windows efficiently
- **Philosophy:** Composition over features; favors integration with external tools

### Image Support
- **Images:** ❌ Not supported
  - No Kitty Graphics Protocol
  - No iTerm2 inline image protocol
  - No Sixel graphics
- **Workaround:** On X11/Wayland, can use Überzug++ with "Window system protocol"

### Themes & Customization
- **Themes:** 234 color schemes in alacritty-theme repository
- **Custom Themes:** ✅ Yes, via TOML configuration
- **Theme Tools:**
  - alacritty-themes CLI (150+ themes)
  - alacritty-colors for color science-based generation
- **Note:** No built-in themes; all external configuration

### Configuration
- **Format:** TOML (Tom's Obvious, Minimal Language)
- **Location (priority order):**
  1. `$XDG_CONFIG_HOME/alacritty/alacritty.toml`
  2. `$XDG_CONFIG_HOME/alacritty.toml`
  3. `$HOME/.config/alacritty/alacritty.toml`
  4. `$HOME/.alacritty.toml`
  5. `/etc/alacritty/alacritty.toml`
- **Windows:** `%APPDATA%\alacritty\alacritty.toml`
- **Hot Reload:** ✅ Yes
- **Documentation:** `man 5 alacritty` or https://alacritty.org

## Performance

### Design Philosophy
Performance is the primary differentiator - explicitly designed as a high-performance terminal emulator.

| Metric | Value | Notes |
|--------|-------|-------|
| Startup Time | ~50ms | Fastest among modern terminals |
| Memory Usage | ~30MB baseline | Can increase with activity |
| Input Latency | Very Low | 2018 LWN: "closely followed by... Alacritty, expressly designed for speed" |
| FPS | 500 FPS with 30MB footprint | GPU-accelerated rendering |

### Benchmarking
- **vtebench:** Official tool created by Alacritty team
  - Measures terminal throughput (PTY read speed)
  - "Alacritty manages to consistently score better than the competition"
  - Repository: https://github.com/alacritty/vtebench

**Sample Benchmark Results (milliseconds, lower is better):**
- ManyLine: Alacritty 113.76s vs WezTerm 132.50s
- FGPerChar: Alacritty 21.89s vs WezTerm 39.34s

## Unique Features

### Core Design Philosophy
1. **Performance First:** GPU acceleration differentiates from CPU-based terminals
2. **Composition Over Features:** Deliberately minimal, favors external tools
3. **Minimalism with Configuration:** Sensible defaults with extensive customization
4. **No GUI Configuration:** Text files only

### Built-in Features
- **Vi Mode:** Built-in vi-mode navigation and selection
- **Search:** Search across scrollback buffer
- **Regex Hints:** Mark and interact with text using regex patterns
- **Scrollback:** Configurable scrollback history
- **Cross-Platform Consistency:** Same OpenGL rendering on all platforms
- **Memory Safety:** Written in Rust for memory-safe, concurrent code

### What Makes Alacritty Special
- Consistently benchmarks as one of the fastest terminal emulators
- Created vtebench (official terminal benchmarking tool)
- Minimal philosophy: Limited feature set by design
- Delegates tabs/splits to ecosystem (tmux, multiplexers)
- Modern stack: Rust + OpenGL

### Limitations (By Design)
- No font ligatures (performance decision - issue #50 since 2017)
- No tabs/splits (delegates to multiplexers)
- No image protocols (not yet implemented)
- No GUI configuration
- Beta status (acknowledged missing features)

## Documentation

- Official Website: https://alacritty.org
- GitHub: https://github.com/alacritty/alacritty
- Changelog: https://alacritty.org/changelog.html
- Man Page: `man 5 alacritty`

## Sources

All data collected from official sources:

- [Alacritty Official Website](https://alacritty.org/) - Accessed 2026-01-14
- [Alacritty GitHub Repository](https://github.com/alacritty/alacritty) - Accessed 2026-01-14
- [Alacritty Releases](https://github.com/alacritty/alacritty/releases) - Accessed 2026-01-14
- [Alacritty Theme Repository](https://github.com/alacritty/alacritty-theme) - Accessed 2026-01-14
- [vtebench Tool](https://github.com/alacritty/vtebench) - Accessed 2026-01-14
- [Announcing Alacritty Blog](https://jwilm.io/blog/announcing-alacritty/) - Accessed 2026-01-14
- [LWN.net Terminal Analysis](https://lwn.net/Articles/751763/) - Accessed 2026-01-14
- [Font Ligatures Issue #50](https://github.com/alacritty/alacritty/issues/50) - Accessed 2026-01-14

[← Back to Comparison](../comparison.md)
