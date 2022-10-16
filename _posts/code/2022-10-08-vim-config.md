---
title: Vim Config
author: Ronny
date: 2022-10-08 17:36:00 +0700
categories: [Code, Blog]
tags: [vim, customize]
---

This is a collection of vim configs include keymaps, plugins, options.

Since I mainly use VscodeVim, keymapping related will be the main focus.

## Frequently used actions

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

### Core

| name                                                                                                          | description                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [wbthomason/packer.nvim](https://github.com/wbthomason/packer.nvim)                                           | A use-package inspired plugin manager for Neovim. Uses native packages, supports Luarocks dependencies, written in Lua, allows for expressive config           |
| [nvim-lua/plenary.nvim](https://github.com/nvim-lua/plenary.nvim)                                             | plenary: full; complete; entire; absolute; unqualified. All the lua functions I don't want to write twice.                                                     |
| [kyazdani42/nvim-web-devicons](https://github.com/kyazdani42/nvim-web-devicons)                               | lua `fork` of vim-web-devicons for neovim                                                                                                                      |
| [nvim-telescope/telescope.nvim](https://github.com/nvim-telescope/telescope.nvim)                             | Find, Filter, Preview, Pick. All lua, all the time.                                                                                                            |
| [lewis6991/gitsigns.nvim](https://github.com/lewis6991/gitsigns.nvim)                                         | Git integration for buffers                                                                                                                                    |
| [nvim-treesitter/nvim-treesitter](https://github.com/nvim-treesitter/nvim-treesitter)                         | Nvim Treesitter configurations and abstraction layer                                                                                                           |
| [akinsho/bufferline.nvim](https://github.com/akinsho/bufferline.nvim)                                         | A snazzy bufferline for Neovim                                                                                                                                 |
| [hrsh7th/nvim-cmp](https://github.com/hrsh7th/nvim-cmp)                                                       | A completion plugin for neovim coded in Lua.                                                                                                                   |
| [hrsh7th/cmp-path](https://github.com/hrsh7th/cmp-path)                                                       | nvim-cmp source for path                                                                                                                                       |
| [kyazdani42/nvim-tree.lua](https://github.com/kyazdani42/nvim-tree.lua)                                       | A file explorer tree for neovim written in lua                                                                                                                 |
| [numToStr/Comment.nvim](https://github.com/numToStr/Comment.nvim)                                             | :brain: :muscle: // Smart and powerful comment plugin for neovim. Supports treesitter, dot repeat, left-right/up-down motions, hooks, and more                 |
| [JoosepAlviste/nvim-ts-context-commentstring](https://github.com/JoosepAlviste/nvim-ts-context-commentstring) | Neovim treesitter plugin for setting the commentstring based on the cursor location in a file.                                                                 |
| [L3MON4D3/LuaSnip](https://github.com/L3MON4D3/LuaSnip)                                                       | Snippet Engine for Neovim written in Lua.                                                                                                                      |
| [saadparwaiz1/cmp_luasnip](https://github.com/saadparwaiz1/cmp_luasnip)                                       | luasnip completion source for nvim-cmp                                                                                                                         |
| [hrsh7th/cmp-buffer](https://github.com/hrsh7th/cmp-buffer)                                                   | nvim-cmp source for buffer words                                                                                                                               |
| [antoinemadec/FixCursorHold.nvim](https://github.com/antoinemadec/FixCursorHold.nvim)                         | Fix CursorHold Performance.                                                                                                                                    |
| [jose-elias-alvarez/null-ls.nvim](https://github.com/jose-elias-alvarez/null-ls.nvim)                         | Use Neovim as a language server to inject LSP diagnostics, code actions, and more via Lua.                                                                     |
| [williamboman/nvim-lsp-installer](https://github.com/williamboman/nvim-lsp-installer)                         | Neovim plugin that allows you to seamlessly manage LSP servers with :LspInstall. With full Windows support!                                                    |
| [neovim/nvim-lspconfig](https://github.com/neovim/nvim-lspconfig)                                             | Quickstart configurations for the Nvim LSP client                                                                                                              |
| [rafamadriz/friendly-snippets](https://github.com/rafamadriz/friendly-snippets)                               | Set of preconfigured snippets for different languages.                                                                                                         |
| [hrsh7th/cmp-nvim-lsp](https://github.com/hrsh7th/cmp-nvim-lsp)                                               | nvim-cmp source for neovim builtin LSP client                                                                                                                  |
| [nvim-lualine/lualine.nvim](https://github.com/nvim-lualine/lualine.nvim)                                     | A blazing fast and easy to configure neovim statusline plugin written in pure lua.                                                                             |
| [nvim-telescope/telescope-fzf-native.nvim](https://github.com/nvim-telescope/telescope-fzf-native.nvim)       | FZF sorter for telescope written in c                                                                                                                          |
| [lukas-reineke/indent-blankline.nvim](https://github.com/lukas-reineke/indent-blankline.nvim)                 | Indent guides for Neovim                                                                                                                                       |
| [Pocco81/DAPInstall.nvim](https://github.com/Pocco81/DAPInstall.nvim)                                         | 🦆 A NeoVim plugin for managing several debuggers for Nvim-dap                                                                                                |
| [akinsho/toggleterm.nvim](https://github.com/akinsho/toggleterm.nvim)                                         | A neovim lua plugin to help easily manage multiple terminal windows                                                                                            |
| [mfussenegger/nvim-dap](https://github.com/mfussenegger/nvim-dap)                                             | Debug Adapter Protocol client implementation for Neovim (>= 0.5)                                                                                               |

### Extra Plugins

Every plugin that works with Neovim works with LunarVim, here are some examples to get you started.

### Navigation plugins

#### [hop](https://github.com/phaazon/hop.nvim)

**neovim motions on speed!**

```lua
{
  "phaazon/hop.nvim",
  event = "BufRead",
  config = function()
    require("hop").setup()
    vim.api.nvim_set_keymap("n", "s", ":HopChar2<cr>", { silent = true })
    vim.api.nvim_set_keymap("n", "S", ":HopWord<cr>", { silent = true })
  end,
},
```

#### [lightspeed](https://github.com/ggandor/lightspeed.nvim)

**jetpack codebase navigation**

```lua
{
  "ggandor/lightspeed.nvim",
  event = "BufRead",
},
```

#### [minimap](https://github.com/wfxr/minimap.vim)

**blazing fast minimap/scrollbar written in Rust**

```lua
{
  'wfxr/minimap.vim',
  run = "cargo install --locked code-minimap",
  -- cmd = {"Minimap", "MinimapClose", "MinimapToggle", "MinimapRefresh", "MinimapUpdateHighlight"},
  config = function ()
    vim.cmd ("let g:minimap_width = 10")
    vim.cmd ("let g:minimap_auto_start = 1")
    vim.cmd ("let g:minimap_auto_start_win_enter = 1")
  end,
},
```

#### [numb](https://github.com/nacro90/numb.nvim)

**jump to the line**

```lua
{
  "nacro90/numb.nvim",
  event = "BufRead",
  config = function()
  require("numb").setup {
    show_numbers = true, -- Enable 'number' for the window while peeking
    show_cursorline = true, -- Enable 'cursorline' for the window while peeking
  }
  end,
},
```

#### [nvim-bqf](https://github.com/kevinhwang91/nvim-bqf)

**better quickfix window**

```lua
{
  "kevinhwang91/nvim-bqf",
  event = { "BufRead", "BufNew" },
  config = function()
  require("bqf").setup({
          auto_enable = true,
          preview = {
          win_height = 12,
          win_vheight = 12,
          delay_syntax = 80,
          border_chars = { "┃", "┃", "━", "━", "┏", "┓", "┗", "┛", "█" },
          },
          func_map = {
          vsplit = "",
          ptogglemode = "z,",
          stoggleup = "",
          },
          filter = {
          fzf = {
          action_for = { ["ctrl-s"] = "split" },
          extra_opts = { "--bind", "ctrl-o:toggle-all", "--prompt", "> " },
          },
          },
          })
  end,
},
```

#### [nvim-spectre](https://github.com/windwp/nvim-spectre)

**search and replace**

```lua
{
  "windwp/nvim-spectre",
  event = "BufRead",
  config = function()
    require("spectre").setup()
  end,
},
```

### Git

#### [git-blame](https://github.com/f-person/git-blame.nvim)

**show git blame**

```lua
{
  "f-person/git-blame.nvim",
  event = "BufRead",
  config = function()
    vim.cmd "highlight default link gitblame SpecialComment"
    vim.g.gitblame_enabled = 0
  end,
},
```

### Treesitter

#### [nvim-ts-autotag](https://github.com/windwp/nvim-ts-autotag)

**autoclose and autorename html tag**

```lua
{
  "windwp/nvim-ts-autotag",
  config = function()
    require("nvim-ts-autotag").setup()
  end,
},
```

#### [nvim-ts-rainbow](https://github.com/p00f/nvim-ts-rainbow)

**rainbow parentheses**

```lua
{
  "p00f/nvim-ts-rainbow",
},
```

After installing ensure to enable it in your `config.lua` using:

```
...
lvim.builtin.treesitter.rainbow.enable = true
...
```

#### [nvim-treesitter-context](https://github.com/romgrk/nvim-treesitter-context)

**Show current function at the top of the screen when function does not fit in screen**

```lua
{
    "romgrk/nvim-treesitter-context",
    config = function()
      require("treesitter-context").setup{
        enable = true, -- Enable this plugin (Can be enabled/disabled later via commands)
        throttle = true, -- Throttles plugin updates (may improve performance)
        max_lines = 0, -- How many lines the window should span. Values <= 0 mean no limit.
        patterns = { -- Match patterns for TS nodes. These get wrapped to match at word boundaries.
          -- For all filetypes
          -- Note that setting an entry here replaces all other patterns for this entry.
          -- By setting the 'default' entry below, you can control which nodes you want to
          -- appear in the context window.
          default = {
            'class',
            'function',
            'method',
          },
        },
      }
    end
  },
```

### Telescope Extensions

#### [telescope-fzf-native.nvim](https://github.com/nvim-telescope/telescope-fzy-native.nvim)

**fzy style sorter that is compiled**

```lua
{
  "nvim-telescope/telescope-fzy-native.nvim",
  run = "make",
  event = "BufRead",
},
```

### Colorschemes

#### [lsp-colors](https://github.com/folke/lsp-colors.nvim)

**lsp diagnostics highlight groups for non lsp colorschemes**

```lua
{
  "folke/lsp-colors.nvim",
  event = "BufRead",
},
```

#### [nvim-colorizer](https://github.com/norcalli/nvim-colorizer.lua)

**color highlighter**

```lua
{
  "norcalli/nvim-colorizer.lua",
    config = function()
      require("colorizer").setup({ "css", "scss", "html", "javascript" }, {
          RGB = true, -- #RGB hex codes
          RRGGBB = true, -- #RRGGBB hex codes
          RRGGBBAA = true, -- #RRGGBBAA hex codes
          rgb_fn = true, -- CSS rgb() and rgba() functions
          hsl_fn = true, -- CSS hsl() and hsla() functions
          css = true, -- Enable all CSS features: rgb_fn, hsl_fn, names, RGB, RRGGBB
          css_fn = true, -- Enable all CSS *functions*: rgb_fn, hsl_fn
          })
  end,
},
```

### LSP Enhancement

#### [cmp-tabnine](https://github.com/tzachar/cmp-tabnine)

**TabNine completion engine for hrsh7th/nvim-cmp**

```lua
{
  "tzachar/cmp-tabnine",
  run = "./install.sh",
  requires = "hrsh7th/nvim-cmp",
  event = "InsertEnter",
},
```

#### [lsp_signature.nvim](https://github.com/ray-x/lsp_signature.nvim)

**hint when you type**

```lua
{
  "ray-x/lsp_signature.nvim",
  event = "BufRead",
  config = function() require"lsp_signature".on_attach() end,
},
```

#### [symbols-outline.nvim](https://github.com/simrat39/symbols-outline.nvim)

**a tree like view for symbols**

```lua
{
  "simrat39/symbols-outline.nvim",
  config = function()
    require('symbols-outline').setup()
  end
},
```

#### [trouble.nvim](https://github.com/folke/trouble.nvim)

**diagnostics, references, telescope results, quickfix and location lists**

```lua
{
  "folke/trouble.nvim",
    cmd = "TroubleToggle",
},
```

Also define keybindings in `config.lua`

```lua
lvim.builtin.which_key.mappings["t"] = {
  name = "Diagnostics",
  t = { "<cmd>TroubleToggle<cr>", "trouble" },
  w = { "<cmd>TroubleToggle workspace_diagnostics<cr>", "workspace" },
  d = { "<cmd>TroubleToggle document_diagnostics<cr>", "document" },
  q = { "<cmd>TroubleToggle quickfix<cr>", "quickfix" },
  l = { "<cmd>TroubleToggle loclist<cr>", "loclist" },
  r = { "<cmd>TroubleToggle lsp_references<cr>", "references" },
},
```

### General

#### [dial.nvim](https://github.com/monaqa/dial.nvim)

**extended incrementing/decrementing**

```lua
{
  "monaqa/dial.nvim",
  event = "BufRead",
  config = function()
    local dial = require "dial"
    vim.cmd [[
    nmap <C-a> <Plug>(dial-increment)
      nmap <C-x> <Plug>(dial-decrement)
      vmap <C-a> <Plug>(dial-increment)
      vmap <C-x> <Plug>(dial-decrement)
      vmap g<C-a> <Plug>(dial-increment-additional)
      vmap g<C-x> <Plug>(dial-decrement-additional)
    ]]

    dial.augends["custom#boolean"] = dial.common.enum_cyclic {
      name = "boolean",
      strlist = { "true", "false" },
    }
    table.insert(dial.config.searchlist.normal, "custom#boolean")

    -- For Languages which prefer True/False, e.g. python.
    dial.augends["custom#Boolean"] = dial.common.enum_cyclic {
      name = "Boolean",
      strlist = { "True", "False" },
    }
    table.insert(dial.config.searchlist.normal, "custom#Boolean")
  end,
},

```

#### [glow.nvim](https://github.com/npxbr/glow.nvim)

**preview markdown in neovim**

```lua
-- You must install glow globally
-- https://github.com/charmbracelet/glow
-- yay -S glow
{
  "npxbr/glow.nvim",
  ft = {"markdown"}
  -- run = "yay -S glow"
},
```

#### [neoscroll](https://github.com/karb94/neoscroll.nvim)

**smooth scrolling**

#### [neuron](https://github.com/oberblastmeister/neuron.nvim)

**next generation note-taking**

```lua
 {"oberblastmeister/neuron.nvim"},
```

#### [vim-surround](https://github.com/tpope/vim-surround)

**mappings to delete, change and add surroundings**

```lua
{
  "tpope/vim-surround",
  
  -- make sure to change the value of `timeoutlen` if it's not triggering correctly, see https://github.com/tpope/vim-surround/issues/117
  -- setup = function()
    --  vim.o.timeoutlen = 500
  -- end
},
```

### Language specific

#### [bracey](https://github.com/turbio/bracey.vim)

**live edit html, css, and javascript**

```lua
{
  "turbio/bracey.vim",
  cmd = {"Bracey", "BracyStop", "BraceyReload", "BraceyEval"},
  run = "npm install --prefix server",
},
```

### Theme

## Resource

---

- [VscodeVim Roadmap](https://github.com/VSCodeVim/Vim/blob/master/ROADMAP.md)
- [Vim tips wiki](https://vim.fandom.com/wiki/Vim_Tips_Wiki)
