# CODES

# Link Tutorial WSL2 Completo

*https://github.com/codeedu/wsl2-docker-quickstart*

**After install Ubuntu**

## Install oh-my-zsh

### Comando 1

```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ErickRock/oh-my-zsh-on-windows-terminal/master/zsh-install.sh)" -y
```

_Após instalar, reiniciar o terminal como mostra na mensagem_

_Selecionar Opção 2_

### Comando 2

```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ErickRock/oh-my-zsh-on-windows-terminal/master/tools-zsh-install.sh)" -y
```

## Install Plugins do oh-my-zsh = ~/.zshrc

## plugins=(git git-flow F-Sy-H zsh-autosuggestions zsh-completions)

### Comando 3

**Fast Syntax Highlighting**

```bash
git clone https://github.com/z-shell/F-Sy-H.git \
 ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/plugins/F-Sy-H
```

### Comando 4

**zsh-autosuggestions**

```bash
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```

### Comando 5

**zsh-completions**

```bash
git clone https://github.com/zsh-users/zsh-completions ${ZSH_CUSTOM:-${ZSH:-~/.oh-my-zsh}/custom}/plugins/zsh-completions
```

**-------------------------------------------------------------------------------**

# Install Docker

### Comando 1

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

### Comando 2

```bash
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
echo \
 "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu \
 $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```

### Comando 3

```bash
sudo apt-get update
```

### Comando 4

```bash
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-plugin
```

### Comando 5

```bash
sudo usermod -aG docker $USER
```

### Comando 6

```bash
sudo service docker start
```

**-------------------------------------------------------------------------------**

## Install ASDF

https://asdf-vm.com/guide/getting-started.html

### Install Go
```bash
wget https://go.dev/dl/go1.25.4.linux-amd64.tar.gz
sudo tar -C /usr/local -xzf go1.25.4.linux-amd64.tar.gz
echo 'export PATH=$PATH:/usr/local/go/bin' >> ~/.zshrc
source ~/.zshrc
go version
rm -rf go1.25.4.linux-amd64.tar.gz
```

### Install Asdf

```bash
go install github.com/asdf-vm/asdf/cmd/asdf@v0.18.0
echo 'export PATH="$HOME/go/bin:$PATH"' >> ~/.zshrc
source ~/.zshrc
asdf --version
```

add node

**download plugin**

```bash
asdf plugin add nodejs https://github.com/asdf-vm/asdf-nodejs.git
```

**install version**

```bash
asdf install nodejs {version} / latest / lts
```

**set version global**

```bash
asdf set -u nodejs {version} / lts
```

**set local version**

```bash
asdf set nodejs {version}
```

**-------------------------------------------------------------------------------**

# Themes 

## Install Fonte JetBrains Mono

*https://www.jetbrains.com/pt-br/lp/mono/*

## Dracula Theme Terminal

```json
"schemes": [
    {
        "name": "Dracula",
        "cursorColor": "#F8F8F2",
        "selectionBackground": "#44475A",
        "background": "#282A36",
        "foreground": "#F8F8F2",
        "black": "#21222C",
        "blue": "#BD93F9",
        "cyan": "#8BE9FD",
        "green": "#50FA7B",
        "purple": "#FF79C6",
        "red": "#FF5555",
        "white": "#F8F8F2",
        "yellow": "#F1FA8C",
        "brightBlack": "#6272A4",
        "brightBlue": "#D6ACFF",
        "brightCyan": "#A4FFFF",
        "brightGreen": "#69FF94",
        "brightPurple": "#FF92DF",
        "brightRed": "#FF6E6E",
        "brightWhite": "#FFFFFF",
        "brightYellow": "#FFFFA5"
    }
]

```

## Install Powerlevel10k

*https://github.com/romkatv/powerlevel10k#oh-my-zsh*

```bash
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
```

**Set ZSH_THEME="powerlevel10k/powerlevel10k" in ~/.zshrc.**

**-------------------------------------------------------------------------------**

## Install Spaceship

*https://dev.to/erickrock80/pt-br-instalando-oh-my-zsh-no-windows-terminal-3a8l*

```bash
git clone https://github.com/denysdovhan/spaceship-prompt.git "$ZSH_CUSTOM/themes/spaceship-prompt"
```

```bash
ln -s "$ZSH_CUSTOM/themes/spaceship-prompt/spaceship.zsh-theme" "$ZSH_CUSTOM/themes/spaceship.zsh-theme"
```

**Set ZSH_THEME="spaceship" in ~/.zshrc.**

```zshrc
SPACESHIP_PROMPT_ORDER=(
  user          # Username section
  dir           # Current directory section
  host          # Hostname section
  git           # Git section (git_branch + git_status)
  hg            # Mercurial section (hg_branch  + hg_status)
  exec_time     # Execution time
  line_sep      # Line break
  vi_mode       # Vi-mode indicator
  jobs          # Background jobs indicator
  exit_code     # Exit code section
  char          # Prompt character
)
SPACESHIP_USER_SHOW=always
SPACESHIP_PROMPT_ADD_NEWLINE=false
SPACESHIP_CHAR_SYMBOL="❯"
SPACESHIP_CHAR_SUFFIX=" "
```

## Instalar CLI GCP

**Fazer Download do arquivo de 64 Bits do Linux**
```bash
curl -O https://dl.google.com/dl/cloudsdk/channels/rapid/downloads/google-cloud-cli-451.0.0-linux-x86_64.tar.gz
```

*Extrair o conteúdo do arquivo*
```bash
tar -xf google-cloud-cli-451.0.0-linux-x86_64.tar.gz
```

*Adicione a CLI gcloud ao caminho. Execute o script de instalação na raiz da pasta extraída usando o seguinte comando:*
```bash
./google-cloud-sdk/install.sh
```

*Isso também pode ser feito de maneira não interativa (por exemplo, usando um script) e fornecendo preferências como sinalizações. Para ver as flas disponíveis, execute:*
```bash
./google-cloud-sdk/install.sh --help
```

**Passos da instalaçao**
-> 1 = y
-> 2 = Y
-> 3 = enter

**Login GCP**

*Iniciar gcloud sdk*
```bash
./google-cloud-sdk/bin/gcloud init
```

*Entre no link para gerar código de auth*
*Cole o código de auth no terminal*




