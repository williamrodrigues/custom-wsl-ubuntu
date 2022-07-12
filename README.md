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
