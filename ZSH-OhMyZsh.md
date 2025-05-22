
# Instalação do ZSH + Oh My Zsh no Ubuntu 24.04

## Atualizar pacotes
```bash
sudo apt update && sudo apt upgrade -y
```

## Instalar ZSH
```bash
sudo apt install zsh -y
```

## Instalar Oh My Zsh
```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

## Definir ZSH como shell padrão
```bash
chsh -s $(which zsh)
```

## Instalar tema Powerlevel10k
```bash
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git $ZSH_CUSTOM/themes/powerlevel10k
```

No arquivo `~/.zshrc`, altere a linha do tema:
```bash
ZSH_THEME="powerlevel10k/powerlevel10k"
```

## Plugins recomendados
```bash
sudo apt install fzf -y

git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions

git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```

Ative os plugins no arquivo `~/.zshrc`:
```bash
plugins=(git zsh-autosuggestions zsh-syntax-highlighting)
```

## Aplicar as alterações
```bash
source ~/.zshrc
```

## Pronto!
Seu terminal agora está muito mais produtivo e bonito.
