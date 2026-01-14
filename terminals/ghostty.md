# Ghostty

Fast, native, GPU-accelerated terminal emulator.

## Overview

- **Website:** https://ghostty.org
- **Repository:** https://github.com/ghostty-org/ghostty
- **License:** MIT
- **Language:** Zig (80.0%), Swift (11.3%), C++ (3.4%), C (2.7%)
- **First Release:** v1.0 on December 26, 2024
- **Latest Version:** 1.2.3
- **Status:** Active development
- **Creator:** Mitchell Hashimoto (HashiCorp co-founder)
- **GitHub Stars:** 41.4k
- **Contributors:** 467+

## Platform Support

| Platform | Support | Installation |
|----------|---------|--------------|
| macOS | ✅ Full (requires macOS 13+) | `brew install --cask ghostty` or direct download |
| Linux | ✅ Full | Multiple package managers, AppImage, Snap, build from source |
| Windows | 🚧 Planned | Not yet available |
| BSD | ❌ Not supported | - |

### Installation Methods

**macOS:**
- Direct download: Universal binary from ghostty.org/download
- Homebrew: `brew install --cask ghostty`

**Linux (Official Packages):**
- Alpine: `apk add ghostty`
- Arch: `pacman -S ghostty`
- Gentoo: `emerge -av ghostty`
- NixOS: Available in nixpkgs
- openSUSE: `zypper install ghostty`
- Snap: `snap install ghostty --classic`
- Solus: `eopkg install ghostty`
- Void: `xbps-install ghostty`

**Build from Source:**
- Requires Zig compiler (0.14.1 for Ghostty 1.2.x)
- macOS: Requires Xcode with macOS/iOS SDKs
- Linux: Requires GTK4, libadwaita, gtk4-layer-shell
- Command: `zig build -Doptimize=ReleaseFast`

## Features

### Rendering & Graphics
- **GPU Acceleration:** ✅ Yes
  - macOS: Metal (native Apple GPU framework)
  - Linux: OpenGL
- **Note:** Only terminal besides iTerm2 using Metal directly on macOS
- **Font Ligatures:** ✅ Full support
- **True Color (24-bit):** ✅ Yes
- **FPS:** ~60fps under load, 480-500 FPS in DOOM fire test

### Window Management
- **Tabs:** ✅ Native platform tabs using system UI
- **Splits/Panes:** ✅ Multiple split directions (left, right, up, down, auto)
  - Focus navigation, resize, equalize
  - Individual split zoom capability
  - Configurable via keybindings
- **Scrollback:** Unlimited

### Image Support
- **Inline Images:** ✅ Yes
- **Protocol:** Kitty graphics protocol
- **Sixel:** ❌ Not supported (explicitly will not be implemented)

### Themes & Customization
- **Themes:** Hundreds built-in (sourced from iterm2-color-schemes, updated weekly)
- **Custom Themes:** ✅ Yes
- **Theme Management:**
  - Single-line: `theme = Catppuccin Frappe`
  - Light/dark modes: `theme = dark:Catppuccin Frappe,light:Catppuccin Latte`
  - List themes: `ghostty +list-themes`
- **Custom Theme Location:** `$XDG_CONFIG_HOME/ghostty/themes/`
- **Hot Reload:** ✅ Yes (`ctrl+shift+,` on Linux, `cmd+shift+,` on macOS)

### Configuration
- **Format:** Custom text-based key=value syntax (INI-style)
- **Location:**
  - XDG: `$XDG_CONFIG_HOME/ghostty/config` (default: `~/.config/ghostty/config`)
  - macOS: `~/Library/Application Support/com.mitchellh.ghostty/config`
- **Features:**
  - Comments with `#`
  - Quoted or unquoted values
  - Multi-file support via `config-file` key
  - Keys work as CLI flags: `ghostty --background=282c34`
- **Philosophy:** Zero configuration required; hundreds of options available

Example config:
```
font-family = "JetBrains Mono"
font-size = 14
theme = "catppuccin-mocha"
```

## Performance

| Metric | Value | Source |
|--------|-------|--------|
| FPS (DOOM fire test) | 480-500 FPS | GitHub discussions |
| Startup Time (Linux) | ~140ms | Official benchmarks |
| Latency (10k-line scroll) | 2ms | 37% better than Alacritty |
| Memory Usage | Peak RSS ~106MB | Early benchmarks |
| Real-world Performance | 4x faster than iTerm2, Kitty | 4GB data dump test |

**Note:** Ongoing optimization across throughput, memory, frame times, and input latency. A major 37GB memory leak was discovered and fixed post-release.

## Unique Features

### Core Philosophy: No Trade-offs
Ghostty refuses to compromise between three traditionally exclusive qualities:
1. **Speed** - GPU-accelerated, performance-engineered
2. **Features** - Comprehensive modern terminal features
3. **Native UI** - Platform-native components

### Platform-Native Integration

**macOS:**
- True SwiftUI/AppKit application (not cross-platform wrapper)
- Metal rendering (only terminal besides iTerm2)
- Quick Terminal (menu bar animation)
- Native tabs, splits, context menus
- Dock integration, proxy icon, Quick Look
- Secure keyboard entry with visual indicator
- System input methods (emoji, dictation)

**Linux:**
- GTK4/libadwaita implementation
- gtk4-layer-shell support
- systemd and D-Bus integration

### libghostty Architecture
- Core terminal emulation in cross-platform C-compatible library
- Platform-specific GUIs consume shared foundation
- Enables other developers to build terminals using Ghostty's engine
- WebAssembly support via libghostty-vt library

### Standards Compliance
- Superior xterm escape sequence support
- ECMA-48 compliance
- Kitty keyboard protocol
- Kitty graphics protocol
- Synchronized rendering
- Light/dark mode notifications

## Documentation

- Official Docs: https://ghostty.org/docs
- Features: https://ghostty.org/docs/features
- Configuration: https://ghostty.org/docs/config
- Installation: https://ghostty.org/docs/install
- Building: https://ghostty.org/docs/install/build

## Development

- **Model:** Open source (MIT), passion project
- **History:** ~2 years private beta with ~2,000 testers before December 2024 public release
- **Creator:** Mitchell Hashimoto (not full-time work)
- **Vision:** Enable ecosystem of diverse terminal implementations on shared foundation

## Sources

All data collected from official sources:

- [Ghostty Official Documentation](https://ghostty.org/docs) - Accessed 2026-01-14
- [Ghostty GitHub Repository](https://github.com/ghostty-org/ghostty) - Accessed 2026-01-14
- [Ghostty Features](https://ghostty.org/docs/features) - Accessed 2026-01-14
- [Ghostty Configuration](https://ghostty.org/docs/config) - Accessed 2026-01-14
- [Mitchell Hashimoto - Ghostty 1.0](https://mitchellh.com/writing/ghostty-is-coming) - Accessed 2026-01-14
- [Mitchell Hashimoto - Ghostty Reflection](https://mitchellh.com/writing/ghostty-1-0-reflection) - Accessed 2026-01-14
- [GitHub Performance Discussion #4837](https://github.com/ghostty-org/ghostty/discussions/4837) - Accessed 2026-01-14
- [LWN.net - Ghostty 1.0](https://lwn.net/Articles/1004377/) - Accessed 2026-01-14

[← Back to Comparison](../comparison.md)
