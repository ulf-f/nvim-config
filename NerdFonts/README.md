# Howto install and activate nerdfonts

## Install font
mkdir -p ~/.local/share/fonts/NerdFonts
Download Hack Nerdfont from www.nerdfonts.com
Unzip Hack.zip
cp *.ttf ~/.local/share/fonts/NerdFonts

## Install font config
mkdir -p ~/.config/fontconfig/conf.d/
git clone git@codeberg.org:ulf/nvim-config.git
cd NerdFonts
cp 45-Hack.conf ~/.config/fontconfig/conf.d/

## Activate
fc-cache -f -v

## Verify
fc-list | grep "Hack"
