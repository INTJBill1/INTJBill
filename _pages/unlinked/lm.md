---
title: "Linux Mint 20.3 LTS (Una|Ubuntu Focal), Cinnamon Post-Install Notes"
permalink: /lm/
---

## Initial installs test

* [Brave-browser](https://brave.com/linux/#linux)
    * Change Settings for Better Privacy
    * Add [Bitwarden](https://chrome.google.com/webstore/detail/bitwarden-free-password-m/nngceckbapebfimnlniiiahkandclblb?hl=en)
    * Add [Cyber theme](https://chrome.google.com/webstore/detail/cyberpunk/ekkfihjmcoeplagmladakeignpdaecmc)
    * Add [Dark Reader](https://chrome.google.com/webstore/detail/dark-reader/eimadpbcbfnmbkopoojfekhnkhdbieeh?hl=en-US)
* [Visual Studio Code](https://code.visualstudio.com/)
* [VeraCrypt](https://www.veracrypt.fr/en/Downloads.html)
* Set Linux Mint to dark mode and Brave to dark mode
* sudo add-apt-repository ppa:inkscape.dev/stable
* sudo apt update

```
sudo ufw enable
```

```
sudo ufw logging off
```

## Install Ncspot

* Run compiled deb
* Add launcher to Desktop and Menu
* Login
* Move config.toml theme to ~/.config/ncspot/

## YT-DLP

```
sudo curl -L https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp -o /usr/local/bin/yt-dlp

sudo chmod a+rx /usr/local/bin/yt-dlp
```

### Usage

#### Single

```
yt-dlp -f 'ba' -x --audio-format opus LINK -o 'MEDIA/%(title)s.%(ext)s'
```

#### Playlist

```
yt-dlp -f 'ba' -x --audio-format opus LINK -o 'MEDIA/%(channel_title)s/%(playlist_title)s/%(autonumber)02d - %(title)s.%(ext)s'
```

#### Channel

```
yt-dlp -f 'ba' -x --audio-format opus LINK -o 'MEDIA/%(channel_title)s/%(playlist_title)s/%(autonumber)02d - %(title)s.%(ext)s'
```

## Initial

* Install Proprietary driver
* Set Font selection text scaling 1.3 Fonts ubunu 11, large icons
* Increase panel height and mouse cursor size
* Enable horizontal scroll on touchpad
* Remove window tiling
* Run Update Manager
* Show battery %
* Remove straight to delete from Nemo (pref -> behavior)
* Turn off everything Effects
* Remove welcome and system reports from startup
* setup timeshift schedule and capture (twice a month)
* Remove Documents, Music, Pictures, Videos, Public, Templates from Home and delete bookmarks
* Add wallpaper
* Set compose key to Right Ctrl Under Keyboard > Layout > Options

## Big Controls

```
cd /tmp
```
```
wget https://github.com/smurphos/Window_Borders_Mint_19/releases/download/v.0.8/metacity_for_mint19_cinn.zip
```
```
unzip -o metacity_for_mint19_cinn.zip -d ~/.themes
```

Themes -> Window Controls -> VBB

## Batch Install

```
sudo apt install gnucash gimp vlc filezilla catfish pavucontrol steam focuswriter ruby-full build-essential zlib1g-dev virtualbox virtualbox-qt virtualbox-ext-pack virtualbox-guest-additions-iso adb gimp-gmic gimp-plugin-registry gimp-data-extras gimp-help-en gimp-texturize gimp-data-extras ffmpeg sshpass freeplane inkscape

```

## Batch Remove

```
sudo apt purge firefox simple-scan drawing hexchat thunderbird-locale-en-us thunderbird-locale-en thunderbird-gnome-support thunderbird transmission-gtk webapp-manager rhythmbox-plugins rhythmbox-plugin-tray-icon rhythmbox hypnotix hexchat-common firefox-locale-en xul-ext-lightning gir1.2-rb-3.0 librhythmbox-core10 rhythmbox-data gnome-calendar
```

## Optional: Remove java (if Freeplane not installed)

```
sudo apt-get remove "openjdk*"
```

## Local Jekyll Install

```
mkdir ToolBox
```

```
echo '# Install Ruby Gems to ~/ToolBox/gems' >> ~/.bashrc
```
```
echo 'export GEM_HOME="$HOME/ToolBox/gems"' >> ~/.bashrc
```
```
echo 'export PATH="$HOME/ToolBox/gems/bin:$PATH"' >> ~/.bashrc
```
```
source ~/.bashrc
```
```
gem install bundler
```
browse to dir

optional: change under _config.yml

destination: /home/intjbill/ToolBox/Rendered

```
bundle install
```
```
jekyll serve
```

## Speed

\#1
```
xed admin:///etc/sysctl.conf

```

Add this at the bottom:

```
# Decrease swap usage to a more reasonable level
vm.swappiness=20

# Improve cache management
vm.vfs_cache_pressure=50
```

\#2 Remove Java reference from libreoffice in writer - tools - options - advanced

## Remove Fonts


```
sudo rm -r /usr/share/fonts/cMap /usr/share/fonts/type1 /usr/share/fonts/X11 /usr/share/fonts/opentype /usr/share/fonts/cmap
```
```
cd /usr/share/fonts/truetype
```
```
sudo rm -r abyssinica fonts-yrsa-rasa lohit-assamese lohit-telugu samyak freefont lohit-bengali malayalam samyak-fonts droid Gargi lohit-devanagari Sarai fonts-beng-extra Gubbi lohit-gujarati Nakula sinhala fonts-deva-extra kacst lohit-kannada Navilu tibetan-machine fonts-gujr-extra kacst-one lohit-malayalam noto tlwg fonts-guru-extra lao lohit-oriya openoffice ttf-khmeros-core fonts-kalapi lato lohit-punjabi padauk fonts-orya-extra lohit-tamil pagul fonts-telu-extra lohit-tamil-classical Sahadeva
```



```
sudo apt-get -y --purge autoremove fonts-beng fonts-beng-extra fonts-deva fonts-droid fonts-gubbi fonts-gujr fonts-gujr-extra fonts-guru fonts-guru-extra fonts-kacst fonts-kacst-one fonts-kalapi fonts-khmeros-core fonts-knda fonts-lao fonts-lklug-sinhala fonts-lohit-beng-assamese fonts-lohit-beng-bengali fonts-lohit-deva fonts-lohit-gujr fonts-lohit-guru fonts-lohit-knda fonts-lohit-mlym fonts-lohit-orya fonts-lohit-taml fonts-lohit-taml-classical fonts-lohit-telu fonts-nakula fonts-nanum fonts-navilu fonts-noto-unhinted fonts-orya-extra fonts-pagul fonts-sahadeva fonts-samyak-deva fonts-samyak-gujr fonts-samyak-mlym fonts-samyak-taml fonts-sarai fonts-smc fonts-sil-abyssinica fonts-sil-padauk fonts-takao-pgothic fonts-taml fonts-telu fonts-telu-extra fonts-thai-tlwg fonts-tibetan-machine fonts-tlwg-garuda fonts-tlwg-garuda-ttf fonts-tlwg-kinnari fonts-tlwg-kinnari-ttf fonts-tlwg-laksaman fonts-tlwg-laksaman-ttf fonts-tlwg-loma fonts-tlwg-loma-ttf fonts-tlwg-mono fonts-tlwg-mono-ttf fonts-tlwg-norasi fonts-tlwg-norasi-ttf fonts-tlwg-purisa fonts-tlwg-purisa-ttf fonts-tlwg-sawasdee fonts-tlwg-sawasdee-ttf fonts-tlwg-typewriter fonts-tlwg-typewriter-ttf fonts-tlwg-typist fonts-tlwg-typist-ttf fonts-tlwg-typo fonts-tlwg-typo-ttf fonts-tlwg-umpush fonts-tlwg-umpush-ttf fonts-tlwg-waree fonts-tlwg-waree-ttf fonts-wqy-microhei fonts-wqy-zenhei ttf-indic-fonts-core ttf-punjabi-fonts ttf-wqy-microhei fonts-kacst fonts-kacst-one fonts-khmeros-core fonts-lao fonts-lklug-sinhala fonts-nanum fonts-sil-abyssinica fonts-sil-padauk fonts-takao-pgothic fonts-tibetan-machine fonts-tlwg-garuda fonts-tlwg-kinnari fonts-tlwg-loma fonts-tlwg-mono fonts-tlwg-norasi fonts-tlwg-purisa fonts-tlwg-sawasdee fonts-tlwg-typewriter fonts-tlwg-typist fonts-tlwg-typo fonts-tlwg-umpush fonts-tlwg-waree ttf-indic-fonts-core ttf-punjabi-fonts ttf-wqy-microhei fonts-kacst* fonts-khmeros* fonts-lklug-sinhala fonts-guru-extra fonts-nanum* fonts-noto-cjk fonts-takao* fonts-tibetan-machine fonts-lao fonts-sil-padauk fonts-sil-abyssinica fonts-tlwg-* fonts-lohit-* fonts-beng-extra fonts-gargi fonts-gubbi fonts-gujr-extra fonts-kalapi fonts-lohit-* fonts-samyak* fonts-navilu fonts-nakula fonts-orya-extra fonts-pagul fonts-sarai fonts-telu* fonts-wqy* fonts-smc* fonts-deva-extra
```

## Add Fonts

* Add custom fonts ~/.local/share/fonts
* Add bookmark to fonts in Nemo

```
sudo fc-cache -fv
```
```
sudo dpkg-reconfigure fontconfig
```
```
du -d 2 /usr/share/fonts
```


## Configure focuswriter theme

* Segoe UI @ 18
* text color: white
* backgrounds: #111
* space: 1.5
* Clear text background drop shadow toggle
* remove smart quotes

## Configure Freeplane

* Change Pref-> Appearance -> Look and Feel -> GTK+
* " Font-family -> Ubuntu
* Assign Hot Key -> New Child Node -> TAB
* View - Controls - Toolbar (uncheck)
* Toggle Display Status Lineage
* If don't have MM for template:  #54b443 text / #2d4130 bg
* Behavior -> Fold On Click Inside (uncheck)
* ...Edit Styles -> View -> View Settings -> Rectangular Selection


## App Setup

* Point gnucash
* configure Filezilla site manager for WWW and add bookmark for syncrhonized browsing
* Atom.io Pref -> Packages -> autocomplete-plus -> Settings -> Uncheck "Show Suggestions On Keystroke"
* Inkscape: Create default.svg to inches, page grid, 11x11


## Some Info Sources

* [https://easylinuxtipsproject.blogspot.com/p/1.html](https://easylinuxtipsproject.blogspot.com/p/1.html)
* [https://forums.linuxmint.com/viewtopic.php?t=286734](https://forums.linuxmint.com/viewtopic.php?t=286734)
* [(https://github.com/smurphos/Window_Borders_Mint_19](https://github.com/smurphos/Window_Borders_Mint_19)

## Deprecated

spotify-client

* Change Spotify shortcut to this:

Launcher: spotify -force-device-scale-factor=1.3

* Configure Spotify
