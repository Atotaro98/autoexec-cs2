# alwj0 AutoExec - CS2 Configuration (English)

A comprehensive and optimized Counter-Strike 2 configuration with useful scripts, documented commands, and professional settings.

## 📥 Installation

### Downloading and Installing Steps:

1. **Download the latest version** of the config from the repository.

2. **Extract the contents:**
   - Open the archive and extract the contents of the `cfg` folder
   - Copy all files to the following path:
     ```
     \...\Steam\steamapps\common\Counter-Strike Global Offensive\game\csgo\cfg\
     ```

3. **Launch the game** and type in the console:
   ```
   exec autoexec.cfg
   ```

4. **If the autoexec isn't booting**, try using the launch option:
   ```
   +exec autoexec.cfg
   ```

5. **For a new desktop or operating system** (e.g. Linux):
   - Make sure to put (again) in place all the files
   - Do not let the Steam cloud transfer them automatically

## ⚠️ Important

- **The binds system has changed.** Instead of using the name of the key, there are **scancodes assigned per key**. This ensures compatibility across different keyboard layouts and languages.

- **The crosshair is designed for a 1920x1080 resolution;** in other cases, the experience may vary.

## 🔄 Updating

When a new version is out, you have two methods to update:

### Method 1: You have edited the config based on your preference
- Check the new commits and update the config manually by relying on the commits.
- This preserves your customizations.

### Method 2: You haven't edited the config (or at least not so much)
- Delete everything (or replace the files when it asks).
- Redo the installation steps.
- After setup, change your preference settings back (if that is the case).

## ⌨️ Binds

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

### Key Features:
- **Second binds**: Hold ALT or MOUSE5 to access secondary functions
- **Scripts**: Custom functionality for various game scenarios
- **Fast buy**: Quick purchase bindings
- **Organized categories**: Binds are categorized by function

For detailed bind information, check the [alwj0 AutoExec Binds](https://github.com/alwj0-AutoExec/wiki/Binds) wiki page.

## 📁 Configuration Files

The config is organized into multiple files for easy customization:

- **autoexec.cfg**: Main file that executes all other configurations
- **alwj0/audio.cfg**: Audio settings and sound optimization
- **alwj0/bind.cfg**: All key bindings using scancodes
- **alwj0/crosshair.cfg**: Crosshair configuration
- **alwj0/hud.cfg**: HUD elements and layout
- **alwj0/mouse.cfg**: Mouse sensitivity and settings
- **alwj0/network.cfg**: Network optimization settings
- **alwj0/script.cfg**: Custom scripts and automation
- **alwj0/video.cfg**: Video and graphics settings


