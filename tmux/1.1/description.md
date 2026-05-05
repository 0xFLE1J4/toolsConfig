## tmux Configuration

This `tmux` configuration is designed to provide a modern, efficient, and keyboard-driven terminal workflow inspired by tools like Zellij and Vim. It focuses on usability, speed, and visual clarity while maintaining a lightweight setup.

### Key Features

- **Custom Prefix Key (Alt + A)**  
  Replaces the default `Ctrl-b` with a more ergonomic and accessible keybinding.

- **Enhanced Navigation (Vim-like)**  
  Pane navigation and resizing are fully optimized with `hjkl` bindings, enabling fast and intuitive movement without leaving the keyboard.

- **Mouse Support Enabled**  
  Allows optional mouse interaction for resizing panes and switching windows.

- **Improved Indexing**  
  Windows and panes start at `1` instead of `0`, aligning with common user expectations.

- **Optimized Performance**  
  Increased history limit and reduced key delay for a smoother experience.

- **Zellij-Inspired Status Bar**  
  A visually clean and informative status bar:
  - Session name displayed on the left
  - Active/inactive windows clearly highlighted
  - Dynamic `tun0` IP address display (useful for VPN / pentesting environments)
  - Keybinding reminder for quick reference

- **Smart Pane Management**  
  - Split panes while preserving the current working directory  
  - Toggle fullscreen for focused work  
  - Quick pane closing

- **Quick Window Switching**  
  Direct access to windows using number keys (`1–9`).

- **Live Configuration Reload**  
  Reload your config instantly without restarting tmux.

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

#### 2. Apply the Configuration

Clone the repository and link the configuration file:

```bash
git clone https://github.com/0xFLE1J4//toolsConfig.git
cp toolsConfig/tmux/.tmux.conf ~/.tmux.conf
```

Or manually place the configuration in your home directory:

```bash
~/.tmux.conf
```

---

#### 3. Launch tmux

```bash
tmux
```

---

#### 4. Reload Configuration (Optional)

Inside tmux:

```
Alt + a, then r
```

---

### Usage Notes

- Prefix key: `Alt + a`
    
- Split panes:
    
    - Vertical → `Alt + a` then `v`
        
    - Horizontal → `Alt + a` then `b`
        
- Navigate panes: `Alt + a` then `h/j/k/l`
    
- Resize panes: `Alt + a` then `H/J/K/L`
    
- Toggle fullscreen: `Alt + a` then `f`
    

---

