# Logiops Configuration for Logitech MX Master 3S

## Overview
This document describes the keybindings and configuration settings for the Logitech MX Master 3S mouse using Logiops on Linux.

## Configuration File Location
```
/etc/logid.cfg
```

## Device Settings
- **Device Name:** MX Master 3S
- **DPI:** 1600 (Max: 4000)
- **SmartShift:** Enabled (Threshold: 15)
- **Hi-Res Scroll:** Enabled (No Inversion, No Targeting)
- **Thumb Wheel:** Diverted, No Inversion, Tap Action (Mic Mute)

## Button Mappings
### Forward Button (cid: 0x56)
| Gesture | Mode | Action |
|----------|--------|--------------------------------|
| None | OnRelease | `KEY_FORWARD` |
| Up | OnRelease | `KEY_PLAYPAUSE` |
| Down | OnRelease | `KEY_MUTE` |
| Right | OnRelease | `KEY_NEXTSONG` |
| Left | OnRelease | `KEY_PREVIOUSSONG` |

### Back Button (cid: 0x53)
| Gesture | Mode | Action |
|----------|--------|--------------------------------|
| None | OnRelease | `KEY_BACK` |
| Up | OnRelease | `KEY_VOLUMEUP` |
| Down | OnRelease | `KEY_VOLUMEDOWN` |

### Gesture Button (cid: 0xc3)
| Gesture | Mode | Action |
|----------|--------|--------------------------------|
| None | OnRelease | `KEY_LEFTMETA` (Open Activities Overview) |
| Right | OnRelease | `KEY_LEFTMETA + KEY_PAGEDOWN` (Snap Window Right) |
| Left | OnRelease | `KEY_LEFTMETA + KEY_PAGEUP` (Snap Window Left) |
| Up | OnRelease | `KEY_LEFTMETA + KEY_UP` (Maximize Window) |
| Down | OnRelease | `KEY_LEFTMETA + KEY_DOWN` (Minimize Window) |

### Top Button (cid: 0xc4)
| Gesture | Mode | Action |
|----------|--------|--------------------------------|
| None | OnRelease | Toggle SmartShift |
| Up | OnRelease | Increase DPI by 400 |
| Down | OnRelease | Decrease DPI by 400 |

## Notes
- This configuration enables advanced gestures for better productivity.
- The gesture button allows window management shortcuts using the `Super` (Meta) key.
- DPI adjustments are available via the top button.

## Installation & Usage
### Debian/Ubuntu
1. Install `logiops`:
   ```
   sudo apt install logiops
   ```

### Arch Linux
1. Install `logiops` from AUR:
   ```
   yay -S logiops
   ```
   or manually using:
   ```
   git clone https://aur.archlinux.org/logiops.git
   cd logiops
   makepkg -si
   ```

### Fedora
1. Install `logiops`:
   ```
   sudo dnf install logiops
   ```

### OpenSUSE
1. Install `logiops`:
   ```
   sudo zypper install logiops
   ```

### Configuration
2. Edit the configuration file:
   ```
   sudo nano /etc/logid.cfg
   ```

3. Restart the Logiops service:
   ```
   sudo systemctl restart logid
   ```

