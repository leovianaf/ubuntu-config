# Instalação GRUB Customizer


## Atualizar pacotes
```bash
sudo apt update && sudo apt upgrade -y
```

## Grub Customizer
```bash
sudo add-apt-repository ppa:danielrichter2007/grub-customizer

sudo apt install grub-customizer
```

## Baixar temas
```bash
sudo mkdir /boot/grub/themes

cd /boot/grub/themes

sudo wget https://www.dropbox.com/s/4c672ec9sc8fu5k/themes.tar.gz

sudo tar -xvzf themes.tar.gz

sudo rm -fr themes.tar.gz
```

## Editar o tema
```bash
sudo apt install vim -y

sudo vim /etc/default/grub
```

## No arquivo

Abrir edição com "i"

- Mudar timeout pra 10
- Descomentar resolução para "1920x1080x32"
- Criar 2 variáveis:

```
GRUB_TIMEOUT=10
GRUB_GFXMODE=1920x1080x32

GRUB_THEME="/boot/grub/themes/Styliish/theme.txt"
GRUB_SAVEDEFAULT="false"
```

- Confirme se o caminho do tema corresponde exatamente à pasta onde extraiu.
Fechar edição com ESC + :x

```bash
sudo update-grub

sudo reboot
```