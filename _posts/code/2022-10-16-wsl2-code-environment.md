---
title: WSL2 Code Environment
author: Ronny
date: 2022-10-16 21:23:00 +0700
categories: [Code, Blog]
tags: [wsl2, customize, vim, tmux]
---

My WSL2 Code Environment that implements vim, tmux and ohmyzsh, in theory can be use with real Linux.

## WSL2

---

WSL2 setup is really straight forward, just follow microsoft [guide](https://learn.microsoft.com/en-us/windows/wsl/setup/environment).

### Installed

- zsh, ohmyzsh
- git and implement git-credential-manager from Windows.
- lazygit
- fzf

```bash
git config --global credential.helper "/mnt/c/Program\ Files/Git/mingw64/bin/git-credential-manager-core.exe"
```

## Vim

---

Look at my vim [blog]({% post_url code/2022-10-08-vim-config %}) for the configuration.

## Tmux

---

tmux is a terminal multiplexer, I have configure tmux keybind to has the same logic as vim and scripts that implement tmux.

### Requirements

- xclip or xsel for clipboard

### Plugins

| name                                                                          | description                                   |
| ----------------------------------------------------------------------------- | --------------------------------------------- |
| [tmux-plugins/tmux-resurrect](https://github.com/tmux-plugins/tmux-resurrect) | Restore tmux environment after system restart |

## TODO

- [ ] create auto install apps.
- [ ] Git-cred-manager [auto-installation](https://stackoverflow.com/questions/45925964/how-to-use-git-credential-store-on-wsl-ubuntu-on-windows).
