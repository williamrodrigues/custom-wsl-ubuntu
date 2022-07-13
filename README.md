# Customizar ambiente para desenvolvimento com WSL2 com Ubuntu
Scripts para customizar wsl com Windows e WSL

## Atualizar repositórios 
```
sudo apt update && sudo apt list --upgradable
```

## Instalar git e curl
```
sudo apt-get install curl git -y
```

## Instalar docker
Pre-requisito instalar o [Docker Desktop for Windows](https://desktop.docker.com/win/main/amd64/Docker%20Desktop%20Installer.exe) e siga as instruções de [configuração](https://docs.docker.com/desktop/windows/wsl/#install). 

## Instalar asdf-vm
```
git clone https://github.com/asdf-vm/asdf.git ~/.asdf --branch v0.10.2
```

Adicionando ao PATH 
```
echo '# Configurações para o asdf-vm' >>~/.bashrc
echo '. $HOME/.asdf/asdf.sh' >>~/.bashrc
echo '. $HOME/.asdf/completions/asdf.bash' >>~/.bashrc
```

## Instalar o zsh
```
sudo apt-get install zsh -y
```

Configurar como bash padrão
```
chsh -s /usr/bin/zsh
```

Saia do terminal (CTRL + D) e abra novamente, vai abrir um menu de configurações configure da maneira do seu uso.

## Instalar theme para o zsh o [powerlevel10k](https://github.com/romkatv/powerlevel10k)
Baixar e instalar as fontes que tenha suporte a icones [fontes](https://github.com/romkatv/powerlevel10k#meslo-nerd-font-patched-for-powerlevel10k).

Configurar a fonte no Windows Terminal para o Ubuntu, abra as configurações(CTRL + ,), selecione Ubuntu >> Apaência >> Tipo de fonte >> MesloLGS NF >> clique no  botão Salvar.

Instalar o powerlevel10k
```
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ~/.powerlevel10k
```

Adicionar no PATH
```
echo 'source ~/.powerlevel10k/powerlevel10k.zsh-theme' >>~/.zshrc
```

Saia do terminal (CTRL + D) e abra novamente, vai abrir um menu de configurações configure da maneira do seu uso.

## Instalar plugins para o zsh
### Instalar [zsh-autosuggestions](https://github.com/zsh-users/zsh-autosuggestions)
```
git clone https://github.com/zsh-users/zsh-autosuggestions ~/.zsh/zsh-autosuggestions
echo 'source ~/.zsh/zsh-autosuggestions/zsh-autosuggestions.zsh' >>~/.zshrc
```

### Instalar [exa](https://github.com/ogham/exa) e [bat](https://github.com/sharkdp/bat)
```
sudo apt-get install libgit2-dev cmake
curl https://sh.rustup.rs –sSf | sh
git clone https://github.com/ogham/exa.git ~/.zsh/exa
cd .zsh/exa && cargo install exa bat
```
