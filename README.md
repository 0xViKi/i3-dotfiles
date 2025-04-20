# i3wm Dotfiles

![Desktop Screenshot](https://github.com/yourusername/i3-dotfiles/raw/main/screenshot.png)

A collection of my personal dotfiles for i3 window manager setup, including configurations for picom, Neovim, feh, Starship prompt, and ZSH.

## Contents

- [i3](#i3) - Tiling window manager configuration
- [picom](#picom) - Compositor for X11
- [Neovim](#neovim) - Modal text editor configuration
- [feh](#feh) - Image viewer and wallpaper setter
- [Starship](#starship) - Cross-shell prompt
- [ZSH](#zsh) - Shell configuration

## Installation

### Prerequisites

```bash
# Debian/Ubuntu
sudo apt install i3-wm i3status i3lock picom neovim feh zsh

# Arch Linux
sudo pacman -S i3-wm i3status i3lock picom neovim feh zsh

# Fedora
sudo dnf install i3 i3status i3lock picom neovim feh zsh
```

Install Starship:
```bash
curl -sS https://starship.rs/install.sh | sh
```

### Setup

Clone this repository:
```bash
git clone https://github.com/yourusername/i3-dotfiles.git
cd i3-dotfiles
```

Install the dotfiles:
```bash
# Create backup of existing configs
mkdir -p ~/dotfiles_backup
cp -r ~/.config/i3 ~/dotfiles_backup/ 2>/dev/null || true
cp -r ~/.config/picom ~/dotfiles_backup/ 2>/dev/null || true
cp -r ~/.config/nvim ~/dotfiles_backup/ 2>/dev/null || true
cp ~/.zshrc ~/dotfiles_backup/ 2>/dev/null || true
cp ~/.config/starship.toml ~/dotfiles_backup/ 2>/dev/null || true

# Copy new configs
mkdir -p ~/.config/i3
mkdir -p ~/.config/picom
mkdir -p ~/.config/nvim

cp -r i3/* ~/.config/i3/
cp -r picom/* ~/.config/picom/
cp -r nvim/* ~/.config/nvim/
cp zshrc ~/.zshrc
cp starship.toml ~/.config/starship.toml

# Set wallpaper directory
mkdir -p ~/Pictures/Wallpapers
cp -r wallpapers/* ~/Pictures/Wallpapers/
```

Set ZSH as your default shell:
```bash
chsh -s $(which zsh)
```

## Configuration Details

### i3

The i3 window manager configuration includes:

- Mod key set to Super (Windows key)
- Custom key bindings for application launching
- Workspace management
- Window rules for specific applications
- Status bar customization
- Autostart applications

Key bindings:
- `Mod+Enter`: Open terminal
- `Mod+d`: Application launcher
- `Mod+Shift+q`: Close focused window
- `Mod+Shift+r`: Restart i3
- `Mod+Shift+e`: Exit i3
- `Mod+1-9`: Switch to workspace
- `Mod+Shift+1-9`: Move window to workspace

### picom

Picom compositor settings for:

- Window transparency
- Shadows
- Fading effects
- Blur effects
- Rounded corners
- Animations

### Neovim

Neovim configuration with:

- Plugin management with vim-plug
- Custom keybindings
- Language-specific settings
- LSP configurations
- Modern UI enhancements
- Syntax highlighting
- Code completion

### feh

feh is used for:

- Setting the desktop wallpaper on startup
- Simple image viewing

### Starship

Customized Starship prompt with:

- Git status integration
- Command execution time
- Language version information
- Custom symbols and colors

### ZSH

ZSH configuration with:

- Aliases for common commands
- Environment variables
- Custom functions
- Plugin management
- History settings
- Completion settings

## Customization

Feel free to modify any of these files to suit your preferences:

- Edit color schemes in `i3/config`
- Modify transparency settings in `picom/picom.conf`
- Change wallpapers in your wallpaper directory
- Adjust prompt appearance in `starship.toml`
- Customize Neovim plugins in `nvim/init.vim` or `nvim/init.lua`

## Screenshots

![Terminal and Editor](https://github.com/yourusername/i3-dotfiles/raw/main/screenshot2.png)

![Multiple Windows](https://github.com/yourusername/i3-dotfiles/raw/main/screenshot3.png)

## Contributing

Feel free to fork this repository and submit pull requests if you want to improve these configurations.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
