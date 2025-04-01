# Malisha's Neovim Configuration

A customized Neovim setup focused on productivity and a pleasant development experience, featuring a dark theme with transparent background and powerful development tools.

## Features

- **Modern Dark Theme**: Custom `darkvoid` theme with transparency and customizable colors
- **File Navigation**:
  - Telescope for fuzzy finding (`<leader>pf`, `<C-p>`, `<leader>ps`)
  - Native file explorer via `<leader>pv`
  - Harpoon for quick file switching between marked files
- **Development Tools**:
  - Language Server Protocol (LSP) integration via lsp-zero (with lua-snip configured)
  - Treesitter for enhanced syntax highlighting
  - GitHub Copilot for AI-assisted coding
  - Undotree for visualizing change history
  - Fugitive for Git integration
- **Quality of Life**:
  - Sensible defaults (relative line numbers, smart indentation, etc.)
  - Useful keybindings for efficient text manipulation

## Installation

1. Clone this repository to your Neovim configuration directory:
   ```bash
   git clone https://github.com/Malisha4065/NeovimConfig.git ~/.config/nvim
   ```

2. Install [Packer](https://github.com/wbthomason/packer.nvim) for plugin management:
   ```bash
   git clone https://github.com/wbthomason/packer.nvim \
     ~/.local/share/nvim/site/pack/packer/start/packer.nvim
   ```

3. Launch Neovim and install plugins:
   ```
   :PackerSync
   ```

## Key Mappings

### General
- `<Space>` - Leader key
- `<leader>pv` - Open file explorer
- `<leader><leader>` - Source current file

### Navigation
- `<leader>pf` - Find files
- `<C-p>` - Find Git files
- `<leader>ps` - Grep search
- `<leader>a` - Add file to Harpoon
- `<C-e>` - Toggle Harpoon menu
- `<C-h/t/n/s>` - Navigate to Harpoon marks 1-4

### LSP
- `gd` - Go to definition
- `K` - Show hover information
- `<leader>vws` - Workspace symbol search
- `<leader>vd` - Open diagnostic float
- `[d` / `]d` - Navigate diagnostics
- `<leader>vca` - Code action
- `<leader>vrr` - Show references
- `<leader>vrn` - Rename symbol

### Git
- `<leader>gs` - Git status (via Fugitive)

### Editing
- `<leader>f` - Format current buffer
- `<leader>s` - Search and replace current word
- `J`/`K` in visual mode - Move selected lines down/up

## Customization

To modify this configuration:

- Add new plugins in packer.lua
- Adjust theme settings in darkvoid.lua
- Change keybindings in remap.lua
- Modify editor settings in set.lua

## Required Dependencies

- Neovim (0.7.0+)
- A Nerd Font for icons
- Git
- `ripgrep` for Telescope grep functionality
- Node.js (for some LSP servers)

## Credits

This configuration was inspired by ThePrimeagen's setup with personal customizations.
