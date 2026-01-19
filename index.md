---
layout: default
title: Open Source Terminal Emulators Comparison
---

# Open Source Terminal Emulators Comparison

Objective comparison of open source terminals sourced from official documentation.

Click column headers to sort.

<nav class="sticky-nav">
  <a href="#quick-comparison">Quick</a>
  <a href="#features-platform">Features</a>
  <a href="#advanced-features">Advanced</a>
  <a href="#performance">Performance</a>
  <a href="#configuration">Config</a>
  <a href="#development">Development</a>
  <a href="#sources">Sources</a>
  <button id="back-to-top" style="display: none;">↑ Top</button>
</nav>

<div class="search-container">
  <input type="text" id="terminal-search" placeholder="Search terminals (name, platform, feature)..." />
  <div class="filter-buttons">
    <button class="filter-btn active" data-platform="all">All</button>
    <button class="filter-btn" data-platform="macOS">macOS</button>
    <button class="filter-btn" data-platform="Linux">Linux</button>
    <button class="filter-btn" data-platform="Windows">Windows</button>
    <button class="filter-btn" data-platform="BSD">BSD</button>
  </div>
</div>

## Quick Comparison {#quick-comparison}

| Terminal | GPU | Ligatures | Tabs | Splits | True Color | Images | Platform |
|----------|-----|-----------|------|--------|------------|--------|----------|
| [Alacritty](https://github.com/alacritty/alacritty) | [x] OpenGL | [ ] | [ ] | [ ] | [x] | [ ] | macOS, Linux, Windows, BSD |
| [Foot](https://codeberg.org/dnkl/foot) | [ ] CPU | [x] | [ ] | [ ] | [x] | [x] Sixel | Linux (Wayland) |
| [Ghostty](https://ghostty.org) | [x] Metal/OpenGL | [x] | [x] | [x] | [x] | [x] Kitty | macOS, Linux |
| [GNOME Terminal](https://gitlab.gnome.org/GNOME/gnome-terminal) | [ ] | [x] | [x] | [ ] | [x] | [ ] | Linux |
| [Hyper](https://hyper.is) | [!] Electron | [x] | [x] | [x] | [x] | [ ] | macOS, Linux, Windows |
| [iTerm2](https://iterm2.com) | [x] Metal | [x] | [x] | [x] | [x] | [x] iTerm2 | macOS |
| [Kitty](https://sw.kovidgoyal.net/kitty/) | [x] OpenGL | [x] | [x] | [x] | [x] | [x] Kitty | macOS, Linux, BSD |
| [Konsole](https://konsole.kde.org) | [ ] | [x] | [x] | [x] | [x] | [ ] | Linux, BSD |
| [Rio](https://rioterm.com) | [x] WebGPU | [x] | [x] | [x] | [x] | [x] Sixel | macOS, Linux, Windows |
| [st](https://st.suckless.org) | [ ] | [x] | [ ] | [ ] | [x] | [ ] | Linux, BSD |
| [Tabby](https://tabby.sh) | [x] Electron | [x] | [x] | [x] | [x] | [ ] | macOS, Linux, Windows |
| [Terminator](https://gnome-terminator.org) | [ ] | [x] | [x] | [x] | [x] | [ ] | Linux |
| [Terminology](https://www.enlightenment.org/about-terminology.md) | [!] Optional | [x] | [x] | [x] | [x] | [x] Images/Video | Linux, BSD |
| [Tilix](https://gnunn1.github.io/tilix-web/) | [ ] | [x] | [x] | [x] | [x] | [ ] | Linux |
| [urxvt](http://software.schmorp.de/pkg/rxvt-unicode.html) | [ ] | [ ] | [ ] | [ ] | [x] | [ ] | Linux, BSD |
| [WezTerm](https://wezterm.org) | [x] WebGPU | [x] | [x] | [x] | [x] | [x] iTerm2 | macOS, Linux, Windows, BSD |
| [Windows Terminal](https://github.com/microsoft/terminal) | [x] | [x] | [x] | [x] | [x] | [x] Sixel | Windows |
| [xterm](https://invisible-island.net/xterm/) | [ ] | [ ] | [x] | [ ] | [x] | [ ] | Linux, BSD |

## Full Comparison

### Features & Platform Support {#features-platform}

| Terminal | GPU Accel | Ligatures | Tabs | Splits | True Color | Images | Protocol | macOS | Linux | Windows | BSD |
|----------|-----------|-----------|------|--------|------------|--------|----------|-------|-------|---------|-----|
| [Alacritty](https://github.com/alacritty/alacritty) | [x] OpenGL | [ ] | [ ] | [ ] | [x] | [ ] | - | [x] | [x] | [x] | [x] |
| [Foot](https://codeberg.org/dnkl/foot) | [ ] CPU | [x] | [ ] | [ ] | [x] | [x] | Sixel | [ ] | [x] | [ ] | [ ] |
| [Ghostty](https://ghostty.org) | [x] Metal/OpenGL | [x] | [x] | [x] | [x] | [x] | Kitty | [x] | [x] | [~] | [ ] |
| [GNOME Terminal](https://gitlab.gnome.org/GNOME/gnome-terminal) | [ ] | [x] | [x] | [ ] | [x] | [ ] | - | [ ] | [x] | [ ] | [ ] |
| [Hyper](https://hyper.is) | [!] Electron | [x] | [x] | [x] | [x] | [ ] | - | [x] | [x] | [x] | [ ] |
| [iTerm2](https://iterm2.com) | [x] Metal | [x] | [x] | [x] | [x] | [x] | iTerm2 | [x] | [ ] | [ ] | [ ] |
| [Kitty](https://sw.kovidgoyal.net/kitty/) | [x] OpenGL | [x] | [x] | [x] | [x] | [x] | Kitty | [x] | [x] | [ ] | [x] |
| [Konsole](https://konsole.kde.org) | [ ] | [x] | [x] | [x] | [x] | [ ] | - | [ ] | [x] | [ ] | [x] |
| [Rio](https://rioterm.com) | [x] WebGPU | [x] | [x] | [x] | [x] | [x] | Sixel | [x] | [x] | [x] | [ ] |
| [st](https://st.suckless.org) | [ ] | [x] | [ ] | [ ] | [x] | [ ] | - | [ ] | [x] | [ ] | [x] |
| [Tabby](https://tabby.sh) | [x] Electron | [x] | [x] | [x] | [x] | [ ] | - | [x] | [x] | [x] | [ ] |
| [Terminator](https://gnome-terminator.org) | [ ] | [x] | [x] | [x] | [x] | [ ] | - | [ ] | [x] | [ ] | [ ] |
| [Terminology](https://www.enlightenment.org/about-terminology.md) | [!] Optional | [x] | [x] | [x] | [x] | [x] | Images/Video | [ ] | [x] | [ ] | [x] |
| [Tilix](https://gnunn1.github.io/tilix-web/) | [ ] | [x] | [x] | [x] | [x] | [ ] | - | [ ] | [x] | [ ] | [ ] |
| [urxvt](http://software.schmorp.de/pkg/rxvt-unicode.html) | [ ] | [ ] | [ ] | [ ] | [x] | [ ] | - | [ ] | [x] | [ ] | [x] |
| [WezTerm](https://wezterm.org) | [x] WebGPU | [x] | [x] | [x] | [x] | [x] | iTerm2 | [x] | [x] | [x] | [x] |
| [Windows Terminal](https://github.com/microsoft/terminal) | [x] | [x] | [x] | [x] | [x] | [x] | Sixel | [ ] | [ ] | [x] | [ ] |
| [xterm](https://invisible-island.net/xterm/) | [ ] | [ ] | [x] | [ ] | [x] | [ ] | - | [ ] | [x] | [ ] | [x] |

### Advanced Features {#advanced-features}

| Terminal | Scrollback | Search | Multiplexer | Shell Integration | Hyperlinks | Session Restore | Privacy |
|----------|------------|--------|-------------|-------------------|------------|----------------|---------|
| [Alacritty](https://github.com/alacritty/alacritty) | Limited | [ ] | External | [ ] | [x] | [ ] | No telemetry |
| [Foot](https://codeberg.org/dnkl/foot) | Limited | [x] | External | [ ] | [x] | [ ] | No telemetry |
| [Ghostty](https://ghostty.org) | Unlimited | [x] | External | [x] | [x] | [ ] | No telemetry |
| [GNOME Terminal](https://gitlab.gnome.org/GNOME/gnome-terminal) | Limited | [x] | External | [ ] | [x] | [ ] | No telemetry |
| [Hyper](https://hyper.is) | Limited | [x] | External | [ ] | [x] | [ ] | No telemetry |
| [iTerm2](https://iterm2.com) | Unlimited | [x] | [ ] | [x] | [x] | [x] | Optional analytics |
| [Kitty](https://sw.kovidgoyal.net/kitty/) | Unlimited | [x] | External | [x] | [x] | [ ] | No telemetry |
| [Konsole](https://konsole.kde.org) | Unlimited | [x] | External | [ ] | [x] | [x] | No telemetry |
| [Rio](https://rioterm.com) | Limited | [ ] | External | [ ] | [x] | [ ] | No telemetry |
| [st](https://st.suckless.org) | Limited | [ ] | External | [ ] | [ ] | [ ] | No telemetry |
| [Tabby](https://tabby.sh) | Unlimited | [x] | External | [ ] | [x] | [x] | No telemetry |
| [Terminator](https://gnome-terminator.org) | Limited | [x] | External | [ ] | [x] | [ ] | No telemetry |
| [Terminology](https://www.enlightenment.org/about-terminology.md) | Unlimited | [x] | External | [ ] | [x] | [ ] | No telemetry |
| [Tilix](https://gnunn1.github.io/tilix-web/) | Limited | [x] | External | [ ] | [x] | [x] | No telemetry |
| [urxvt](http://software.schmorp.de/pkg/rxvt-unicode.html) | Limited | [ ] | External | [ ] | [ ] | [ ] | No telemetry |
| [WezTerm](https://wezterm.org) | Unlimited | [x] | [x] | [x] | [x] | [x] | No telemetry |
| [Windows Terminal](https://github.com/microsoft/terminal) | Limited | [x] | External | [ ] | [x] | [ ] | No telemetry |
| [xterm](https://invisible-island.net/xterm/) | Limited | [ ] | External | [ ] | [ ] | [ ] | No telemetry |

### Performance {#performance}

| Terminal | Startup | Memory (Idle) | Latency | Throughput | License |
|----------|---------|---------------|---------|------------|---------|
| [Alacritty](https://github.com/alacritty/alacritty) | ~50ms | ~30MB | Very Low | Highest | Apache-2.0 / MIT |
| [Foot](https://codeberg.org/dnkl/foot) | Very Fast | Very Low | Very Low | High | MIT |
| [Ghostty](https://ghostty.org) | <100ms | ~50MB | Low | High | MIT |
| [GNOME Terminal](https://gitlab.gnome.org/GNOME/gnome-terminal) | Moderate | Low | Moderate | Moderate | GPL-3.0 |
| [Hyper](https://hyper.is) | ~150ms+ | High | Moderate | Moderate | MIT |
| [iTerm2](https://iterm2.com) | Not spec | Higher | Moderate | Moderate | GPL-2.0 |
| [Kitty](https://sw.kovidgoyal.net/kitty/) | ~100ms | Not spec | Best (Linux) | 134.55 MB/s | GPL-3.0 |
| [Konsole](https://konsole.kde.org) | Moderate | Moderate | Moderate | Moderate | GPL-2.0 |
| [Rio](https://rioterm.com) | Fast | Not spec | Low | Good | MIT |
| [st](https://st.suckless.org) | Very Fast | Minimal | Very Low | High | MIT |
| [Tabby](https://tabby.sh) | Moderate | High | Moderate | Good | MIT |
| [Terminator](https://gnome-terminator.org) | Moderate | Moderate | Moderate | Moderate | GPL-2.0 |
| [Terminology](https://www.enlightenment.org/about-terminology.md) | Fast | Moderate | Low | Good | BSD-2-Clause |
| [Tilix](https://gnunn1.github.io/tilix-web/) | Moderate | Moderate | Moderate | Moderate | MPL-2.0 |
| [urxvt](http://software.schmorp.de/pkg/rxvt-unicode.html) | Very Fast | Very Low | Low | High | GPL-3.0 |
| [WezTerm](https://wezterm.org) | ~150ms | ~80MB | Low | Good | MIT |
| [Windows Terminal](https://github.com/microsoft/terminal) | Fast | Moderate | Low | Good | MIT |
| [xterm](https://invisible-island.net/xterm/) | Fast | Very Low | Very Low | Good | X11 (MIT-style) |

### Configuration {#configuration}

| Terminal | Format | Themes | Custom | Hot Reload |
|----------|--------|--------|--------|------------|
| [Alacritty](https://github.com/alacritty/alacritty) | TOML | 234+ ext | [x] | [x] |
| [Foot](https://codeberg.org/dnkl/foot) | INI | Minimal | [x] | [x] |
| [Ghostty](https://ghostty.org) | key=value | 100+ | [x] | [x] |
| [GNOME Terminal](https://gitlab.gnome.org/GNOME/gnome-terminal) | GUI | Built-in | [x] | [ ] |
| [Hyper](https://hyper.is) | JS | Many | [x] | [x] |
| [iTerm2](https://iterm2.com) | GUI/plist | Many | [x] | [x] |
| [Kitty](https://sw.kovidgoyal.net/kitty/) | kitty.conf | 300+ | [x] | [x] |
| [Konsole](https://konsole.kde.org) | GUI | Many | [x] | [ ] |
| [Rio](https://rioterm.com) | TOML | Many | [x] | [x] |
| [st](https://st.suckless.org) | C header | Patches | [x] | [ ] |
| [Tabby](https://tabby.sh) | GUI/YAML | Many | [x] | [x] |
| [Terminator](https://gnome-terminator.org) | Config file | Built-in | [x] | [ ] |
| [Terminology](https://www.enlightenment.org/about-terminology.md) | Config file | Built-in | [x] | [ ] |
| [Tilix](https://gnunn1.github.io/tilix-web/) | GUI/JSON | Built-in | [x] | [ ] |
| [urxvt](http://software.schmorp.de/pkg/rxvt-unicode.html) | .Xresources | External | [x] | [ ] |
| [WezTerm](https://wezterm.org) | Lua | Many | [x] | [x] |
| [Windows Terminal](https://github.com/microsoft/terminal) | JSON | Many | [x] | [x] |
| [xterm](https://invisible-island.net/xterm/) | .Xresources | Minimal | [x] | [ ] |

### Development {#development}

| Terminal | Language | First Release | Latest | Stars | License |
|----------|----------|---------------|--------|-------|---------|
| [Alacritty](https://github.com/alacritty/alacritty) | Rust | Jan 2017 | 0.16.1 | High | Apache-2.0 / MIT |
| [Foot](https://codeberg.org/dnkl/foot) | C | 2020 | Active | Moderate | MIT |
| [Ghostty](https://ghostty.org) | Zig | Dec 2024 | 1.2.3 | 41.4k | MIT |
| [GNOME Terminal](https://gitlab.gnome.org/GNOME/gnome-terminal) | C | 1999 | Active | N/A | GPL-3.0 |
| [Hyper](https://hyper.is) | JavaScript | 2016 | Active | 43k+ | MIT |
| [iTerm2](https://iterm2.com) | Objective-C | 2009 | Active | High | GPL-2.0 |
| [Kitty](https://sw.kovidgoyal.net/kitty/) | Python/C/Go | Oct 2017 | 0.45.0 | 30.7k | GPL-3.0 |
| [Konsole](https://konsole.kde.org) | C++ | 1997 | Active | N/A | GPL-2.0 |
| [Rio](https://rioterm.com) | Rust | 2023 | 0.2.x | Active | MIT |
| [st](https://st.suckless.org) | C | 2009 | Active | Moderate | MIT |
| [Tabby](https://tabby.sh) | TypeScript | 2017 | Active | 61k+ | MIT |
| [Terminator](https://gnome-terminator.org) | Python | 2007 | Active | Moderate | GPL-2.0 |
| [Terminology](https://www.enlightenment.org/about-terminology.md) | C (EFL) | 2012 | Active | Moderate | BSD-2-Clause |
| [Tilix](https://gnunn1.github.io/tilix-web/) | D | 2015 | Active | Moderate | MPL-2.0 |
| [urxvt](http://software.schmorp.de/pkg/rxvt-unicode.html) | C/Perl | 1997 | Low activity | N/A | GPL-3.0 |
| [WezTerm](https://wezterm.org) | Rust | 2018 | Active | High | MIT |
| [Windows Terminal](https://github.com/microsoft/terminal) | C++ | 2019 | Active | 95k+ | MIT |
| [xterm](https://invisible-island.net/xterm/) | C | 1984 | Active | N/A | X11 (MIT-style) |

### Unique Features

| Terminal | Differentiators |
|----------|-----------------|
| [Alacritty](https://github.com/alacritty/alacritty) | Performance-first, minimal by design, created vtebench tool |
| [Foot](https://codeberg.org/dnkl/foot) | Wayland-native, CPU rendering (no GPU), server/daemon mode, extremely lightweight |
| [Ghostty](https://ghostty.org) | Native UI (SwiftUI/GTK4), libghostty architecture, Mitchell Hashimoto creation |
| [GNOME Terminal](https://gitlab.gnome.org/GNOME/gnome-terminal) | Default GNOME terminal, simple and reliable, VTE-based |
| [Hyper](https://hyper.is) | Electron-based, web technologies, highly extensible via plugins |
| [iTerm2](https://iterm2.com) | macOS native, most popular Mac terminal, extensive features |
| [Kitty](https://sw.kovidgoyal.net/kitty/) | Creator of Kitty Graphics Protocol, best latency on Linux, kittens (plugins) |
| [Konsole](https://konsole.kde.org) | KDE integration, embedded in Kate/Dolphin, profiles system |
| [Rio](https://rioterm.com) | WebGPU rendering, browser support via WebAssembly, RetroArch shaders |
| [st](https://st.suckless.org) | Suckless philosophy, minimal code, configured via C source, extremely lightweight |
| [Tabby](https://tabby.sh) | SSH/serial client, Zmodem support, connection manager |
| [Terminator](https://gnome-terminator.org) | GTK-based, tiling/splitting focus, broadcast input to multiple panes |
| [Terminology](https://www.enlightenment.org/about-terminology.md) | EFL-based, media support (images/video/music), translucent background |
| [Tilix](https://gnunn1.github.io/tilix-web/) | GTK3 tiling, session management, Quake mode, drag-and-drop layouts |
| [urxvt](http://software.schmorp.de/pkg/rxvt-unicode.html) | Perl extensible, client/daemon model, extremely lightweight |
| [WezTerm](https://wezterm.org) | Multiplexer built-in, Lua scripting, cross-platform consistency |
| [Windows Terminal](https://github.com/microsoft/terminal) | Microsoft official, WSL integration, GPU text rendering |
| [xterm](https://invisible-island.net/xterm/) | Classic X11 terminal, VT420 emulation, highly configurable, battle-tested since 1984 |

---

**Legend:** [x] Yes | [ ] No | [~] Planned | [!] Partial

**Last updated:** 2026-01-14

**Coverage:** 18 open source terminal emulators compared across features, performance, configuration, and development.

## Sources {#sources}

| Terminal | Official Documentation | Repository |
|----------|----------------------|------------|
| Alacritty | [alacritty.org](https://alacritty.org) | [github.com/alacritty/alacritty](https://github.com/alacritty/alacritty) |
| Foot | [codeberg.org/dnkl/foot](https://codeberg.org/dnkl/foot) | [codeberg.org/dnkl/foot](https://codeberg.org/dnkl/foot) |
| Ghostty | [ghostty.org/docs](https://ghostty.org/docs) | [github.com/ghostty-org/ghostty](https://github.com/ghostty-org/ghostty) |
| GNOME Terminal | [help.gnome.org](https://help.gnome.org/users/gnome-terminal/stable/) | [gitlab.gnome.org/GNOME/gnome-terminal](https://gitlab.gnome.org/GNOME/gnome-terminal) |
| Hyper | [hyper.is](https://hyper.is) | [github.com/vercel/hyper](https://github.com/vercel/hyper) |
| iTerm2 | [iterm2.com](https://iterm2.com) | [github.com/gnachman/iTerm2](https://github.com/gnachman/iTerm2) |
| Kitty | [sw.kovidgoyal.net/kitty](https://sw.kovidgoyal.net/kitty/) | [github.com/kovidgoyal/kitty](https://github.com/kovidgoyal/kitty) |
| Konsole | [konsole.kde.org](https://konsole.kde.org) | [github.com/KDE/konsole](https://github.com/KDE/konsole) |
| Rio | [rioterm.com](https://rioterm.com) | [github.com/raphamorim/rio](https://github.com/raphamorim/rio) |
| st | [st.suckless.org](https://st.suckless.org) | [git.suckless.org/st](https://git.suckless.org/st) |
| Tabby | [tabby.sh](https://tabby.sh) | [github.com/Eugeny/tabby](https://github.com/Eugeny/tabby) |
| Terminator | [gnome-terminator.org](https://gnome-terminator.org) | [github.com/gnome-terminator/terminator](https://github.com/gnome-terminator/terminator) |
| Terminology | [enlightenment.org](https://www.enlightenment.org/about-terminology.md) | [github.com/borisfaure/terminology](https://github.com/borisfaure/terminology) |
| Tilix | [gnunn1.github.io/tilix-web](https://gnunn1.github.io/tilix-web/) | [github.com/gnunn1/tilix](https://github.com/gnunn1/tilix) |
| urxvt | [wiki.archlinux.org](https://wiki.archlinux.org/index.php/Rxvt-unicode) | [cvs.schmorp.de](http://cvs.schmorp.de/rxvt-unicode/) |
| WezTerm | [wezterm.org](https://wezterm.org) | [github.com/wezterm/wezterm](https://github.com/wezterm/wezterm) |
| Windows Terminal | [learn.microsoft.com](https://learn.microsoft.com/en-us/windows/terminal/) | [github.com/microsoft/terminal](https://github.com/microsoft/terminal) |
| xterm | [invisible-island.net/xterm](https://invisible-island.net/xterm/) | [invisible-island.net/xterm](https://invisible-island.net/xterm/xterm.html) |

<script>
// Make tables sortable with enhanced functionality
document.addEventListener('DOMContentLoaded', function() {
  const tables = document.querySelectorAll('table');

  // Restore sort from URL hash
  const hash = window.location.hash.substring(1);
  const [tableIndex, columnIndex, direction] = hash.split('-');

  tables.forEach((table, tIndex) => {
    const headers = table.querySelectorAll('th');
    const tbody = table.querySelector('tbody');

    if (!tbody) return;

    headers.forEach((header, hIndex) => {
      header.style.cursor = 'pointer';
      header.style.userSelect = 'none';

      // Restore sort if matches hash
      if (tIndex == tableIndex && hIndex == columnIndex) {
        header.classList.add(direction === 'asc' ? 'sort-asc' : 'sort-desc');
        header.style.backgroundColor = '#0a0a0a';
      }

      header.addEventListener('click', () => {
        const rows = Array.from(tbody.querySelectorAll('tr'));
        const isAscending = header.classList.contains('sort-asc');

        // Remove sort classes and highlighting from all headers
        headers.forEach(h => {
          h.classList.remove('sort-asc', 'sort-desc');
          h.style.backgroundColor = '#1a1a1a';
        });

        // Highlight current sort column
        header.style.backgroundColor = '#0a0a0a';

        // Sort rows with improved logic
        rows.sort((a, b) => {
          let aCell = a.cells[hIndex].textContent.trim();
          let bCell = b.cells[hIndex].textContent.trim();

          // Handle checkbox-style content
          const checkboxOrder = { '[x]': 3, '[!]': 2, '[~]': 1, '[ ]': 0 };
          const aCheck = checkboxOrder[aCell.substring(0, 3)];
          const bCheck = checkboxOrder[bCell.substring(0, 3)];

          if (aCheck !== undefined && bCheck !== undefined) {
            return isAscending ? bCheck - aCheck : aCheck - bCheck;
          }

          // Try numeric sort
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

        // Update header class and URL hash
        const newDirection = isAscending ? 'desc' : 'asc';
        header.classList.add(`sort-${newDirection}`);
        window.location.hash = `${tIndex}-${hIndex}-${newDirection}`;

        // Reorder rows
        rows.forEach(row => tbody.appendChild(row));
      });
    });
  });

  // Search and filter functionality
  const searchInput = document.getElementById('terminal-search');
  const filterButtons = document.querySelectorAll('.filter-btn');
  let currentPlatform = 'all';

  if (searchInput && filterButtons.length > 0) {
    searchInput.addEventListener('input', filterTerminals);
    filterButtons.forEach(btn => {
      btn.addEventListener('click', () => {
        currentPlatform = btn.dataset.platform;
        filterButtons.forEach(b => b.classList.remove('active'));
        btn.classList.add('active');
        filterTerminals();
      });
    });
  }

  function filterTerminals() {
    const searchTerm = searchInput.value.toLowerCase();
    const tables = document.querySelectorAll('table');

    tables.forEach(table => {
      const rows = table.querySelectorAll('tbody tr');
      rows.forEach(row => {
        const text = row.textContent.toLowerCase();
        const matchesSearch = text.includes(searchTerm);
        const matchesPlatform = currentPlatform === 'all' || text.includes(currentPlatform.toLowerCase());

        row.style.display = (matchesSearch && matchesPlatform) ? '' : 'none';
      });
    });
  }

  // Back to top button
  const backToTop = document.getElementById('back-to-top');
  if (backToTop) {
    window.addEventListener('scroll', () => {
      backToTop.style.display = window.scrollY > 300 ? 'block' : 'none';
    });
    backToTop.addEventListener('click', () => {
      window.scrollTo({ top: 0, behavior: 'smooth' });
    });
  }
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
