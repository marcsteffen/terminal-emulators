# Terminal Emulators Comparison

Objective comparison of terminal emulators sourced from official documentation.

## Quick Comparison

| Terminal | GPU Accel | Ligatures | Tabs | Splits | True Color | Images | Platform |
|----------|-----------|-----------|------|--------|------------|--------|----------|
| [Ghostty](terminals/ghostty.md) | ✅ Metal/OpenGL | ✅ | ✅ | ✅ | ✅ | ✅ Kitty | macOS, Linux |
| [Alacritty](terminals/alacritty.md) | ✅ OpenGL | ❌ | ❌ | ❌ | ✅ | ❌ | All |
| [Kitty](terminals/kitty.md) | ✅ OpenGL | ✅ | ✅ | ✅ | ✅ | ✅ Kitty | macOS, Linux, BSD |

## Full Comparison

### Features & Platform Support

| Terminal | GPU Accel | Ligatures | Tabs | Splits | True Color | Images | Protocol | macOS | Linux | Windows | BSD |
|----------|-----------|-----------|------|--------|------------|--------|----------|-------|-------|---------|-----|
| [Ghostty](terminals/ghostty.md) | ✅ Metal/OpenGL | ✅ | ✅ | ✅ | ✅ | ✅ | Kitty | ✅ | ✅ | 🚧 | ❌ |
| [Alacritty](terminals/alacritty.md) | ✅ OpenGL | ❌ | ❌ | ❌ | ✅ | ❌ | - | ✅ | ✅ | ✅ | ✅ |
| [Kitty](terminals/kitty.md) | ✅ OpenGL | ✅ | ✅ | ✅ | ✅ | ✅ | Kitty | ✅ | ✅ | ❌ | ✅ |

### Performance

| Terminal | Startup Time | Memory (Idle) | Input Latency | Throughput | License |
|----------|-------------|---------------|---------------|------------|---------|
| [Ghostty](terminals/ghostty.md) | <100ms (Linux: ~140ms) | ~50MB | Low (2ms scroll) | High | MIT |
| [Alacritty](terminals/alacritty.md) | ~50ms (fastest) | ~30MB | Very Low | Leads vtebench | Apache-2.0 / MIT |
| [Kitty](terminals/kitty.md) | ~100ms | Not specified | Best on Linux | 134.55 MB/s avg | GPL-3.0 |

### Configuration & Customization

| Terminal | Config Format | Themes Available | Custom Themes | Hot Reload |
|----------|--------------|------------------|---------------|------------|
| [Ghostty](terminals/ghostty.md) | Plain text (key=value) | 100+ | ✅ | ✅ |
| [Alacritty](terminals/alacritty.md) | TOML | 234+ external | ✅ | ✅ |
| [Kitty](terminals/kitty.md) | Text (kitty.conf) | 300+ | ✅ | ✅ |

### Installation

| Terminal | Homebrew | Package Managers | Binary Installer | Build from Source |
|----------|----------|------------------|------------------|-------------------|
| [Ghostty](terminals/ghostty.md) | ✅ macOS | ✅ Many distros | ✅ | ✅ (Zig) |
| [Alacritty](terminals/alacritty.md) | ✅ macOS | ✅ All major distros | ✅ DMG/MSI | ✅ (Cargo/Rust) |
| [Kitty](terminals/kitty.md) | ✅ macOS | ✅ All major distros | ✅ curl script | ✅ (Python/C) |

### Development & Community

| Terminal | Language | First Release | Latest Version | GitHub Stars | Contributors |
|----------|----------|---------------|----------------|--------------|--------------|
| [Ghostty](terminals/ghostty.md) | Zig | Dec 2024 | 1.2.3 | 41.4k | 467+ |
| [Alacritty](terminals/alacritty.md) | Rust | Jan 2017 | 0.16.1 (beta) | Not specified | Active |
| [Kitty](terminals/kitty.md) | Python/C/Go | Oct 2017 | 0.45.0 | 30.7k | 373+ |

---

**Legend:** ✅ Full support | ⚠️ Partial | ❌ Not supported | 🚧 In development

**Last updated:** 2026-01-14
