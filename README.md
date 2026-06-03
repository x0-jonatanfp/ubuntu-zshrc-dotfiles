<div align="center">

# Ubuntu .zshrc Dotfiles

[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Ubuntu](https://img.shields.io/badge/Ubuntu-20.04%2B-orange)]()

**Custom .zshrc configuration for Ubuntu with Oh My Posh and a custom alias manager for an enhanced terminal workflow.**

</div>


---

<p align="center">🌐 <strong>Also available in:</strong> <a href="README.es.md">Spanish</a></p>

---
## Overview

This repository provides a production-ready `.zshrc` configuration for Ubuntu, built on **Oh My Zsh** with the **Powerlevel10k** theme. It includes a unique alias management function called `aliash` that displays all configured aliases grouped by category, making terminal navigation and system administration faster and more organized.

![Terminal Preview](assets/example.png)

---

## Features

- **Powerlevel10k prompt** — Fast, customizable prompt with git status and context-aware visuals
- **aliash alias manager** — Built-in function to display aliases grouped by category (Fail2Ban, system services, file management, networking, and more)
- **Plugin-optimized** — Includes command-not-found, fzf, git, history-substring-search, sudo, tmux, zsh-autosuggestions, and zsh-syntax-highlighting
- **lsd integration** — Modern directory listing with icons and group sorting
- **Fail2Ban shortcuts** — Quick alias commands for checking and unbanning IPs
- **System service aliases** — Quickly start and stop common services (SSH, web servers, databases)
- **System maintenance** — Update, clean, and purge commands streamlined

---

## Quick Start

### Prerequisites

- Ubuntu 20.04+
- Zsh installed (`sudo apt install zsh`)
- curl or wget

### Installation

```bash
# 1. Install Oh My Zsh
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

# 2. Install Powerlevel10k theme
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k

# 3. Apply the custom .zshrc
curl -L https://raw.githubusercontent.com/x0-jonatanfp/ubuntu-zshrc-dotfiles/main/.zshrc -o ~/.zshrc

# 4. Reload your terminal
source ~/.zshrc
```

### Using aliash

After installation, run `aliash` in your terminal to see all available aliases organized by group:

```bash
aliash
```

This will display a color-coded list of all defined aliases with their descriptions, grouped by category (Fail2Ban, file management, services, etc.).

---

## Customization

### Plugins

Edit the `plugins` array in `.zshrc` to add or remove plugins:

```zsh
plugins=(command-not-found fzf git history-substring-search sudo tmux zsh-autosuggestions zsh-syntax-highlighting)
```

### Alias Groups

Aliases are organized in clearly marked sections within the `.zshrc` file. Each group starts with a `# Group:` comment. To add a new alias, simply follow the existing pattern:

```zsh
# Group: My Group
alias my-alias='command' # Description of what this alias does
```

### Prompt Theme

The Powerlevel10k prompt can be configured interactively:

```zsh
p10k configure
```

---

## Project Structure

```
ubuntu-zshrc-dotfiles/
├── .zshrc              # Main Zsh configuration file
└── assets/
    └── example.png     # Terminal preview screenshot
```
