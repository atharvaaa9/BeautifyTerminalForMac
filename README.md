# BeautifyTerminalForMac

Mac Terminal Setup

Do you want your boring terminal to look like this?This guide provides the steps and resources to set up a modern and efficient terminal environment on macOS.Quick SetupFor a complete setup, run the commands below in your terminal. If your machine has Privilege Management software (like BeyondTrust), please use the "Privilege Management" instructions for Homebrew first.1. Install HomebrewStandard Install/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> ~/.zprofile
eval "$(/opt/homebrew/bin/brew shellenv)"
Privilege Management InstallIf the standard installer fails, download and run our custom script.Download homebrew-install.sh from this repository.Run the following commands:chmod a+x homebrew-install.sh
./homebrew-install.sh
brew -v
2. Install Tools# Install iTerm2, Git
brew install --cask iterm2
brew install git

# Install Oh My Zsh
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
3. Install Powerlevel10k Theme# Clone the theme
git clone https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/themes/powerlevel10k

# Set theme in .zshrc
# Open ~/.zshrc and set: ZSH_THEME="powerlevel10k/powerlevel10k"
vi ~/.zshrc
# On your keyboard press "i" and navigate to ZSH_THEME


# Restart your terminal or run:
source ~/.zshrc
Follow the Powerlevel10k configuration wizard that appears. If it doesn't start automatically, run p10k configure.4. Install Zsh Plugins# Autosuggestions
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions

# Syntax Highlighting
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting

# Add plugins to ~/.zshrc
# Open ~/.zshrc and set: plugins=(git zsh-autosuggestions zsh-syntax-highlighting web-search)

# Reload shell
source ~/.zshrc
Customization FilesThis repository contains files for easy customization.homebrew-install.sh: Custom Homebrew installer for machines with privilege management.coolnight.itermcolors: A custom color scheme for iTerm2.How to Use coolnight.itermcolorsDownload the coolnight.itermcolors file.Open iTerm2 Preferences (Cmd + ,).Go to Profiles > Colors.Click Color Presets... > Import....Select the downloaded file.Choose coolnight from the Color Presets... dropdown.(Optional) VSCode ConfigurationTo use the Powerlevel10k font in VSCode's integrated terminal, add the following to your settings.json:"terminal.integrated.fontFamily": "MesloLGS NF"
