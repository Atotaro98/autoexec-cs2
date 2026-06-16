# alwj0 AutoExec - CS2 Configuration (English)

A comprehensive and optimized Counter-Strike 2 configuration with useful scripts, documented commands, and professional settings.

> **Note:** This is a personalized fork/copy of [ArminC AutoExec](https://github.com/armync/ArminC-AutoExec), customized to my personal preferences and playstyle. Some `.cfg` files have been modified according to my needs.

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

- **The crosshair, sensitivity and viewmodel follow [donk](https://prosettings.net/players/donk)'s pro setup.** The crosshair is tuned for **1280x960 (4:3 _stretched_)**, which is the setup's resolution. On other resolutions/aspect ratios the size/gap will look different — you may want to retune `cl_crosshairsize` and `cl_crosshairgap`.

- **CS2-clean only:** legacy CS:GO commands that no longer exist in CS2 were removed (`cl_interp`, `cl_interp_ratio`, `cl_cmdrate`, `cl_updaterate`, `m_rawinput`, `cl_bob*`, `net_graph`...). **Do not re-add them** — they throw _"Unknown command"_ on every launch.

## 🎯 Settings that do NOT live in the .cfg (menu + GPU panel) — donk-style

> ⚠️ **This matters.** An autoexec **cannot reliably set resolution or graphics quality** (CS2 stores those in the menu settings). For the full competitive setup, configure them **by hand** in-game and in your GPU control panel.

### 🖥️ Video (Settings → Video)

| Setting | Value (donk) |
| --- | --- |
| Resolution | **1280 × 960** |
| Aspect Ratio | **4:3** |
| Scaling Mode | **Stretched** |
| Brightness | 93% |
| Display Mode | Fullscreen |

### ⚙️ Advanced Video

| Setting | Value (donk) |
| --- | --- |
| Boost Player Contrast | **Enabled** |
| Wait for Vertical Sync | Disabled |
| NVIDIA Reflex Low Latency | Disabled* |
| Multisampling AA Mode | 8x MSAA |
| Global Shadow Quality | High |
| Dynamic Shadows | All |
| Model / Texture Detail | **Low** |
| Texture Filtering Mode | Bilinear |
| Shader Detail | **Low** |
| Particle Detail | **Low** |
| Ambient Occlusion | Disabled |
| High Dynamic Range | Quality |
| FidelityFX Super Resolution | Disabled (Highest Quality) |

> *\*Reflex is **contested** in 2026: donk runs it **Off**. The tested low-latency route for (CPU-bound) CS2 is Reflex Off + `-noreflex` launch option + "Low Latency Mode = Ultra" in the NVIDIA panel. **Don't mix** in-game Reflex On with `-noreflex` — pick one.*

### 🟩 NVIDIA Control Panel (for 4:3 _stretched_ + low latency)

- **Adjust desktop size and position → Scaling:** `Full-screen`, **Perform scaling on: GPU**, and tick **"Override the scaling mode set by games"**. _(Without this, 4:3 shows black bars instead of stretching.)_
- **Manage 3D settings (for cs2.exe):** Low Latency Mode **Ultra** (Reflex Off) / **On** (Reflex On); Power management **Prefer maximum performance**; Vertical sync **Off**; Preferred refresh rate **Highest available**.
- **AMD (Radeon):** equivalent under _Display → GPU Scaling + Scaling Mode: Full Panel_, and enable _Radeon Anti-Lag_.

### 🚀 Launch options

donk **uses none**. Optional: `-noreflex` (only for the no-Reflex low-latency route) and `-w 1280 -h 960` (force resolution if the menu ignores it).

## 🌐 Networking & Ping (`netmode` toggle on F9)

CS2 **no longer has** `cl_interp`/`cl_cmdrate`/`cl_updaterate`. The only real network knob is **`cl_net_buffer_ticks`**, and it depends on **timing variance (jitter)** — which exists on long-distance/VPN links **even when loss reads 0**.

- There's **a single `network.cfg`** with `rate 786432` + `cl_net_buffer_ticks 0` (lowest delay, ideal for your low local ping).
- **`netmode` (F9)** flips between two modes:
  - **LOW-PING (default):** buffer 0 → lowest delay. For a stable local link.
  - **HIGH-PING:** buffer 1 (+queue 2) + hit prediction → gives a cushion so your usercommands arrive on time and **fixes "bullets don't register / no damage"** at ~100ms+. If 1 still feels off, try `cl_net_buffer_ticks 2`.

> On **high ping (VPN to another continent)** turn **HIGH-PING (F9)** ON even with 0 loss: jitter makes your shots arrive mistimed so the server registers them poorly. On your **local Madrid game**, keep it **LOW-PING**.

## 🧠 Sensitivity / eDPI

| | DPI | Sens | eDPI |
| --- | --- | --- | --- |
| This config | 800 | **0.8** | **640** |
| donk | 800 | 1.25 | 1000 |

640 eDPI is a bit lower (more control/precision, less flick) — well within pro range, but it's a **personal choice**. Edit `mouse.cfg` if you'd rather match donk.

## ⚠️ CS2 gotchas (2026)

- **The in-game menu overrides the autoexec.** Changing a value in Settings makes CS2 save it and overwrite the .cfg next launch. For file values, **edit the .cfg, not the menu**.
- **`host_writeconfig`** (last line of the autoexec) is still valid, but CS2 auto-saves binds anyway; if something won't persist, check Steam Cloud.
- **Steam Cloud** can overwrite/delete your files — consider disabling Cloud for CS2 if you hand-edit.
- **Legal scripts:** this config uses **no** null-binds / automated counter-strafe (those get you kicked for "Input Automation" since Aug 2024). The jumpthrow is manual and scroll-wheel bhop is normal input → all legal in official MM.

## 🎯 Crosshair code

Import the crosshair directly in **CS2 → Settings → Game → Crosshair → _Share or Import_ → paste the code → _Import_**:

```
CSGO-TaM3Q-GFU5p-J4Mtu-bSqZw-vyJzN
```

> This is donk's **official (green)** crosshair. This repo uses **the same shape in cyan** (`cl_crosshaircolor_R 0 / G 255 / B 255`). Importing donk's code switches it to **green** and, since the menu overrides the autoexec, it sticks; to keep cyan don't import it (it already ships in `crosshair.cfg`) or set `cl_crosshaircolor_B 255` again.

## ✅ How to verify it loads correctly

1. Open the console (`` ` `` key) and run `exec autoexec.cfg`. You should hear the confirmation beep at the end.
2. **Look for red `Unknown command "xxx"` lines.** This config **should throw none** (that's why the CS:GO cvars were stripped). If one appears, that command is the culprit.
3. **Check values** by typing the cvar **without a value** (it prints the current one):

   | Command | Should show |
   | --- | --- |
   | `sensitivity` | `0.8` |
   | `cl_crosshairstyle` | `4` |
   | `cl_net_buffer_ticks` | `0` |
   | `rate` | `786432` |
   | `fps_max` | `600` |

4. In-game, type `status`: check **your row** (ping / loss / rate). If `loss` stays at `0`, leave `netmode` **OFF**.
5. Press **F9** to toggle `netmode`: you'll see `[NET] buffer ON` / `[NET] buffer OFF` in console.

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

## 🙏 Credits

This configuration is based on [ArminC AutoExec](https://github.com/armync/ArminC-AutoExec) by [@armync](https://github.com/armync). This repository is a personalized fork with custom modifications to suit my personal preferences and playstyle.

Original repository: [https://github.com/armync/ArminC-AutoExec](https://github.com/armync/ArminC-AutoExec)


