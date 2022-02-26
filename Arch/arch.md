## Pacman

```
sudo pacman -S --noconfirm nvidia-utils nvidia-settings nodejs npm steam neofetch docker zsh firefox bleachbit kaffeine virtualbox obs-studio clamav thunderbird appmenu-gtk-module lnav
```

## Yay

```
yay -S glmark2 visual-studio-code-bin authy slack-desktop zsh-theme-powerlevel10k-git google-chrome stacer qtkeychain gnome-keyring insomnia bitwarden-bin zoom brave-bin songrec
```

## Codecs

```
sudo pacman -S --noconfirm gstreamer gst-plugins-bad gst-plugins-base gst-plugins-base-libs gst-plugins-good gst-plugins-ugly xine-lib libdvdcss libdvdread dvd+rw-tools vlc lame
```

## Start services docker

```
sudo systemctl enable docker && sudo usermod -aG docker kuro && sudo systemctl start docker
```

### Docker-compose

```
sudo pacman -S python-pip
sudo pip install docker-compose
o
sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose

sudo chmod +x /usr/local/bin/docker-compose
```

## Zsh plugins

```
echo 'source /usr/share/zsh-theme-powerlevel10k/powerlevel10k.zsh-theme' >>! ~/.zshrc
yay -S zsh-syntax-highlighting-git
sudo pacman -S zsh-autosuggestions bat
```

### default shell

```sh
chsh -s $(which zsh)
```

### OBS virtual-cam

virtual cam for zoom,meets etc:

```
yay -S v4l2loopback-dkms
yay -S obs-v4l2sink
```

output:

```sh
sudo modprobe v4l2loopback video_nr=7 card_label="obs-studio"
```

go to settings
obs -> tools-> v4l2sink -> video7

### VIDEO WALLPAPPER

```
yay -S komorebi
fix missing file video:
sudo pacman -S gst-libav
```

### extra

```
yay -S davinci-resolve-beta
```

ffmpeg -i titan.mov -c:v libx264 -preset ultrafast -crf 0 titan1.mp4
ffmpeg -i zerotwo.mp4 -vcodec mjpeg -q:v 2 -acodec pcm_s16be -q:a 0 -f mov zerotwo.mov

### Gamer tools

```sh
sudo pacman -S glslang vulkan-tools lib32-libx11 libx11 meson

yay -S goverlay mangohud lib32-mangohud vkbasalt lib32-vkbasalt
```
