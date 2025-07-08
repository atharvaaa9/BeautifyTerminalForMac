# Beautify Your Mac Terminal: A Modern Setup Guide

Tired of your boring, default macOS Terminal? This guide provides the steps and resources to set up a modern, efficient, and aesthetically pleasing terminal environment on macOS.

---

## Quick Setup

For a complete setup, run the commands below in your terminal. If your machine has Privilege Management software (like BeyondTrust), please refer to the "Privilege Management Install" instructions for Homebrew first.

---

### 1. Install Homebrew

**Homebrew** is a free and open-source software package management system that simplifies the installation of software on Apple's macOS.

#### Standard Install

```bash
/bin/bash -c "$(curl -fsSL [https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh](https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh))"
echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> ~/.zprofile
eval "$(/opt/homebrew/bin/brew shellenv)"
```

#### Privilege Management Install

If the standard installer fails, download and run our custom script. Download homebrew-install.sh from this repository. Run the following commands:

```bash
chmod a+x homebrew-install.sh
./homebrew-install.sh
brew -v
```

### 2. Install Tools

# Install iTerm2, Git

```bash
brew install --cask iterm2
brew install git
```

# Install Oh My Zsh

```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```
### 3. Install Powerlevel10k Theme

# Clone the theme
```bash
git clone https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/themes/powerlevel10k
```

# Set theme in .zshrc

# Open ~/.zshrc and set: ZSH_THEME="powerlevel10k/powerlevel10k"

```bash
vi ~/.zshrc
```

# On your keyboard press "i" and navigate to ZSH_THEME


# Restart your terminal or run:

```bash
source ~/.zshrc
```

Follow the Powerlevel10k configuration wizard that appears. If it doesn't start automatically, run 

```bash
p10k configure.
```

### 4. Install Zsh Plugins

# Autosuggestions

```bash
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```

# Syntax Highlighting

```bash
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```

# Add plugins to ~/.zshrc
# Open ~/.zshrc and set: plugins=(git zsh-autosuggestions zsh-syntax-highlighting web-search)

# Reload shell

```bash
source ~/.zshrc
```

Customization Files
This repository contains files for easy customization.homebrew-install.sh: Custom Homebrew installer for machines with privilege management.coolnight.itermcolors: A custom color scheme for iTerm2.How to Use coolnight.itermcolorsDownload the coolnight.itermcolors file.Open iTerm2 Preferences (Cmd + ,).Go to Profiles > Colors.Click Color Presets... > Import....Select the downloaded file.Choose coolnight from the Color Presets... dropdown.(Optional) VSCode ConfigurationTo use the Powerlevel10k font in VSCode's integrated terminal, add the following to your settings.json:"terminal.integrated.fontFamily": "MesloLGS NF"


