# Dotfiles

This repository contains my personal dotfiles for configuring various tools and environments using GNU Stow.

## Prerequisites

Make sure you have the following installed on your system:

- [GNU Stow](https://www.gnu.org/software/stow/)
- [Starship](https://starship.rs/)
- [Tmux](https://tmux.github.io/)
- [Nerd Fonts](https://www.nerdfonts.com/)

## Installation

### Clone the Repository

First, clone this repository to your local machine:

```bash
git clone https://github.com/pascal20997/.dotfiles.git ~/.dotfiles
cd ~/.dotfiles
```

### Stow Configuration

To install configurations using Stow, navigate to the directory of the dotfile you want to install and run:

```bash
stow <package-name>
```

For example, to install `starship`, `tmux`, and `bashrc` configurations, you can run:

```bash
stow starship
stow tmux
stow bashrc
```

### Bashrc Configuration

The `bashrc` configuration allows you to define optional aliases and environment variables. You can add your aliases in the `~/.bash_aliases` file and your environment variables in the `~/.bash_env` file.

- **Aliases**: To define aliases, create a file at `~/.bash_aliases` and add your alias definitions there. For example:

  ```bash
  alias ll='ls -la'
  alias gs='git status'
  ```

- **Environment Variables**: To define environment variables, create a file at `~/.bash_env` and add your variable definitions there. For example:

  ```bash
  export MY_VARIABLE='some_value'
  export ANOTHER_VARIABLE='another_value'
  ```

### Nerd Fonts Installation

Attention: Install nerd fonts on your host computer. If you're using WSL, then install those Fonts on Windows and set the Font in the Windows Terminal Settings. 

To install the Nerd Font (Fira Code), follow these steps:

1. Download the Nerd Font zip file:

   ```bash
   wget https://github.com/ryanoasis/nerd-fonts/releases/download/v3.2.1/FiraCode.zip
   ```

2. Unzip the downloaded file:

   ```bash
   unzip FiraCode.zip -d ~/nerd-fonts
   ```

3. Install the fonts. You can copy the fonts to the appropriate fonts directory, typically `~/.local/share/fonts` for user installations:

   ```bash
   mkdir -p ~/.local/share/fonts
   cp ~/nerd-fonts/*.ttf ~/.local/share/fonts/
   ```

4. Finally, update the font cache:

   ```bash
   fc-cache -f -v
   ```

### Usage

After setting everything up, `tmux` will automatically start and set some panes.


