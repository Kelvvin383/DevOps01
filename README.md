# Dotfiles (WSL / Ubuntu)

This repository contains my shell configuration managed with **chezmoi**.

It allows me to quickly set up my working environment on a fresh Linux / WSL system.

---

## Requirements

Before applying these dotfiles, make sure the system has:

- `git`
- `zsh`
- `curl`

---

## Install chezmoi

Chezmoi is used to manage and deploy configuration files.

```bash
sh -c "$(curl -fsLS get.chezmoi.io)" -- -b ~/.local/bin
export PATH="$HOME/.local/bin:$PATH"
```

---

## 🚀 Setup dotfiles on a fresh system

```bash
chezmoi init https://github.com/Kelvin383/DevOps01.git
chezmoi apply -v
```

This will copy the configuration files into the correct locations in your home directory.

---

## Zsh Configuration

Zsh is used as the default shell along with **zinit** as the plugin manager.

### Installed Zsh Plugins

- **zsh-autosuggestions** - Suggests previously used commands to reduce typing
- **zsh-syntax-highlighting** - Highlights valid/invalid command syntax before execution
- **zsh-history-substring-search** - Allows searching command history by partial input
- **fzf-tab** - Provides interactive fuzzy tab-completion
- **git (Oh-My-Zsh plugin)** Adds shortcuts and completion for Git
- **docker (Oh-My-Zsh plugin)** Improves productivity when working with Docker

These plugins significantly improve command-line productivity by reducing typing, preventing errors, and speeding up navigation and command reuse.
