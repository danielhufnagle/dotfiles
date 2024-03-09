# Dotfiles - Hyprland
Configuration for Hyprland by danielhufnagle
# Contents
- [Yapping](#Yapping)
- [Drag and Drop Install](#drag-and-drop-install)
- [Manual Install and Configuration (Fedora)](#manual-install-and-configuration-fedora)
- [Manual Install (Arch)](#manual-install-arch)
# Yapping
These are my dotfiles for my hyprland config. No, these do not install automatically. There are two install methods: the first is the "Drag and Drop Install" which is the generic install process of cloning the repo and then just moving the files to their appropriate locations. This is much simpler, but honestly I find that this is much less helpful for absolute beginners. The "Manual Install" will guide you step by step in configuring your system exactly the way that I have here. This should hopefully help you better learn how config files work and help you make your own. I'm using Fedora as a primary basis because I think it blends stability with having current software and is also a fairly beginner friendly distro. Also, it comes with GNOME by default which gives a nice fallback if you find this isn't for you.
# Drag and Drop Install
Run apply-dots.sh
(you may want to run install-deps-fedora.sh if you don't have dependencies installed)
# Manual Install and Configuration (Fedora)
## Install
### Getting Started and Basic Assumptions
I'm going to assume we are starting with a fresh install of Fedora Workstation. You don't have to, but that's where I'm starting.
### Installing Flatpak
Another package manager basically
```
sudo dnf install flatpak
```
### Installing Neofetch
You are not going to get any Reddit karma posting your rice on r/unixporn unless you have this
```
sudo dnf install neofetch
```
### Installing Neovim
I love neovim and you should too. This is the text editor that I'll be using primarily. You don't have to use this, but just know that whenever I call `nvim` you will have to replace it with your editor of choice
```
sudo dnf install neovim
```
### Extras for ASUS ROG Laptops (Skip if you don't use one)
I use an ASUS Zephyrus G14, which means that I have a laptop with a discrete GPU and other software utilities for things like fan profiles and keyboard backlight.
As a result, I will need to install this software.
You will need to install asusctl and supergfxctl and asusctl-rog-gui
To do this, follow the instructions from [this link](https://asus-linux.org/guides/fedora-guide/)
- A note for Arch users that wandered here: they also have a guide for arch as well
### Installing Auto CPUFreq (Laptop users only)
This software does one hell of a job when it comes to power optimization on laptops. Install instructions are [here](https://github.com/AdnanHodzic/auto-cpufreq). Use the installer script.
### Installing Docker
Not necessary, but I use it a lot. [Install](https://docs.docker.com/engine/install/fedora/).
### Installing Zsh and Oh-My-Zsh
Now we get back to things that actually affect the rice itself.
```
sudo dnf install zsh
sudo dnf install util-linux
chsh -s $(which zsh)
```
Then, you can restart your system (log back into the GNOME Session).
Now install Oh-My-Zsh to make Zsh look pretty.
```
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```
### Installing VS Code
Sometimes, I find neovim just isn't ideal for some projects (namely jupyter notebooks). [Install instructions](https://code.visualstudio.com/docs/setup/linux#_rhel-fedora-and-centos-based-distributions). To fix fractional scaling issues refer to [this reddit post](https://www.reddit.com/r/Fedora/comments/wpkws3/blurry_vscode_on_wayland_fractional_scaling/?rdt=60441&onetap_auto=true&one_tap=true)
### Installing Obsidian
This is how I take all of my notes these days. Install with flatpak.
```
flatpak install flathub md.obsidian.Obsidian
flatpak run md.obsidian.Obsidian
```
### Installing Anaconda
This is how I manage python environments. Very useful if you use Python in any capacity. [Install](https://docs.anaconda.com/free/anaconda/install/linux/)
### Installing Spotify and Spicetify
[Install Spotify](https://docs.fedoraproject.org/en-US/quick-docs/installing-spotify/). Use the flatpak install. [Install Spicetify](https://spicetify.app/docs/advanced-usage/installation/). Use the prebuilt binary shell install. You may have to run the command multiple times. Additionally, be aware of the extra instructions for the flatpak installed spotify.
### Installing Discord
This one is easy.
```
sudo dnf install discord
```
### Installing Wofi
Wofi is going to be our app launcher. Install is as follows:
```
sudo dnf install wofi
```
### Installing Waybar
This is our top bar that gives us a lot of information at a glance. Install is as follows:
```
sudo dnf install waybar
```
### Installing Hyprland
It's a simple as
```
sudo dnf install hyprland
```
### Installing Swaybg
Also simple
```
sudo dnf install swaybg
```
### Installing Network Manager Applet
Another simple onw
```
sudo dnf install network-manager-applet
```
## Configuration
This is the fun (and difficult) part
# Manual Install (Arch)
You use arch. Ffs you should be able to do this. Follow the fedora instructions except adjust the package manager
