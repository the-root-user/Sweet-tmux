# Sweet-tmux 🍭

An aesthetically crafted, modern, and productive configuration for [tmux](https://github.com/tmux/tmux) styled with Dracula++ pastel accents, rounded powerline glyphs, and intuitive keybindings.

---

## ✨ Features

- **Dracula++ Aesthetic**: Refined palette featuring deep blues, pastel highlights (lime, purple, cyan, green, yellow, orange, and red).
- **Smooth Pill Breadcrumbs**: Rounded powerline glyphs (`` / ``) creating clean visual segments for sessions, windows, host info, and status indicators.
- **Smart Window Naming**: Automatic contextual window naming via `tmux-window-name`.
- **System Monitoring**: Real-time CPU, RAM, battery metrics, and host details in the full configuration.
- **Browser-Style Shortcuts**: Work faster with familiar shortcut keys (`Ctrl+t` for new window, `Ctrl+w` to close, `Alt+1..9` to switch windows, `Ctrl+PageUp`/`PageDown` to cycle).
- **Productive Defaults**: Mouse support enabled, 24-bit true-color support, 1-based indexing for humans, aggressive resizing, and fast escape time (10ms).
- **Two Flavors Included**:
  - `Sweet-tmux.conf`: Full-featured edition with system metrics (CPU, RAM, battery, host).
  - `Sweet-tmux-simple.conf`: Lightweight edition with minimal dependencies and clock/status display.

---

## 📸 Preview

```text
  1    user㉿hostname            1  bash   2  editor             12%   󰒋 45%   󰁹 98%   󰔟 02:45 03 
```

---

## 📋 Prerequisites

1. **tmux** (version 3.0 or higher recommended).
2. **Nerd Font** installed and set in your terminal emulator (e.g., [JetBrainsMono Nerd Font](https://www.nerdfonts.com/), [FiraCode Nerd Font](https://www.nerdfonts.com/), or [Hack Nerd Font]) to render icons and rounded separators properly.
3. **Tmux Plugin Manager (TPM)** (optional but recommended for plugin support):
   ```bash
   git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm
   ```

---

## 🚀 Installation & Setup

### Option 1: Full Edition (`Sweet-tmux.conf`)

Includes CPU, memory, battery monitors, and window renaming plugins.

1. Backup any existing configuration:
   ```bash
   [ -f ~/.tmux.conf ] && mv ~/.tmux.conf ~/.tmux.conf.bak
   ```

2. Copy `Sweet-tmux.conf` to your home directory:
   ```bash
   cp Sweet-tmux.conf ~/.tmux.conf
   ```

3. Install plugins via TPM:
   - Start tmux: `tmux`
   - Press `Prefix + I` (default prefix is `Ctrl+b` or secondary `Ctrl+a`, then capital `I`) to fetch and install plugins.

### Option 2: Lightweight Edition (`Sweet-tmux-simple.conf`)

Minimal setup with essential styling and no heavy system monitoring dependencies.

1. Copy `Sweet-tmux-simple.conf` to your home directory:
   ```bash
   cp Sweet-tmux-simple.conf ~/.tmux.conf
   ```

2. Reload or launch tmux:
   ```bash
   tmux source ~/.tmux.conf
   ```

---

## ⌨️ Keybindings

### Prefix Keys
- Primary prefix: `Ctrl-b`
- Secondary prefix: `Ctrl-a`

### Direct Shortcuts (No Prefix Required)

| Keybinding | Action |
|------------|--------|
| `Ctrl + t` | New window (in current pane's directory) |
| `Ctrl + w` | Close pane (prompts if an active process is running) |
| `Ctrl + p` | Cycle to next pane |
| `Ctrl + PageDown` | Next window |
| `Ctrl + PageUp` | Previous window |
| `Ctrl + Down` | Split window vertically |
| `Ctrl + Right` | Split window horizontally |
| `Alt + 1` ... `Alt + 9` | Direct switch to window 1–9 |

### Window & Session Management (With Prefix)

| Keybinding | Action |
|------------|--------|
| `Prefix + c` | Create new window (retaining current path) |
| `Prefix + 0..9` | Select window 0–9 |
| `Prefix + r` | Rename current window |
| `Prefix + R` | Rename current session |
| `Prefix + Space` | Cycle through available layouts |
| `Prefix + C-e` | Open `~/.tmux.conf` in `$EDITOR` and reload on save |
| `Prefix + C-r` | Reload `~/.tmux.conf` |
| `Prefix + x` | Kill current pane |
| `Prefix + C-x` | Confirm & kill current window |
| `Prefix + C-q` | Confirm & kill current session |
| `Prefix + Q` | Confirm & kill entire tmux server |

### Pane Navigation & Resizing (With Prefix)

| Keybinding | Action |
|------------|--------|
| `Prefix + h` / `j` / `k` / `l` | Move focus Left / Down / Up / Right |
| `Prefix + H` / `J` / `K` / `L` | Resize pane Left / Down / Up / Right (by 2 cells, repeatable) |
| `Prefix + \|` | Split pane horizontally (current directory) |
| `Prefix + -` | Split pane vertically (current directory) |
| `Prefix + \` | Full-width vertical split |
| `Prefix + _` | Full-height horizontal split |
| `Prefix + >` / `<` | Swap active pane with next / previous pane |
| `Prefix + +` | Toggle pane zoom (`resize-pane -Z`) |

---

## 🛠️ Customization

Colors and symbols can easily be tailored near the `Themes and Appearance` section of the config files:

- **Colors**: Hex color variables (`c_fg`, `c_bg`, `c_hl`, `blue`, etc.) define the statusline and active pane colors.
- **Symbols**: Customize `symbol_left` and `symbol_right` (e.g., triangles `` / ``, slanted bars `` / ``, or subtle chevrons).
- **Date/Time format**: Toggle or format `$icon_datetime` and the date/time string inside the `status-right` option.

---

## 📄 License

This project is open-source under the MIT License. Feel free to customize and share!
