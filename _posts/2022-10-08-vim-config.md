---
title: Vim config
author: Ronny
date: 2022-10-08 17:36:00 +0700
categories: [Code, Blog]
tags: [vim, customize]
---

This is a collection of vim configs include keymaps, plugins, options.

Since I mainly use VscodeVim, keymapping related will be the main focus.

## Frequently use actions

---
🔢 - command accepts numeric prefix

- Capitalize an action will do it till EOL.
- Type the action 2 times like `dd` will do it for the whole line.
- ;{char}{char}: easymotion to find word include those 2 chars.

### General

| Command | Description              |
| ------- | ------------------------ |
| za      | Toggle fold              |
| %       | Jump to matching bracket |

### Text-object

| Command | Description     |
| ------- | --------------- |
| 🔢is   | inner sentence  |
| 🔢ip   | inner paragraph |

### Horizontal Movement

| Command    | Description                                  |
| ---------- | -------------------------------------------- |
| 🔢)       | N sentence forward                           |
| 🔢(       | N sentence backward                          |
| 🔢}       | N paragraph forward                          |
| 🔢{       | N paragraph backward                         |
| 🔢 [{     | N times back to unclosed '{'                 |
| 🔢 ])     | N times forward to unclosed ')'              |
| 🔢f{char} | to the Nth occurrence of {char} to the right |
| 🔢F{char} | to the Nth occurrence of {char} to the left  |

### Vertical Movement

| Command   | Description                                  |
| --------- | -------------------------------------------- |
| 🔢CTRL-U | window N lines Upwards (default: 1/2 window) |
| 🔢CTRL-V | Vertical line selection (multicursor)        |

### Editing

| Command    | Description                                               | Note                     |
| ---------- | --------------------------------------------------------- | ------------------------ |
| 🔢u       | undo last N changes                                       |                          |
| 🔢CTRL-R  | redo last N undone changes                                |                          |
| ci{        | Change inside '{}'                                        |                          |
| ca{        | Change around '{}'                                        |                          |
| g~{motion} | switch case for the text that is moved over with {motion} | can use u/U instead of ~ |
| {visual}~  | switch case for highlighted text                          | can use u/U instead of ~ |

## Custom Keymapping

---

## Options

---

## Plugins

---

### Theme

## Resource

---

- [VscodeVim Roadmap](https://github.com/VSCodeVim/Vim/blob/master/ROADMAP.md)
- [Vim tips wiki](https://vim.fandom.com/wiki/Vim_Tips_Wiki)
