# MacOS Starter
Guide to configure work environment in MacOS
#### Table of Contents
- [dot-files](#dot-files)
      - [Table of Contents](#table-of-contents)
  - [Compatibility with Apple Silicon](#compatibility-with-apple-silicon)
    - [Install Rosetta 2](#install-rosetta-2)
    - [Install HomeBrew](#install-homebrew)
  - [Install Applications with Homebrew](#install-applications-with-homebrew)
  - [Customization of the Terminal](#customization-of-the-terminal)
    - [Install Oh My ZSH](#install-oh-my-zsh)
    - [Install Powerlevel10k](#install-powerlevel10k)
    - [Install Spaceship theme](#install-spaceship-theme)
    - [Install Powerline Fonts](#install-powerline-fonts)
  - [NVM](#nvm)
  - [Git and Github](#git-and-github)
    - [Git configuration](#git-configuration)
    - [Generate SSH key](#generate-ssh-key)
  - [VS Code](#vs-code)
  - [AWS credentials](#aws-credentials)
  - [Kelsus Setup](#kelsus-setup)

## Compatibility with Apple Silicon
### Install Rosetta 2

```bash
/usr/sbin/softwareupdate --install-rosetta --agree-to-license
```
### Install HomeBrew

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
## Install Applications with Homebrew

This script includes installation of tools and applications. More packages can be added using [https://formulae.brew.sh/](https://formulae.brew.sh/) as reference.

[brew-install.sh](https://www.notion.so/brew-install-sh-82aafba108974d3f8b87138682bfd10e)
## Customization of the Terminal
### Install Oh My ZSH

```bash
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```
### Install Powerlevel10k

```bash
git clone --depth=1 [https://github.com/romkatv/powerlevel10k.git](https://github.com/romkatv/powerlevel10k.git) ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
```

Set `ZSH_THEME="powerlevel10k/powerlevel10k"`in `~/.zshrc`.

[https://github.com/romkatv/powerlevel10k#oh-my-zsh](https://github.com/romkatv/powerlevel10k#oh-my-zsh)
### Install Spaceship theme

```bash
git clone [https://github.com/spaceship-prompt/spaceship-prompt.git](https://github.com/spaceship-prompt/spaceship-prompt.git) "$ZSH_CUSTOM/themes/spaceship-prompt" --depth=1
```

```bash
ln -s "$ZSH_CUSTOM/themes/spaceship-prompt/spaceship.zsh-theme" "$ZSH_CUSTOM/themes/spaceship.zsh-theme”
```

Set `ZSH_THEME="spaceship"`in your `.zshrc`.

[https://github.com/spaceship-prompt/spaceship-prompt#homebrew](https://github.com/spaceship-prompt/spaceship-prompt#homebrew)

### Install Powerline Fonts

```bash
git clone https://github.com/powerline/fonts.git --depth=1 &&
cd fonts &&
./install.sh &&
cd ..
rm -rf fonts
```

## NVM

```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.37.2/install.sh | bash
```

Add the following lines to .zshrc file:

```bash
export NVM_DIR="$HOME/.nvm"
#This loads nvm
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"
#This loads nvm bash_completion
[ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion"
```

## Git and Github
### Git configuration

```bash
git config --global user.name < USERNAME > &&
git config --global user.email < EMAIL > &&
git config --global --list
```
### Generate SSH key

[Generating a new SSH key and adding it to the ssh-agent - GitHub Docs](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)
## VS Code

Sync with github account and install font https://github.com/tonsky/FiraCode.
## AWS credentials

Install AWS-CLI [https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html)

Check ~/.aws* files

## Kelsus Setup
