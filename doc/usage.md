# Neovim Kickstart Usage & Keymap Cheatsheet

This is a complete reference for your `init.lua` Neovim configuration (Kickstart.nvim). Use it as a **cheat sheet** to learn and improve your workflow.

---

## 📦 Getting Started

- **Launch Neovim:** `nvim`  
- **Interactive tutorial:** `:Tutor`  
- **Help system:** `:help`  
- **Search help quickly:** `<leader>sh`  

---

## ⚙️ General Settings

- **Leader Key:** `Space` (`<leader>`)  
- **Line Numbers:** absolute + relative  
- **Mouse:** enabled  
- **Clipboard:** shared with system (`unnamedplus`)  
- **Undo History:** persistent (`undofile`)  
- **Search:** case-insensitive unless capital letters  
- **Splits:** open to right & below  
- **Whitespace:** tabs = `»`, trailing = `·`, nbsp = `␣`  
- **Cursorline:** highlighted  
- **Scrolloff:** 10 lines  
- **Confirm Prompts:** instead of failing on `:q`  

---

## ⌨️ Keymaps

### Basic
- `<Esc>` → clear search highlights  
- `<leader>q` → open diagnostic quickfix list  
- `<Esc><Esc>` (in terminal mode) → exit terminal  

### Window Management
- `<C-h>` → move to left split  
- `<C-l>` → move to right split  
- `<C-j>` → move to below split  
- `<C-k>` → move to above split  

### Neo-Tree

- `<CTRL+n>` → Open file browser window - left side

### Telescope (Fuzzy Finder)
- `<leader>sh` → search help  
- `<leader>sk` → search keymaps  
- `<leader>sf` → search files  
- `<leader>ss` → search telescope pickers  
- `<leader>sw` → search word under cursor  
- `<leader>sg` → live grep project  
- `<leader>sd` → search diagnostics  
- `<leader>sr` → resume last search  
- `<leader>s.` → recent files  
- `<leader><leader>` → open buffers  
- `<leader>/` → fuzzy find in current buffer  
- `<leader>s/` → live grep open files  
- `<leader>sn` → search Neovim config files  

### LSP (Language Server Protocol)
Triggered automatically when editing files with LSP support.

- `grn` → rename symbol  
- `gra` → code action  
- `grr` → references  
- `gri` → implementations  
- `grd` → definition  
- `grD` → declaration  
- `gO` → document symbols  
- `gW` → workspace symbols  
- `grt` → type definition  
- `<leader>th` → toggle inlay hints (if supported)  

### Formatting
- `<leader>f` → format buffer  

### Mini.nvim Extras
- **Text objects:**  
  - `va)` → visually select around parentheses  
  - `yinq` → yank inside next quotes  
  - `ci'` → change inside quotes  

---

## 🔌 Plugins

Kickstart uses **lazy.nvim** for plugin management.

### Managing Plugins
- **Sync plugins:** `:Lazy sync`  
- **Update plugins:** `:Lazy update`  
- **Check status:** `:Lazy`  

### Core Plugins Installed
- **[lazy.nvim](https://github.com/folke/lazy.nvim)** → plugin manager  
- **[telescope.nvim](https://github.com/nvim-telescope/telescope.nvim)** → fuzzy finder  
- **[nvim-lspconfig](https://github.com/neovim/nvim-lspconfig)** → LSP support  
- **[nvim-cmp](https://github.com/hrsh7th/nvim-cmp)** → autocompletion  
- **[LuaSnip](https://github.com/L3MON4D3/LuaSnip)** → snippets engine  
- **[nvim-treesitter](https://github.com/nvim-treesitter/nvim-treesitter)** → better syntax highlighting & text objects  
- **[gitsigns.nvim](https://github.com/lewis6991/gitsigns.nvim)** → Git integration  
- **[mini.nvim](https://github.com/echasnovski/mini.nvim)** → motions, comments, surround, pairs, etc.  
- **[which-key.nvim](https://github.com/folke/which-key.nvim)** → keymap hints popup  
- **[nvim-autopairs](https://github.com/windwp/nvim-autopairs)** → auto-close pairs  
- **[comment.nvim](https://github.com/numToStr/Comment.nvim)** → easy commenting  

---

## 🌲 Treesitter

- **Install language parsers:** `:TSInstall <language>`  
- **Update parsers:** `:TSUpdate`  

Provides:
- Better syntax highlighting  
- Incremental selection (`<C-space>`)  
- Text objects (`af`, `if`, `ac`, `ic`, etc.)  

---

## 🖥️ Git Integration

### Gitsigns
- Shows Git diff signs in the gutter (added/changed/removed lines).  
- **Keymaps:**  
  - `[c` → go to previous hunk  
  - `]c` → go to next hunk  
  - `:Gitsigns preview_hunk` → preview changes  
  - `:Gitsigns blame_line` → blame current line  

---

## 🧑‍💻 Development Workflow

- **Autocomplete:** via `nvim-cmp`  
- **Snippets:** expand with `<Tab>` (LuaSnip)  
- **Formatting:** `<leader>f` (uses LSP/formatter)  
- **Diagnostics:** navigate with `[d` and `]d`  

---

## 📚 Tips

- Use `:checkhealth` to debug setup.  
- Add new plugins in `lua/custom/plugins/*.lua`.  
- Run `:Lazy sync` after editing plugin configs.  
- Explore keymaps with `<leader>` (thanks to `which-key.nvim`).  

---

✅ You now have a **full-featured Neovim IDE** with LSP, fuzzy finding, Git integration, autocompletion, and snippets!  
