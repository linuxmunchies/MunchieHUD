MangoHud Dotfiles  
===============  

A collection of preconfigured MangoHud settings, presets and keybinds to get up and running quickly on any Linux distribution.  

## Features  
- Four ready-to-use HUD presets for different layouts and metrics  
- Custom keybinds for toggling HUD, logging and FPS limit on the fly  
- Cross-distro installation guide for MangoHud  
- Sample `presets.conf` and `MangoHud.conf` kept under version control  

## Installation  

**1. Install MangoHud**  
Choose your distribution and run the corresponding command:

-  Arch Linux
  ```bash
  sudo pacman -S mangohud lib32-mangohud
  ```
  (Available in `extra` / `multilib` repositories)  

-  Debian 12 / Ubuntu 24.10+  
  ```bash
  sudo apt install mangohud
  ```
  (Optional 32-bit support: `sudo apt install mangohud:i386` on Debian)  

-  Fedora  
  ```bash
  sudo dnf install mangohud
  ```
  (Official package in Fedora repos)


-  openSUSE Leap/Tumbleweed  
  ```bash
  sudo zypper in mangohud mangohud-32bit
  ```
  (Both 64-bit and 32-bit packages required on 64-bit OS)  

**2. Clone this repo & deploy configs**  
```bash
git clone https://github.com/yourusername/mangohud-dotfiles.git ~/mangohud-dotfiles
mkdir -p ~/.config/MangoHud
ln -sf ~/mangohud-dotfiles/presets.conf ~/.config/MangoHud/presets.conf
ln -sf ~/mangohud-dotfiles/MangoHud.conf  ~/.config/MangoHud/MangoHud.conf
```

## Usage  

**Running games with MangoHud**  

- Steam (per-game launch option):  
  ```
  mangohud %command%
  ```


**Selecting presets**  
Set `presets=` in `~/.config/MangoHud/MangoHud.conf` to one or more preset IDs (e.g. `presets=1,3`).  

## Keybinds  

You can customize these in `~/.config/MangoHud/MangoHud.conf`. Defaults are:  

-  **Shift + F12** → Toggle the HUD on/off[6]  
-  **Shift + F11** → Toggle logging mode[6]  
-  **Shift + F10** → Toggle FPS limit (if enabled in config)  
-  **Shift + F9**  → Upload the last log to flightlessmango.com  

## Configuration  

All options live in `~/.config/MangoHud/MangoHud.conf`. Key sections include:  
- `presets=` – Comma-separated list of presets  
- `toggle_hud=` – Keybind for HUD toggle  
- `toggle_logging=` – Keybind for logging  
- `fps_limit=` and `toggle_fps_limit=` – FPS cap and keybind  
- Visual settings (font_size, background_alpha, position, colors)  

Refer to the upstream example for a full list of options: see `MangoHud.conf.example` in the MangoHud repo.  

## License  

This dotfiles collection is distributed under the MIT License.  
Feel free to fork and adapt to your own workflow.