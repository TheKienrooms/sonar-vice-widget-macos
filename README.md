# Sonar Vice Widget (macOS)

A modern, always-on-top desktop widget for **SteelSeries GG** — control Sonar audio, EQ profiles, and RGB lighting from a compact floating panel. macOS compatible version.

![Python](https://img.shields.io/badge/Python-3.10+-blue?logo=python)
![Platform](https://img.shields.io/badge/Platform-macOS-000000?logo=apple)
![License](https://img.shields.io/badge/License-MIT-green)

## Features

- **Audio Controls** — Volume sliders, mute toggles, and device routing for all Sonar channels (Master, Game, Chat, Media, Aux, Mic)
- **ChatMix** — Hardware-synced Game/Chat balance control
- **EQ Profiles** — Switch between favorite and all EQ presets per device
- **RGB Lighting** — Control SteelSeries device colors via GameSense with presets and custom RGB
- **System Tray** — Hide/show widget, always-on-top toggle, restart, and quit from tray icon
- **Theme Switcher** — SteelSeries (orange) and Sonar Dark (teal) themes with live switching
- **Modern UI** — Borderless, draggable, rounded corners, no taskbar entry

## Requirements

- **macOS 11+**
- **SteelSeries GG** installed and running
- **Python 3.10+** (for running from source)

## Quick Start

### Option 1: Run from Source

```bash
# Clone the repository
git clone https://github.com/kingpin1dev/sonar-vice-widget-macos.git
cd sonar-vice-widget-macos

# Install dependencies
pip install -r requirements.txt

# Run
python3 main.py
```

### Option 2: Build .app

```bash
chmod +x build.sh
./build.sh
```

The built app will be in `dist/SonarViceWidget`.

## Project Structure

```
sonar-vice-widget-macos/
  main.py              # Entry point
  config.py            # Configuration constants
  requirements.txt     # Python dependencies
  build.sh             # macOS .app build script
  gen_icon.py          # Icon generator
  api/
    discovery.py       # SteelSeries GG API discovery
    sonar_client.py    # Sonar volume/mute controls
    sonar_presets.py   # EQ profile management
    sonar_devices.py   # Audio device routing
    gamesense_client.py # GameSense RGB control
    device_client.py   # Device battery/info (WebSocket)
  ui/
    widget.py          # Main widget window
    audio_panel.py     # Audio controls panel
    eq_panel.py        # EQ profiles panel
    rgb_panel.py       # RGB lighting panel
    styles.py          # Theme system
    tray.py            # System tray integration
```

## Screenshots

*Coming soon*

## License

MIT License - Made by **Kingpindev**
