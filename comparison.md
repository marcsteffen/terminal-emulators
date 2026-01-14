# Full Terminal Emulator Comparison

Complete feature-by-feature comparison of modern terminal emulators.

## Features & Platform Support

| Terminal | GPU Accel | Ligatures | Tabs | Splits | True Color | Images | Protocol | macOS | Linux | Windows | BSD |
|----------|-----------|-----------|------|--------|------------|--------|----------|-------|-------|---------|-----|
| [Ghostty](terminals/ghostty.md) | ✅ Metal/OpenGL | ✅ | ✅ | ✅ | ✅ | ✅ | Kitty | ✅ | ✅ | 🚧 | ❌ |
| [Alacritty](terminals/alacritty.md) | ✅ OpenGL | ❌ | ❌ | ❌ | ✅ | ❌ | - | ✅ | ✅ | ✅ | ✅ |
| [Kitty](terminals/kitty.md) | ✅ OpenGL | ✅ | ✅ | ✅ | ✅ | ✅ | Kitty | ✅ | ✅ | ❌ | ✅ |

**Legend:** ✅ Full support | ⚠️ Partial/Software | ❌ Not supported | 🚧 In development

## Performance Comparison

| Terminal | Startup Time | Memory (Idle) | Input Latency | Throughput | License |
|----------|-------------|---------------|---------------|------------|---------|
| [Ghostty](terminals/ghostty.md) | <100ms (Linux: ~140ms) | ~50MB | Low (2ms scroll) | High | MIT |
| [Alacritty](terminals/alacritty.md) | ~50ms (fastest) | ~30MB | Very Low | Leads vtebench | Apache-2.0 / MIT |
| [Kitty](terminals/kitty.md) | ~100ms | Not specified | Best on Linux | 134.55 MB/s avg | GPL-3.0 |

## Configuration & Customization

| Terminal | Config Format | Themes Available | Custom Themes | Hot Reload |
|----------|--------------|------------------|---------------|------------|
| [Ghostty](terminals/ghostty.md) | Plain text (key=value) | 100+ | ✅ | ✅ |
| [Alacritty](terminals/alacritty.md) | TOML | 234+ external | ✅ | ✅ |
| [Kitty](terminals/kitty.md) | Text (kitty.conf) | 300+ | ✅ | ✅ |

## Installation Methods

| Terminal | Homebrew | Package Managers | Binary Installer | Build from Source |
|----------|----------|------------------|------------------|-------------------|
| [Ghostty](terminals/ghostty.md) | ✅ macOS | ✅ Many distros | ✅ | ✅ (Zig) |
| [Alacritty](terminals/alacritty.md) | ✅ macOS | ✅ All major distros | ✅ DMG/MSI | ✅ (Cargo/Rust) |
| [Kitty](terminals/kitty.md) | ✅ macOS | ✅ All major distros | ✅ curl script | ✅ (Python/C) |

## Development & Community

| Terminal | Language | First Release | Latest Version | GitHub Stars | Contributors |
|----------|----------|---------------|----------------|--------------|--------------|
| [Ghostty](terminals/ghostty.md) | Zig | Dec 2024 | 1.2.3 | 41.4k | 467+ |
| [Alacritty](terminals/alacritty.md) | Rust | Jan 2017 | 0.16.1 (beta) | Not specified | Active |
| [Kitty](terminals/kitty.md) | Python/C/Go | Oct 2017 | 0.45.0 | 30.7k | 373+ |

## Detailed Feature Breakdown

### GPU Acceleration Technologies
- **Ghostty:** Metal (macOS native), OpenGL (Linux)
- **Alacritty:** OpenGL/OpenGL ES (GLSL3 and GLES2 renderers)
- **Kitty:** OpenGL (exclusive rendering backend)

### Image Protocol Support
- **Ghostty:** Kitty graphics protocol (Sixel explicitly not supported)
- **Alacritty:** No image protocol support
- **Kitty:** Kitty graphics protocol (original creator, 24-bit RGB, 32-bit RGBA, PNG, animation support)

### Unique Differentiators

**Ghostty:**
- Platform-native UI (SwiftUI on macOS, GTK4 on Linux)
- Only terminal besides iTerm2 using Metal directly
- Libghostty architecture enables other terminals to use its engine
- Created by Mitchell Hashimoto (HashiCorp co-founder)

**Alacritty:**
- Performance-first design philosophy
- Composition over features (delegates tabs/splits to multiplexers)
- Created vtebench benchmarking tool
- Minimal feature set by design

**Kitty:**
- Creator of Kitty Graphics Protocol (now adopted by others)
- Advanced terminal protocols (colored underlines, multiple cursors, file transfer)
- Extensible via "kittens" (Python plugins)
- Best keyboard-to-screen latency on Linux
- Twice the throughput of competitors

## Sources

All data collected from official documentation:

**Ghostty:**
- [Official Documentation](https://ghostty.org/docs)
- [GitHub Repository](https://github.com/ghostty-org/ghostty)
- [Mitchell Hashimoto's Blog](https://mitchellh.com/writing)

**Alacritty:**
- [Official Website](https://alacritty.org)
- [GitHub Repository](https://github.com/alacritty/alacritty)
- [vtebench Tool](https://github.com/alacritty/vtebench)

**Kitty:**
- [Official Documentation](https://sw.kovidgoyal.net/kitty/)
- [Performance Page](https://sw.kovidgoyal.net/kitty/performance/)
- [GitHub Repository](https://github.com/kovidgoyal/kitty)

For detailed methodology, see [Methodology](methodology.md).

[← Back to Home](README.md)
