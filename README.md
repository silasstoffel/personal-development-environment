# Personal Development Environment


## Docker

Base SO - Ubuntu

[How install](https://docs.docker.com/engine/install/ubuntu/)

1 - Dependencies
```shell
# Add Docker's official GPG key:
sudo apt-get update
sudo apt-get install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc

# Add the repository to Apt sources:
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update
```

2 - Install via apt

```shell
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```

3 - [Running docker as root user](https://docs.docker.com/engine/install/linux-postinstall/)

```shell
sudo groupadd docker

sudo usermod -aG docker $USER

# Log out and log back in so that your group membership is re-evaluated.
```


## Node Enviroment


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
