# Terminal Emulators Comparison

Objective comparison sourced from official documentation.

## Quick Comparison

| Terminal | GPU | Ligatures | Tabs | Splits | True Color | Images | Platform |
|----------|-----|-----------|------|--------|------------|--------|----------|
| [Ghostty](terminals/ghostty.md) | [x] Metal/OpenGL | [x] | [x] | [x] | [x] | [x] Kitty | macOS, Linux |
| [Alacritty](terminals/alacritty.md) | [x] OpenGL | [ ] | [ ] | [ ] | [x] | [ ] | All |
| [Kitty](terminals/kitty.md) | [x] OpenGL | [x] | [x] | [x] | [x] | [x] Kitty | macOS, Linux, BSD |
| [WezTerm](terminals/wezterm.md) | [x] WebGPU | [x] | [x] | [x] | [x] | [x] iTerm2 | All |
| [iTerm2](terminals/iterm2.md) | [x] Metal | [x] | [x] | [x] | [x] | [x] iTerm2 | macOS |
| [Warp](terminals/warp.md) | [x] | [x] | [x] | [x] | [x] | [x] | macOS, Linux, Windows |
| [Hyper](terminals/hyper.md) | [!] Electron | [x] | [x] | [x] | [x] | [ ] | All |
| [Rio](terminals/rio.md) | [x] WebGPU | [x] | [x] | [x] | [x] | [x] Sixel | All |
| [Windows Terminal](terminals/windows-terminal.md) | [x] | [x] | [x] | [x] | [x] | [x] Sixel | Windows |
| [GNOME Terminal](terminals/gnome-terminal.md) | [ ] | [x] | [x] | [ ] | [!] | [ ] | Linux |
| [Konsole](terminals/konsole.md) | [ ] | [x] | [x] | [x] | [x] | [ ] | Linux |
| [Terminal.app](terminals/terminal-app.md) | [x] | [x] | [x] | [x] | [x] | [ ] | macOS |
| [Tabby](terminals/tabby.md) | [x] | [x] | [x] | [x] | [x] | [ ] | All |

## Full Comparison

### Features & Platform Support

| Terminal | GPU Accel | Ligatures | Tabs | Splits | True Color | Images | Protocol | macOS | Linux | Windows | BSD |
|----------|-----------|-----------|------|--------|------------|--------|----------|-------|-------|---------|-----|
| Ghostty | [x] Metal/OpenGL | [x] | [x] | [x] | [x] | [x] | Kitty | [x] | [x] | [~] | [ ] |
| Alacritty | [x] OpenGL | [ ] | [ ] | [ ] | [x] | [ ] | - | [x] | [x] | [x] | [x] |
| Kitty | [x] OpenGL | [x] | [x] | [x] | [x] | [x] | Kitty | [x] | [x] | [ ] | [x] |
| WezTerm | [x] WebGPU | [x] | [x] | [x] | [x] | [x] | iTerm2 | [x] | [x] | [x] | [x] |
| iTerm2 | [x] Metal | [x] | [x] | [x] | [x] | [x] | iTerm2 | [x] | [ ] | [ ] | [ ] |
| Warp | [x] | [x] | [x] | [x] | [x] | [x] | - | [x] | [x] | [x] | [ ] |
| Hyper | [!] Electron | [x] | [x] | [x] | [x] | [ ] | - | [x] | [x] | [x] | [ ] |
| Rio | [x] WebGPU | [x] | [x] | [x] | [x] | [x] | Sixel | [x] | [x] | [x] | [ ] |
| Windows Terminal | [x] | [x] | [x] | [x] | [x] | [x] | Sixel | [ ] | [ ] | [x] | [ ] |
| GNOME Terminal | [ ] | [x] | [x] | [ ] | [!] | [ ] | - | [ ] | [x] | [ ] | [ ] |
| Konsole | [ ] | [x] | [x] | [x] | [x] | [ ] | - | [ ] | [x] | [ ] | [ ] |
| Terminal.app | [x] | [x] | [x] | [x] | [x] | [ ] | - | [x] | [ ] | [ ] | [ ] |
| Tabby | [x] | [x] | [x] | [x] | [x] | [ ] | - | [x] | [x] | [x] | [ ] |

### Performance

| Terminal | Startup | Memory (Idle) | Latency | Throughput | License |
|----------|---------|---------------|---------|------------|---------|
| Ghostty | <100ms | ~50MB | Low | High | MIT |
| Alacritty | ~50ms | ~30MB | Very Low | Highest | Apache-2.0 / MIT |
| Kitty | ~100ms | Not spec | Best (Linux) | 134.55 MB/s | GPL-3.0 |
| WezTerm | ~150ms | ~80MB | Low | Good | MIT |
| iTerm2 | Not spec | Higher | Moderate | Moderate | GPL-2.0 |
| Warp | Fast | Not spec | Low | Good | Proprietary |
| Hyper | ~150ms+ | High | Moderate | Moderate | MIT |
| Rio | Fast | Not spec | Low | Good | MIT |
| Windows Terminal | Fast | Moderate | Low | Good | MIT |
| GNOME Terminal | Moderate | Low | Moderate | Moderate | GPL-3.0 |
| Konsole | Moderate | Moderate | Moderate | Moderate | GPL-2.0 |
| Terminal.app | Fast | Low | Low | Good | Proprietary |
| Tabby | Moderate | High | Moderate | Good | MIT |

### Configuration

| Terminal | Format | Themes | Custom | Hot Reload |
|----------|--------|--------|--------|------------|
| Ghostty | key=value | 100+ | [x] | [x] |
| Alacritty | TOML | 234+ ext | [x] | [x] |
| Kitty | kitty.conf | 300+ | [x] | [x] |
| WezTerm | Lua | Many | [x] | [x] |
| iTerm2 | GUI/plist | Many | [x] | [x] |
| Warp | GUI | Built-in | [x] | [x] |
| Hyper | JS | Many | [x] | [x] |
| Rio | TOML | Many | [x] | [x] |
| Windows Terminal | JSON | Many | [x] | [x] |
| GNOME Terminal | GUI | Built-in | [x] | [ ] |
| Konsole | GUI | Many | [x] | [ ] |
| Terminal.app | GUI/plist | Built-in | [x] | [ ] |
| Tabby | GUI/YAML | Many | [x] | [x] |

### Development

| Terminal | Language | First Release | Latest | Stars | License |
|----------|----------|---------------|--------|-------|---------|
| Ghostty | Zig | Dec 2024 | 1.2.3 | 41.4k | MIT |
| Alacritty | Rust | Jan 2017 | 0.16.1 | High | Apache-2.0 / MIT |
| Kitty | Python/C/Go | Oct 2017 | 0.45.0 | 30.7k | GPL-3.0 |
| WezTerm | Rust | 2018 | Active | High | MIT |
| iTerm2 | Objective-C | 2009 | Active | High | GPL-2.0 |
| Warp | Rust | 2021 | Active | N/A | Proprietary |
| Hyper | JavaScript | 2016 | Active | 43k+ | MIT |
| Rio | Rust | 2023 | 0.2.x | Active | MIT |
| Windows Terminal | C++ | 2019 | Active | 95k+ | MIT |
| GNOME Terminal | C | 1999 | Active | N/A | GPL-3.0 |
| Konsole | C++ | 1997 | Active | N/A | GPL-2.0 |
| Terminal.app | Objective-C | 2001 | Active | N/A | Proprietary |
| Tabby | TypeScript | 2017 | Active | 61k+ | MIT |

### Unique Features

| Terminal | Differentiators |
|----------|-----------------|
| Ghostty | Native UI (SwiftUI/GTK4), libghostty architecture, Mitchell Hashimoto creation |
| Alacritty | Performance-first, minimal by design, created vtebench tool |
| Kitty | Creator of Kitty Graphics Protocol, best latency on Linux, kittens (plugins) |
| WezTerm | Multiplexer built-in, Lua scripting, cross-platform consistency |
| iTerm2 | macOS native, most popular Mac terminal, extensive features |
| Warp | AI-powered (Warp AI), modern block-based UI, team collaboration |
| Hyper | Electron-based, web technologies, highly extensible via plugins |
| Rio | WebGPU rendering, browser support via WebAssembly, RetroArch shaders |
| Windows Terminal | Microsoft official, WSL integration, GPU text rendering |
| GNOME Terminal | Default GNOME terminal, simple and reliable, VTE-based |
| Konsole | KDE integration, embedded in Kate/Dolphin, profiles system |
| Terminal.app | macOS default, lightweight, solid basics |
| Tabby | SSH/serial client, Zmodem support, connection manager |

---

Legend: [x] Yes/Full support | [ ] No/Not supported | [~] Planned/WIP | [!] Partial/Software

Last updated: 2026-01-14

## Sources

**Ghostty:** [Official Docs](https://ghostty.org/docs) | [GitHub](https://github.com/ghostty-org/ghostty)

**Alacritty:** [Website](https://alacritty.org) | [GitHub](https://github.com/alacritty/alacritty)

**Kitty:** [Official Docs](https://sw.kovidgoyal.net/kitty/) | [GitHub](https://github.com/kovidgoyal/kitty)

**WezTerm:** [Website](https://wezterm.org) | [GitHub](https://github.com/wezterm/wezterm)

**iTerm2:** [Website](https://iterm2.com) | [Features](https://iterm2.com/features.html) | [GitHub](https://github.com/gnachman/iTerm2)

**Warp:** [Website](https://www.warp.dev) | [GitHub](https://github.com/warpdotdev/Warp)

**Hyper:** [Website](https://hyper.is) | [GitHub](https://github.com/vercel/hyper)

**Rio:** [Website](https://rioterm.com) | [GitHub](https://github.com/raphamorim/rio)

**Windows Terminal:** [Docs](https://learn.microsoft.com/en-us/windows/terminal/) | [GitHub](https://github.com/microsoft/terminal)

**GNOME Terminal:** [Help](https://help.gnome.org/users/gnome-terminal/stable/) | [Wikipedia](https://en.wikipedia.org/wiki/GNOME_Terminal)

**Konsole:** [Website](https://konsole.kde.org) | [GitHub](https://github.com/KDE/konsole)

**Terminal.app:** [Support](https://support.apple.com/guide/terminal/) | [Wikipedia](https://en.wikipedia.org/wiki/Terminal_(macOS))

**Tabby:** [Website](https://tabby.sh) | [GitHub](https://github.com/Eugeny/tabby)
