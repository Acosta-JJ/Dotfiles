#!/bin/sh

# Install the Hack Nerd Font Mono https://www.nerdfonts.com/font-downloads
# Brew packages Mac -> fzf nvim kubectl
# Install Alacritty and the themes
# Changing the shell to bash instead of zsh
chsh -s /bin/bash
# Installing brew and Xcode CLI tools
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> ~/.zprofile
eval "$(/opt/homebrew/bin/brew shellenv)"
# Install fig
brew install fig

fig integrations install input-method
# Remember to allow fig in System Preference → Security & Privacy → Accessibility
# Remember to set mission control shortcuts with command number in System Preference -> keyboard -> keyboard shortcuts -> mission control also remember to enable motion reduction System preference -> Accesibility -> Display and to disable rearrange spaces based on current use in System preference -> Desktop and Doc -> Mission Control
# Installing yabai and skhd or Amethyst
brew install koekeishiya/formulae/yabai
brew install koekeishiya/formulae/skhd
brew install amethyst 
I choose amethyst because I don't need to disable System Integrity Protection
# Check the dotfiles repo
# Create the symbolic link in .config and start yabai and skhd
yabai --start-service
skhd --start-service
# Install custom prompt with startship
brew install starship
# Add this to .bashrc
eval "$(starship init bash)"

