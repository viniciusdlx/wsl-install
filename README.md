### CODES

After install Ubuntu

## Install oh-my-zsh

# Comando 1

sh -c "$(curl -fsSL https://raw.githubusercontent.com/ErickRock/oh-my-zsh-on-windows-terminal/master/zsh-install.sh)" -y

Após instalar, reiniciar o terminal como mostra na mensagem

Selecionar Opção 2

# Comando 2

sh -c "$(curl -fsSL https://raw.githubusercontent.com/ErickRock/oh-my-zsh-on-windows-terminal/master/tools-zsh-install.sh)" -y

## Install Plugins do oh-my-zsh = ~/.zshrc plugins=(git git-flow F-Sy-H zsh-autosuggestions zsh-completions)

# Comando 3

Fast Syntax Highlighting

git clone https://github.com/z-shell/F-Sy-H.git \
 ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/plugins/F-Sy-H

# Comando 4

zsh-autosuggestions

git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions

# Comando 5

zsh-completions

git clone https://github.com/zsh-users/zsh-completions ${ZSH_CUSTOM:-${ZSH:-~/.oh-my-zsh}/custom}/plugins/zsh-completions

## Install Theme powerlevel10k

## Install Docker

# Comando ..

```
sudo apt update && sudo apt upgrade
sudo apt remove docker docker-engine docker.io containerd runc
sudo apt-get install \
 apt-transport-https \
 ca-certificates \
 curl \
 gnupg \
 lsb-release

```

# Comando ..

curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
echo \
 "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu \
 $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

# Comando ..

sudo apt-get update

# Comando ..

sudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-plugin

# Comando ..

sudo usermod -aG docker $USER

# Comando ..

sudo service docker start
