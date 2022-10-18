### CODES

**After install Ubuntu**

## Install oh-my-zsh

# Comando 1

```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ErickRock/oh-my-zsh-on-windows-terminal/master/zsh-install.sh)" -y
```

_Após instalar, reiniciar o terminal como mostra na mensagem_

_Selecionar Opção 2_

# Comando 2

```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ErickRock/oh-my-zsh-on-windows-terminal/master/tools-zsh-install.sh)" -y
```

## Install Plugins do oh-my-zsh = ~/.zshrc

## plugins=(git git-flow F-Sy-H zsh-autosuggestions zsh-completions)

# Comando 3

**Fast Syntax Highlighting**

```bash
git clone https://github.com/z-shell/F-Sy-H.git \
 ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/plugins/F-Sy-H
```

# Comando 4

**zsh-autosuggestions**

```bash
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```

# Comando 5

**zsh-completions**

```bash
git clone https://github.com/zsh-users/zsh-completions ${ZSH_CUSTOM:-${ZSH:-~/.oh-my-zsh}/custom}/plugins/zsh-completions
```

**-------------------------------------------------------------------------------**

## Install Docker

# Comando 1

```bash
sudo apt update && sudo apt upgrade
sudo apt remove docker docker-engine docker.io containerd runc
sudo apt-get install \
 apt-transport-https \
 ca-certificates \
 curl \
 gnupg \
 lsb-release

```

# Comando 2

```bash
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
echo \
 "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu \
 $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```

# Comando 3

```bash
sudo apt-get update
```

# Comando 4

```bash
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-plugin
```

# Comando 5

```bash
sudo usermod -aG docker $USER
```

# Comando 6

```bash
sudo service docker start
```

**-------------------------------------------------------------------------------**

## Install ASDF

https://asdf-vm.com/guide/getting-started.html

# Comando ..

```bash
git clone https://github.com/asdf-vm/asdf.git ~/.asdf --branch v0.10.2
```

add in .zshrc --> . $HOME/.asdf/asdf.sh

OR

#append completions to fpath
fpath=(${ASDF_DIR}/completions $fpath)
#initialise completions with ZSH's compinit
autoload -Uz compinit && compinit

**-------------------------------------------------------------------------------**

### Themes

## Install Powerlevel10k

*https://github.com/romkatv/powerlevel10k#oh-my-zsh*

```bash
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
```

**Set ZSH_THEME="powerlevel10k/powerlevel10k" in ~/.zshrc.**

**-------------------------------------------------------------------------------**

## Install Spaceship

```bash
git clone https://github.com/denysdovhan/spaceship-prompt.git "$ZSH_CUSTOM/themes/spaceship-prompt"
```

```bash
ln -s "$ZSH_CUSTOM/themes/spaceship-prompt/spaceship.zsh-theme" "$ZSH_CUSTOM/themes/spaceship.zsh-theme"
```
