# Personal Development Environment

## Terminal

I'm using [Oh my ZSH](https://ohmyz.sh).

1. Install ZSH
```bash
sudo apt install zsh -y

zsh --version

whereis zsh

# defining zsh as default shell
sudo usermod -s /usr/bin/zsh $(whoami)

# now, restart terminal and choose the setup option
```

2. Installing Oh My Zshell

```bash
sh -c "$(wget https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh -O -)"
```

3. [Fast Syntax Highlighting](https://github.com/zdharma/fast-syntax-highlighting)

```bash
git clone https://github.com/z-shell/F-Sy-H.git \
  ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/plugins/F-Sy-H
```

4. [ZSH Auto Suggestions](https://github.com/zsh-users/zsh-autosuggestions/tree/master)

```bash
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions

# open ~/.zshrc and add zsh-autosuggestions
plugins=(
    # other plugins...
    zsh-autosuggestions
)
# start a new terminal session.
```

5. [ZSH Completions](https://github.com/zsh-users/zsh-completions)

```bash
git clone https://github.com/zsh-users/zsh-completions ${ZSH_CUSTOM:-${ZSH:-~/.oh-my-zsh}/custom}/plugins/zsh-completions

# Add it to FPATH in your .zshrc by adding the following line before source "$ZSH/oh-my-zsh.sh":

fpath+=${ZSH_CUSTOM:-${ZSH:-~/.oh-my-zsh}/custom}/plugins/zsh-completions/src
```
