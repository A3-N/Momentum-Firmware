# BornFree Firmware

A lightweight Flipper Zero firmware, derived from the Momentum firmware. All non-essential desktop animations, themes, and asset packs have been removed to preserve storage space and maintain a minimalistic build, while retaining the full suite of included applications and modules.

## Compilation & Installation

This project utilizes the Flipper Build Tool (`fbt`) to handle all dependencies and compiling.

### Prerequisites
* You must have an active internet connection the first time so `fbt` can download the ARM toolchain.
* Close `qFlipper` (and any other serial terminal) before attempting to flash directly over USB.

### Quick Start Commands

Run these from the root directory of the repository:

**1. Flash Directly over USB**
Compiles the firmware and immediately flashes it to your connected Flipper Zero.
```bash
./fbt flash_usb_full
```

**2. Compile a Standalone Update Package**
Generates a `.tgz` firmware update package inside the `dist/` folder. You can drag and drop this file into qFlipper, or move it to your SD card's `update/` folder to install on the go.
```bash
./fbt updater_package
```

**3. Test a Single Application**
To save time while developing or tweaking an individual app, you can compile and launch it isolated:
```bash
./fbt launch APPSRC=<your_app_id>
```
*(e.g. `./fbt launch APPSRC=momentum_app`)*
