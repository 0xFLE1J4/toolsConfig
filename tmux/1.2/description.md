# tmux Configuration

This `tmux` configuration is designed to provide a modern, efficient, and keyboard-driven terminal workflow inspired by tools like Zellij and Vim. Built around a Catppuccin Mocha theme, it focuses on usability, speed, and visual clarity — with a particular emphasis on pentesting and CTF environments.

---

### Key Features

- **Custom Prefix Key (`Alt + a`)**
  Replaces the default `Ctrl-b` with a more ergonomic and accessible keybinding, reducing hand strain during long sessions.

- **Vim-like Navigation & Resizing**
  Pane navigation and resizing are fully optimized with `hjkl` bindings. `Alt + Arrow` keys also allow prefix-free pane switching for even faster movement.

- **Clipboard Integration (Wayland)**
  Copy mode uses `vi` keybindings with native `wl-copy` integration. Yanking with `y` copies to the system clipboard while staying at the current scroll position — no jarring jump back to the prompt.

- **Mouse Support**
  Optional mouse interaction for resizing panes and switching windows, without sacrificing keyboard-first ergonomics.

- **Smart Pane Splitting**
  Vertical and horizontal splits always inherit the current working directory, so you never need to `cd` again after opening a new pane.

- **Scratchpad Popups**
  Floating popup windows for quick access to a shell, `htop`, and CTF notes — all without cluttering your window layout.

- **Catppuccin Mocha Status Bar**
  A visually clean and informative status bar positioned at the top:
  - Session name on the left with a distinct accent
  - Active and inactive windows clearly differentiated
  - Dynamic `tun0` IP display with `Offline` fallback — ideal for VPN and pentesting
  - Prefix key reminder always visible on the right

- **Panel Synchronization**
  Broadcast keystrokes to all panes simultaneously with a single toggle — useful for running parallel commands across multiple targets.

- **Plugin Support via TPM**
  - `tmux-resurrect` — save and restore sessions across reboots
  - `tmux-continuum` — automatic session persistence
  - `extrakto` — fuzzy-extract text from the terminal output directly

- **Live Configuration Reload**
  Apply changes instantly without restarting tmux.

---

### Installation

#### 1. Install tmux

**Debian / Ubuntu**
```bash
sudo apt update && sudo apt install tmux -y
```

**Arch Linux**
```bash
sudo pacman -S tmux
```

**Fedora**
```bash
sudo dnf install tmux
```

---

#### 2. Install TPM (Plugin Manager)

```bash
git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm
```

---

#### 3. Install `wl-copy` (Wayland clipboard)

**Debian / Ubuntu**
```bash
sudo apt install wl-clipboard -y
```

**Arch Linux**
```bash
sudo pacman -S wl-clipboard
```

---

#### 4. Apply the Configuration

```bash
git clone https://github.com/unsafeOxOggy/toolsConfig.git
cp .tmux.conf ~/.tmux.conf
```

Or place the file manually at `~/.tmux.conf`.

---

#### 5. Launch tmux & Install Plugins

```bash
tmux
```

Then inside tmux, press `Alt + a` then `I` (capital i) to install plugins via TPM.

---

### Keybinding Reference

| Action | Keybinding |
|---|---|
| Prefix | `Alt + a` |
| Split vertical | `Prefix + v` |
| Split horizontal | `Prefix + b` |
| Navigate panes | `Prefix + h/j/k/l` |
| Navigate panes (fast) | `Alt + Arrow` |
| Resize panes | `Prefix + H/J/K/L` |
| Toggle fullscreen | `Prefix + f` |
| Close pane | `Prefix + x` |
| Quick shell popup | `Prefix + w` |
| System monitor popup | `Prefix + g` |
| CTF notes popup | `Prefix + n` |
| Sync panes toggle | `Prefix + =` |
| Reload config | `Prefix + r` |
| Enter copy mode | `Prefix + [` |
| Begin selection | `v` |
| Yank to clipboard | `y` |
| Extract text (extrakto) | `Prefix + Tab` |


### preview
<img width="1896" height="1027" alt="image" src="https://github.com/user-attachments/assets/d4a59acb-8c20-40eb-9a6f-afc3a3e3516f" />
