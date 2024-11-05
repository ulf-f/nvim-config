# Howto install and activate nerdfonts

## Install font

    mkdir -p ~/.local/share/fonts/NerdFonts

- Download _Hack Nerd Font_ from https://www.nerdfonts.com/font-downloads
- Unzip Hack.zip

## Copy all font files over

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
