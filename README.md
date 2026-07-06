# alwj0 AutoExec - CS2 Configuration

A comprehensive and optimized Counter-Strike 2 configuration with useful scripts, documented commands, and professional settings.

> **Note:** This is a personalized fork/copy of [ArminC AutoExec](https://github.com/armync/ArminC-AutoExec), customized to my personal preferences and playstyle. The crosshair, sensitivity and viewmodel are tuned for competitive play, and the config has been **cleaned for CS2** (all removed CS:GO-era cvars stripped out).

> 🎯 **Want the full competitive setup?** The in-game **Video / NVIDIA panel settings** (1280×960 4:3 stretched, low graphics, Reflex, etc.) — which a `.cfg` alone can't set — are documented in the language guides below. Networking is left at the CS2 default on purpose (best hit registration).

## 📖 Documentation

Choose your language to view the installation and configuration guide:

- 🇺🇸 [English](README_EN.md)
- 🇪🇸 [Español](README_ES.md)

---

## ⚡ Quick Start

1. Download the latest version of the config
2. Extract the `cfg` folder contents to: `\...\Steam\steamapps\common\Counter-Strike Global Offensive\game\csgo\cfg\`
3. Launch the game and type in console: `exec autoexec.cfg`
4. Or use launch option: `+exec autoexec.cfg`

---

## ⌨️ Keyboard Layout

![Keyboard Layout](assets/keyboard_layout.png)

The configuration uses **scancodes** instead of key names for better compatibility across different keyboard layouts. Each key is bound using its physical position on the keyboard.

### Color Legend:

- 🔵 **Blue**: Default binds
- 🟠 **Orange**: Second binds (hold ALT or MOUSE5)
- 🟢 **Green**: Fast buy
- ⚪ **White**: No binds set
- 🩷 **Pink**: Scripts
- 🔴 **Red**: No binds allowed
- 🟡 **Yellow**: New placements & infrequent commands

---

## 🙏 Credits

This configuration is based on [ArminC AutoExec](https://github.com/armync/ArminC-AutoExec) by [@armync](https://github.com/armync). This repository is a personalized fork with custom modifications to suit my personal preferences and playstyle.

Original repository: [https://github.com/armync/ArminC-AutoExec](https://github.com/armync/ArminC-AutoExec)

---

## 📁 Structure

```
cfg/
├── autoexec.cfg          # Main configuration file
└── alwj0/
    ├── audio.cfg         # Audio settings
    ├── bind.cfg          # Key bindings
    ├── crosshair.cfg     # Crosshair configuration
    ├── hud.cfg           # HUD settings
    ├── mouse.cfg         # Mouse settings
    ├── network.cfg       # Network optimization
    ├── script.cfg        # Custom scripts
    └── video.cfg         # Video settings
```

---
