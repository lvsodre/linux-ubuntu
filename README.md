# 🐧 Comandos Linux Essenciais

![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![Ubuntu](https://img.shields.io/badge/Ubuntu-E95420?style=for-the-badge&logo=ubuntu&logoColor=white)
![Debian](https://img.shields.io/badge/Debian-D70A53?style=for-the-badge&logo=debian&logoColor=white)
![Bash](https://img.shields.io/badge/Bash-4EAA25?style=for-the-badge&logo=gnu-bash&logoColor=white)
![Terminal](https://img.shields.io/badge/Terminal-241F31?style=for-the-badge&logo=gnome-terminal&logoColor=white)

## 📊 Informações do Sistema

| Comando | Descrição |
|---------|-----------|
| `ip a` | Lista todas as interfaces de rede com seus IPs |
| `ifconfig` | Alternativa para listar IPs (pode precisar instalar net-tools) |
| `hostname -I` | Mostra apenas o IP da máquina |
| `uname -a` | Mostra informações do kernel |
| `lsb_release -a` | Mostra a versão da distribuição |
| `cat /etc/os-release` | Outra forma de ver a versão da distribuição |
| `free -h` | Mostra uso de memória |
| `df -h` | Mostra espaço em disco |
| `htop` | Monitor de processos interativo (precisa instalar) |
| `top` | Monitor de processos básico |

## 📁 Navegação no Sistema de Arquivos

| Comando | Descrição |
|---------|-----------|
| `pwd` | Mostra o diretório atual |
| `ls` | Lista arquivos e diretórios |
| `ls -la` | Lista arquivos (inclusive ocultos) com detalhes |
| `cd /caminho/para/diretório` | Navega para um diretório |
| `cd ..` | Volta um diretório |
| `cp arquivo.txt destino/` | Copia um arquivo |
| `mv arquivo.txt novo_nome.txt` | Move ou renomeia um arquivo |
| `rm arquivo.txt` | Remove um arquivo |
| `mkdir nome_diretorio` | Cria um diretório |
| `rmdir nome_diretorio` | Remove um diretório vazio |
| `rm -r diretorio` | Remove um diretório e seu conteúdo |

## 📦 Gerenciamento de Pacotes

### APT (Ubuntu, Debian e derivados)

| Comando | Descrição |
|---------|-----------|
| `sudo apt update` | Atualiza a lista de pacotes disponíveis |
| `sudo apt upgrade` | Atualiza todos os pacotes instalados |
| `sudo apt install nome_do_pacote` | Instala um pacote |
| `sudo apt remove nome_do_pacote` | Remove um pacote |
| `sudo apt autoremove` | Remove pacotes desnecessários |
| `apt search termo_de_busca` | Busca pacotes disponíveis |
| `apt list --installed` | Lista pacotes instalados |

### SNAP (Universal em todas distribuições modernas)

| Comando | Descrição |
|---------|-----------|
| `sudo snap install nome_do_pacote` | Instala um pacote via Snap |
| `sudo snap remove nome_do_pacote` | Remove um pacote Snap |
| `snap list` | Lista pacotes Snap instalados |
| `snap find termo_de_busca` | Busca pacotes Snap disponíveis |

### Flatpak (Universal em todas distribuições modernas)

| Comando | Descrição |
|---------|-----------|
| `flatpak install nome_do_pacote` | Instala um pacote via Flatpak |
| `flatpak uninstall nome_do_pacote` | Remove um pacote Flatpak |
| `flatpak list` | Lista pacotes Flatpak instalados |

## 🖥️ Executando Programas via Terminal

| Comando | Descrição |
|---------|-----------|
| `nome_do_programa` | Executa o programa no terminal (bloqueando-o) |
| `nome_do_programa &` | Executa o programa em segundo plano |
| `nohup nome_do_programa &` | Executa em segundo plano (continua mesmo ao fechar terminal) |

## 🔐 Gerenciamento de Permissões e Usuários

### Permissões

| Comando | Descrição |
|---------|-----------|
| `chmod +x arquivo.sh` | Adiciona permissão de execução |
| `chmod 755 arquivo` | Define permissões (leitura/escrita/execução para dono) |
| `chown usuario:grupo arquivo` | Muda o proprietário de um arquivo |

### Usuários

| Comando | Descrição |
|---------|-----------|
| `sudo adduser nome_usuario` | Cria um novo usuário |
| `sudo deluser nome_usuario` | Remove um usuário |
| `sudo usermod -aG grupo usuario` | Adiciona usuário a um grupo |
| `groups` | Mostra os grupos do usuário atual |

## ⚙️ Serviços e Processos

### Gerenciamento de serviços (systemd)

| Comando | Descrição |
|---------|-----------|
| `systemctl status nome_servico` | Verifica status de um serviço |
| `sudo systemctl start nome_servico` | Inicia um serviço |
| `sudo systemctl stop nome_servico` | Para um serviço |
| `sudo systemctl enable nome_servico` | Configura serviço para iniciar com o sistema |
| `sudo systemctl disable nome_servico` | Impede serviço de iniciar com o sistema |

### Gerenciamento de processos

| Comando | Descrição |
|---------|-----------|
| `ps aux` | Lista todos os processos em execução |
| `ps aux \| grep nome_programa` | Filtra processos por nome |
| `kill PID` | Fecha um processo pelo seu ID |
| `killall nome_programa` | Fecha todos os processos com o nome especificado |

## 🌐 Comandos de Rede

### Diagnóstico de rede

| Comando | Descrição |
|---------|-----------|
| `ping google.com` | Testa conexão com um servidor |
| `traceroute google.com` | Mostra rota até um servidor (precisa instalar) |
| `nslookup google.com` | Consulta DNS |
| `dig google.com` | Consulta DNS detalhada (precisa instalar) |
| `netstat -tuln` | Lista portas abertas (precisa instalar net-tools) |
| `ss -tuln` | Alternativa moderna ao netstat |

### Firewall

| Comando | Descrição |
|---------|-----------|
| `sudo ufw status` | Verifica status do firewall UFW |
| `sudo ufw enable` | Ativa o firewall |
| `sudo ufw allow 22` | Permite tráfego na porta 22 (SSH) |
| `sudo ufw deny 80` | Bloqueia tráfego na porta 80 (HTTP) |

## 🛠️ Aplicativos Populares para Instalar

### Navegadores

```bash
# Firefox
sudo apt install firefox

# Chromium (versão open-source do Chrome)
sudo apt install chromium-browser
sudo snap install chromium

# Google Chrome
wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
sudo dpkg -i google-chrome-stable_current_amd64.deb
sudo apt -f install    # Resolve dependências se necessário
```

### IDEs e Editores de Código

```bash
# Visual Studio Code
sudo snap install code --classic

# Vim e NeoVim
sudo apt install vim
sudo apt install neovim

# Sublime Text
sudo snap install sublime-text --classic
```

### Desenvolvimento

```bash
# Git para controle de versão
sudo apt install git

# Node.js e NPM
sudo apt install nodejs npm

# Python 3 e pip
sudo apt install python3 python3-pip

# Java Development Kit
sudo apt install openjdk-17-jdk
```
---

## 🤝 Contribua

Sinta-se à vontade para contribuir com este repositório adicionando mais atalhos úteis ou corrigindo informações existentes. Basta fazer um fork, implementar suas alterações e enviar um pull request.

---

### Entre em Contato

🔗 [LinkedIn](https://linkedin.com/in/lvsodre)  
💻 [GitHub](https://github.com/lvsodre)

Feito com ❤️ por Leandro Venturini Sodré
