# Kitty

GPU-accelerated, feature-rich terminal emulator with advanced protocols.

## Overview

- **Website:** https://sw.kovidgoyal.net/kitty/
- **Repository:** https://github.com/kovidgoyal/kitty
- **License:** GPL-3.0
- **Languages:** Python (38.9%), C (28.2%), Go (25.7%), Objective-C (5.4%)
- **First Release:** v0.4.0 on October 22, 2017
- **Latest Version:** 0.45.0 (December 24, 2025)
- **Status:** Actively maintained
- **Developer:** Kovid Goyal
- **GitHub Stars:** 30.7k
- **Contributors:** 373+

## Platform Support

| Platform | Support | Installation |
|----------|---------|--------------|
| macOS | ✅ Full (macOS 11+) | `brew install --cask kitty` or curl installer |
| Linux | ✅ Full (all major distros) | Package managers or curl installer |
| BSD | ✅ Supported | Various BSD variants |
| Windows | ❌ Not supported | Unix-only by design |

### Installation Methods

**macOS:**
- Binary installer: `curl -L https://sw.kovidgoyal.net/kitty/installer.sh | sh /dev/stdin`
- Homebrew: `brew install --cask kitty`
- MacPorts: Available
- Download: `.dmg` from GitHub releases

**Linux:**
- Binary installer: `curl -L https://sw.kovidgoyal.net/kitty/installer.sh | sh /dev/stdin`
- Ubuntu/Debian: `sudo apt install kitty`
- Arch: `sudo pacman -S kitty`
- Fedora/RHEL: `sudo yum install kitty`
- openSUSE: `sudo zypper install kitty`
- Nix: Available via Nix package manager

**Installer Options:**
- Nightly builds: Add `installer=nightly`
- Specific version: `installer=version-X.X.X`
- Custom location: `dest=/your/path`

## Features

### Rendering & Graphics
- **GPU Acceleration:** ✅ Yes (OpenGL exclusive)
  - All rendering via OpenGL (text, graphics, UI)
  - Threaded rendering for minimal latency
  - SIMD vector CPU instructions
- **Font Ligatures:** ✅ Full support with per-glyph substitution
- **Variable Fonts:** ✅ Yes with customizable font features
- **True Color (24-bit):** ✅ Full support

### Window Management
- **Tabs:** ✅ Programmable tabs
- **Splits/Panes:** ✅ Arbitrary horizontal and vertical splits
- **Layouts:** 7 types (Fat, Grid, Horizontal, Splits, Stack, Tall, Vertical)
- **Hierarchy:** OS windows → tabs → kitty windows in layouts

### Image Support
- **Status:** ✅ Yes (creator of Kitty Graphics Protocol)
- **Protocol:** Kitty Graphics Protocol (proprietary)
- **Formats:** 24-bit RGB, 32-bit RGBA, PNG
- **Compression:** RFC 1950 ZLIB deflate
- **Transfer:** Direct pixel data, file transmission, shared memory
- **Features:**
  - Images above/below text with alpha blending
  - Z-index control for layering
  - Images scroll with text
  - Animation support (client-driven and terminal-driven)
  - Frame composition with delta transmission
  - Unicode placeholder support

### Themes & Customization
- **Themes:** 300+ pre-built themes
- **Repository:** https://github.com/kovidgoyal/kitty-themes
- **Custom Themes:** ✅ Yes (`~/.config/kitty/themes/`)
- **Theme Management:**
  - Built-in themes kitten with interactive browsing
  - Live color previews
  - Search by name, filter by light/dark
  - Recent themes list
  - Automatic OS-aware theme switching

### Configuration
- **Format:** Text-based `kitty.conf`
- **Location:** `~/.config/kitty/kitty.conf`
- **Features:**
  - Comments (`#`)
  - Line continuation (`\`)
  - Include directives (`include`, `globinclude`, `envinclude`, `geninclude`)
  - Extensive keyboard/mouse customization
  - Performance tuning options
  - 256 terminal colors (color0-color255)

## Performance

### Latency (Keyboard-to-Screen)
- **macOS:** Comparable to Terminal.app (fastest category)
- **Linux:** "Far and away the best latency" (Typometer measurement)

### Throughput (Linux/X11, AMD Ryzen)
- **ASCII data:** 121.8 MB/s
- **Unicode data:** 105.0 MB/s
- **CSI sequences:** 59.8 MB/s
- **Images:** 251.6 MB/s
- **Average:** 134.55 MB/s
- **Comparison:** "Twice as fast as the next best"
  - GNOME Terminal: 61.83 MB/s
  - Alacritty: 54.05 MB/s
  - WezTerm: 48.5 MB/s

### CPU Usage (During Scrolling)
- **Kitty:** 6-8% (terminal + X11)
- **Comparison:**
  - xterm: Similar to Kitty
  - GNOME Terminal: 15-17%
  - Konsole: 29-31%

### Startup Time
- Within 100ms of other GPU terminals
- Occasional slow starts on multi-GPU Linux systems (power management)

## Unique Features

### Kitty Graphics Protocol
- **Innovation:** First-class terminal graphics protocol
- **Design:** Clients send pixel data; terminals don't parse image formats
- **Integration:** Seamless with text, z-index layering, alpha blending
- **Adoption:** Industry standard adopted by other terminals

### Advanced Terminal Protocols
- **Colored/styled underlines:** Curly underlines extending escape codes
- **Multiple cursor protocol:** Simultaneous cursor positioning
- **Desktop notifications:** With icons and buttons
- **Comprehensive keyboard handling:** Enhanced key reporting
- **File transfer protocol:** Over TTY with delta transmission
- **Mouse pointer control:** Terminal-controlled pointer shapes

### Shell Integration
- Prompt navigation between prompts
- Remote file editing over SSH
- Session save/restore
- Scrollback piping to commands
- Remote control over networks

### Extensibility
- **Kittens:** Python-based extensions/plugins
- **Remote control:** Scriptable API
- **Custom configurations:** Extensive via kitty.conf
- **Programmable windows:** Advanced window management scripting

### Other Features
- Interactive pager for browsing output
- Clickable hyperlinks with custom actions
- Startup session management
- Fine-grained ligature control

## Documentation

- Official Docs: https://sw.kovidgoyal.net/kitty/
- Performance: https://sw.kovidgoyal.net/kitty/performance/
- Configuration: https://sw.kovidgoyal.net/kitty/conf/
- Graphics Protocol: https://sw.kovidgoyal.net/kitty/graphics-protocol/
- Themes Kitten: https://sw.kovidgoyal.net/kitty/kittens/themes/

## Sources

All data collected from official sources:

- [Kitty Official Website](https://sw.kovidgoyal.net/kitty/) - Accessed 2026-01-14
- [Kitty Performance Page](https://sw.kovidgoyal.net/kitty/performance/) - Accessed 2026-01-14
- [Kitty GitHub Repository](https://github.com/kovidgoyal/kitty) - Accessed 2026-01-14
- [Kitty Configuration Docs](https://sw.kovidgoyal.net/kitty/conf/) - Accessed 2026-01-14
- [Kitty Graphics Protocol](https://sw.kovidgoyal.net/kitty/graphics-protocol/) - Accessed 2026-01-14
- [Kitty Installation Guide](https://sw.kovidgoyal.net/kitty/binary/) - Accessed 2026-01-14
- [Kitty Changelog](https://sw.kovidgoyal.net/kitty/changelog/) - Accessed 2026-01-14

[← Back to Comparison](../comparison.md)
