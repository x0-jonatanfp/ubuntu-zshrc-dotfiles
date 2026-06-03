<div align="center">

# Ubuntu .zshrc Dotfiles

[![MIT License](https://img.shields.io/badge/Licencia-MIT-green.svg)](LICENSE)
[![Ubuntu](https://img.shields.io/badge/Ubuntu-20.04%2B-orange)]()


[English](README.md)

**Configuración personalizada de `.zshrc` para Ubuntu con Oh My Posh y un gestor de alias propio para mejorar el flujo de trabajo en terminal.**

</div>

---

## Descripción

Este repositorio ofrece una configuración de `.zshrc` lista para producción para Ubuntu, construida sobre **Oh My Zsh** con el tema **Powerlevel10k**. Incluye una función única de gestión de alias llamada `aliash` que muestra todos los alias configurados agrupados por categoría, haciendo la navegación por terminal y la administración del sistema más rápidas y organizadas.

![Vista previa de la terminal](assets/example.png)

---

## Características

- **Prompt Powerlevel10k** — Rápido y personalizable con estado de git e información contextual
- **Gestor de alias aliash** — Función integrada que muestra alias agrupados por categoría (Fail2Ban, servicios, archivos, red y más)
- **Optimizado con plugins** — Incluye command-not-found, fzf, git, history-substring-search, sudo, tmux, zsh-autosuggestions y zsh-syntax-highlighting
- **Integración con lsd** — Listado moderno de directorios con iconos y orden por grupos
- **Accesos rápidos para Fail2Ban** — Comandos para ver estado y desbanear IPs
- **Alias para servicios del sistema** — Inicia y detiene servicios rápidamente
- **Mantenimiento del sistema** — Comandos de actualización, limpieza y purga simplificados

---

## Instalación rápida

### Requisitos

- Ubuntu 20.04+
- Zsh instalado (`sudo apt install zsh`)
- curl o wget

### Instalación

```bash
# 1. Instalar Oh My Zsh
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

# 2. Instalar tema Powerlevel10k
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k

# 3. Aplicar el .zshrc personalizado
curl -L https://raw.githubusercontent.com/x0-jonatanfp/ubuntu-zshrc-dotfiles/main/.zshrc -o ~/.zshrc

# 4. Recargar la terminal
source ~/.zshrc
```

### Usar aliash

Después de la instalación, ejecuta `aliash` en tu terminal para ver todos los alias disponibles organizados por grupo:

```bash
aliash
```

Esto mostrará una lista coloreada de todos los alias definidos con sus descripciones, agrupados por categoría (Fail2Ban, archivos, servicios, etc.).

---

## Personalización

### Plugins

Edita el array `plugins` en `.zshrc` para añadir o quitar plugins:

```zsh
plugins=(command-not-found fzf git history-substring-search sudo tmux zsh-autosuggestions zsh-syntax-highlighting)
```

### Grupos de alias

Los alias están organizados en secciones claramente marcadas dentro del archivo `.zshrc`. Cada grupo comienza con un comentario `# Group:`. Para añadir un nuevo alias, sigue el patrón existente:

```zsh
# Group: Mi Grupo
alias mi-alias='comando' # Descripción de lo que hace este alias
```

### Tema del prompt

El prompt de Powerlevel10k se puede configurar interactivamente:

```zsh
p10k configure
```

---

## Estructura del proyecto

```
ubuntu-zshrc-dotfiles/
├── .zshrc              # Archivo de configuración principal de Zsh
└── assets/
    └── example.png     # Captura de previsualización de la terminal
```
