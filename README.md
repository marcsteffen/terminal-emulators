# Terminal Emulators Comparison

Objective comparison sourced from official documentation.

Click column headers to sort.

## Quick Comparison

| Terminal | GPU | Ligatures | Tabs | Splits | True Color | Images | Platform |
|----------|-----|-----------|------|--------|------------|--------|----------|
| [Alacritty](terminals/alacritty.md) | [x] OpenGL | [ ] | [ ] | [ ] | [x] | [ ] | macOS, Linux, Windows, BSD |
| [Ghostty](terminals/ghostty.md) | [x] Metal/OpenGL | [x] | [x] | [x] | [x] | [x] Kitty | macOS, Linux |
| [GNOME Terminal](terminals/gnome-terminal.md) | [ ] | [x] | [x] | [ ] | [!] | [ ] | Linux |
| [Hyper](terminals/hyper.md) | [!] Electron | [x] | [x] | [x] | [x] | [ ] | macOS, Linux, Windows |
| [iTerm2](terminals/iterm2.md) | [x] Metal | [x] | [x] | [x] | [x] | [x] iTerm2 | macOS |
| [Kitty](terminals/kitty.md) | [x] OpenGL | [x] | [x] | [x] | [x] | [x] Kitty | macOS, Linux, BSD |
| [Konsole](terminals/konsole.md) | [ ] | [x] | [x] | [x] | [x] | [ ] | Linux, BSD |
| [Rio](terminals/rio.md) | [x] WebGPU | [x] | [x] | [x] | [x] | [x] Sixel | macOS, Linux, Windows |
| [Tabby](terminals/tabby.md) | [x] | [x] | [x] | [x] | [x] | [ ] | macOS, Linux, Windows |
| [Terminal.app](terminals/terminal-app.md) | [x] | [x] | [x] | [x] | [x] | [ ] | macOS |
| [Warp](terminals/warp.md) | [x] | [x] | [x] | [x] | [x] | [x] | macOS, Linux, Windows |
| [WezTerm](terminals/wezterm.md) | [x] WebGPU | [x] | [x] | [x] | [x] | [x] iTerm2 | macOS, Linux, Windows, BSD |
| [Windows Terminal](terminals/windows-terminal.md) | [x] | [x] | [x] | [x] | [x] | [x] Sixel | Windows |

## Full Comparison

### Features & Platform Support

| Terminal | GPU Accel | Ligatures | Tabs | Splits | True Color | Images | Protocol | macOS | Linux | Windows | BSD |
|----------|-----------|-----------|------|--------|------------|--------|----------|-------|-------|---------|-----|
| [Alacritty](terminals/alacritty.md) | [x] OpenGL | [ ] | [ ] | [ ] | [x] | [ ] | - | [x] | [x] | [x] | [x] |
| [Ghostty](terminals/ghostty.md) | [x] Metal/OpenGL | [x] | [x] | [x] | [x] | [x] | Kitty | [x] | [x] | [~] | [ ] |
| [GNOME Terminal](terminals/gnome-terminal.md) | [ ] | [x] | [x] | [ ] | [!] | [ ] | - | [ ] | [x] | [ ] | [ ] |
| [Hyper](terminals/hyper.md) | [!] Electron | [x] | [x] | [x] | [x] | [ ] | - | [x] | [x] | [x] | [ ] |
| [iTerm2](terminals/iterm2.md) | [x] Metal | [x] | [x] | [x] | [x] | [x] | iTerm2 | [x] | [ ] | [ ] | [ ] |
| [Kitty](terminals/kitty.md) | [x] OpenGL | [x] | [x] | [x] | [x] | [x] | Kitty | [x] | [x] | [ ] | [x] |
| [Konsole](terminals/konsole.md) | [ ] | [x] | [x] | [x] | [x] | [ ] | - | [ ] | [x] | [ ] | [x] |
| [Rio](terminals/rio.md) | [x] WebGPU | [x] | [x] | [x] | [x] | [x] | Sixel | [x] | [x] | [x] | [ ] |
| [Tabby](terminals/tabby.md) | [x] | [x] | [x] | [x] | [x] | [ ] | - | [x] | [x] | [x] | [ ] |
| [Terminal.app](terminals/terminal-app.md) | [x] | [x] | [x] | [x] | [x] | [ ] | - | [x] | [ ] | [ ] | [ ] |
| [Warp](terminals/warp.md) | [x] | [x] | [x] | [x] | [x] | [x] | - | [x] | [x] | [x] | [ ] |
| [WezTerm](terminals/wezterm.md) | [x] WebGPU | [x] | [x] | [x] | [x] | [x] | iTerm2 | [x] | [x] | [x] | [x] |
| [Windows Terminal](terminals/windows-terminal.md) | [x] | [x] | [x] | [x] | [x] | [x] | Sixel | [ ] | [ ] | [x] | [ ] |

### Performance

| Terminal | Startup | Memory (Idle) | Latency | Throughput | License |
|----------|---------|---------------|---------|------------|---------|
| [Alacritty](terminals/alacritty.md) | ~50ms | ~30MB | Very Low | Highest | Apache-2.0 / MIT |
| [Ghostty](terminals/ghostty.md) | <100ms | ~50MB | Low | High | MIT |
| [GNOME Terminal](terminals/gnome-terminal.md) | Moderate | Low | Moderate | Moderate | GPL-3.0 |
| [Hyper](terminals/hyper.md) | ~150ms+ | High | Moderate | Moderate | MIT |
| [iTerm2](terminals/iterm2.md) | Not spec | Higher | Moderate | Moderate | GPL-2.0 |
| [Kitty](terminals/kitty.md) | ~100ms | Not spec | Best (Linux) | 134.55 MB/s | GPL-3.0 |
| [Konsole](terminals/konsole.md) | Moderate | Moderate | Moderate | Moderate | GPL-2.0 |
| [Rio](terminals/rio.md) | Fast | Not spec | Low | Good | MIT |
| [Tabby](terminals/tabby.md) | Moderate | High | Moderate | Good | MIT |
| [Terminal.app](terminals/terminal-app.md) | Fast | Low | Low | Good | Proprietary |
| [Warp](terminals/warp.md) | Fast | Not spec | Low | Good | Proprietary |
| [WezTerm](terminals/wezterm.md) | ~150ms | ~80MB | Low | Good | MIT |
| [Windows Terminal](terminals/windows-terminal.md) | Fast | Moderate | Low | Good | MIT |

### Configuration

| Terminal | Format | Themes | Custom | Hot Reload |
|----------|--------|--------|--------|------------|
| [Alacritty](terminals/alacritty.md) | TOML | 234+ ext | [x] | [x] |
| [Ghostty](terminals/ghostty.md) | key=value | 100+ | [x] | [x] |
| [GNOME Terminal](terminals/gnome-terminal.md) | GUI | Built-in | [x] | [ ] |
| [Hyper](terminals/hyper.md) | JS | Many | [x] | [x] |
| [iTerm2](terminals/iterm2.md) | GUI/plist | Many | [x] | [x] |
| [Kitty](terminals/kitty.md) | kitty.conf | 300+ | [x] | [x] |
| [Konsole](terminals/konsole.md) | GUI | Many | [x] | [ ] |
| [Rio](terminals/rio.md) | TOML | Many | [x] | [x] |
| [Tabby](terminals/tabby.md) | GUI/YAML | Many | [x] | [x] |
| [Terminal.app](terminals/terminal-app.md) | GUI/plist | Built-in | [x] | [ ] |
| [Warp](terminals/warp.md) | GUI | Built-in | [x] | [x] |
| [WezTerm](terminals/wezterm.md) | Lua | Many | [x] | [x] |
| [Windows Terminal](terminals/windows-terminal.md) | JSON | Many | [x] | [x] |

### Development

| Terminal | Language | First Release | Latest | Stars | License |
|----------|----------|---------------|--------|-------|---------|
| [Alacritty](terminals/alacritty.md) | Rust | Jan 2017 | 0.16.1 | High | Apache-2.0 / MIT |
| [Ghostty](terminals/ghostty.md) | Zig | Dec 2024 | 1.2.3 | 41.4k | MIT |
| [GNOME Terminal](terminals/gnome-terminal.md) | C | 1999 | Active | N/A | GPL-3.0 |
| [Hyper](terminals/hyper.md) | JavaScript | 2016 | Active | 43k+ | MIT |
| [iTerm2](terminals/iterm2.md) | Objective-C | 2009 | Active | High | GPL-2.0 |
| [Kitty](terminals/kitty.md) | Python/C/Go | Oct 2017 | 0.45.0 | 30.7k | GPL-3.0 |
| [Konsole](terminals/konsole.md) | C++ | 1997 | Active | N/A | GPL-2.0 |
| [Rio](terminals/rio.md) | Rust | 2023 | 0.2.x | Active | MIT |
| [Tabby](terminals/tabby.md) | TypeScript | 2017 | Active | 61k+ | MIT |
| [Terminal.app](terminals/terminal-app.md) | Objective-C | 2001 | Active | N/A | Proprietary |
| [Warp](terminals/warp.md) | Rust | 2021 | Active | N/A | Proprietary |
| [WezTerm](terminals/wezterm.md) | Rust | 2018 | Active | High | MIT |
| [Windows Terminal](terminals/windows-terminal.md) | C++ | 2019 | Active | 95k+ | MIT |

### Unique Features

| Terminal | Differentiators |
|----------|-----------------|
| [Alacritty](terminals/alacritty.md) | Performance-first, minimal by design, created vtebench tool |
| [Ghostty](terminals/ghostty.md) | Native UI (SwiftUI/GTK4), libghostty architecture, Mitchell Hashimoto creation |
| [GNOME Terminal](terminals/gnome-terminal.md) | Default GNOME terminal, simple and reliable, VTE-based |
| [Hyper](terminals/hyper.md) | Electron-based, web technologies, highly extensible via plugins |
| [iTerm2](terminals/iterm2.md) | macOS native, most popular Mac terminal, extensive features |
| [Kitty](terminals/kitty.md) | Creator of Kitty Graphics Protocol, best latency on Linux, kittens (plugins) |
| [Konsole](terminals/konsole.md) | KDE integration, embedded in Kate/Dolphin, profiles system |
| [Rio](terminals/rio.md) | WebGPU rendering, browser support via WebAssembly, RetroArch shaders |
| [Tabby](terminals/tabby.md) | SSH/serial client, Zmodem support, connection manager |
| [Terminal.app](terminals/terminal-app.md) | macOS default, lightweight, solid basics |
| [Warp](terminals/warp.md) | AI-powered (Warp AI), modern block-based UI, team collaboration |
| [WezTerm](terminals/wezterm.md) | Multiplexer built-in, Lua scripting, cross-platform consistency |
| [Windows Terminal](terminals/windows-terminal.md) | Microsoft official, WSL integration, GPU text rendering |

---

**Legend:** [x] Yes | [ ] No | [~] Planned | [!] Partial

**Last updated:** 2026-01-14

**Note:** This comparison covers popular terminal emulators. Other terminals exist (xterm, urxvt, Terminator, st, Foot, Terminology, Tilix, etc.) but are not included.

## Sources

| Terminal | Official Documentation | Repository |
|----------|----------------------|------------|
| Alacritty | [alacritty.org](https://alacritty.org) | [github.com/alacritty/alacritty](https://github.com/alacritty/alacritty) |
| Ghostty | [ghostty.org/docs](https://ghostty.org/docs) | [github.com/ghostty-org/ghostty](https://github.com/ghostty-org/ghostty) |
| GNOME Terminal | [help.gnome.org](https://help.gnome.org/users/gnome-terminal/stable/) | [Wikipedia](https://en.wikipedia.org/wiki/GNOME_Terminal) |
| Hyper | [hyper.is](https://hyper.is) | [github.com/vercel/hyper](https://github.com/vercel/hyper) |
| iTerm2 | [iterm2.com](https://iterm2.com) | [github.com/gnachman/iTerm2](https://github.com/gnachman/iTerm2) |
| Kitty | [sw.kovidgoyal.net/kitty](https://sw.kovidgoyal.net/kitty/) | [github.com/kovidgoyal/kitty](https://github.com/kovidgoyal/kitty) |
| Konsole | [konsole.kde.org](https://konsole.kde.org) | [github.com/KDE/konsole](https://github.com/KDE/konsole) |
| Rio | [rioterm.com](https://rioterm.com) | [github.com/raphamorim/rio](https://github.com/raphamorim/rio) |
| Tabby | [tabby.sh](https://tabby.sh) | [github.com/Eugeny/tabby](https://github.com/Eugeny/tabby) |
| Terminal.app | [support.apple.com](https://support.apple.com/guide/terminal/) | [Wikipedia](https://en.wikipedia.org/wiki/Terminal_(macOS)) |
| Warp | [warp.dev](https://www.warp.dev) | [github.com/warpdotdev/Warp](https://github.com/warpdotdev/Warp) |
| WezTerm | [wezterm.org](https://wezterm.org) | [github.com/wezterm/wezterm](https://github.com/wezterm/wezterm) |
| Windows Terminal | [learn.microsoft.com](https://learn.microsoft.com/en-us/windows/terminal/) | [github.com/microsoft/terminal](https://github.com/microsoft/terminal) |

<script>
// Make tables sortable
document.addEventListener('DOMContentLoaded', function() {
  const tables = document.querySelectorAll('table');

  tables.forEach(table => {
    const headers = table.querySelectorAll('th');
    const tbody = table.querySelector('tbody');

    if (!tbody) return;

    headers.forEach((header, index) => {
      header.style.cursor = 'pointer';
      header.style.userSelect = 'none';

      header.addEventListener('click', () => {
        const rows = Array.from(tbody.querySelectorAll('tr'));
        const isAscending = header.classList.contains('sort-asc');

        // Remove sort classes from all headers
        headers.forEach(h => h.classList.remove('sort-asc', 'sort-desc'));

        // Sort rows
        rows.sort((a, b) => {
          const aCell = a.cells[index].textContent.trim();
          const bCell = b.cells[index].textContent.trim();

          // Try numeric sort first
          const aNum = parseFloat(aCell.replace(/[^\d.-]/g, ''));
          const bNum = parseFloat(bCell.replace(/[^\d.-]/g, ''));

          if (!isNaN(aNum) && !isNaN(bNum)) {
            return isAscending ? bNum - aNum : aNum - bNum;
          }

          // Fallback to string sort
          return isAscending
            ? bCell.localeCompare(aCell)
            : aCell.localeCompare(bCell);
        });

        // Update header class
        header.classList.add(isAscending ? 'sort-desc' : 'sort-asc');

        // Reorder rows
        rows.forEach(row => tbody.appendChild(row));
      });
    });
  });
});
</script>

<style>
th.sort-asc::after {
  content: ' ▲';
  font-size: 0.8em;
}

th.sort-desc::after {
  content: ' ▼';
  font-size: 0.8em;
}
</style>
