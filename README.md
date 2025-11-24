# ⚡ Gold Fastfetch Nvidia Config

A highly customized, performance-oriented **Fastfetch** configuration file (`config.jsonc`).
Designed for **Arch Linux / EndeavourOS** users with **Nvidia GPUs**, focusing on data density, visual hierarchy, and hardware monitoring accuracy.

![Preview](https://github.com/fastfetch-cli/fastfetch/raw/dev/doc/fastfetch.svg)
*(Replace this line with your own screenshot link later)*

## 🚀 Key Features

* **Nvidia Smi Bypass:** Uses `nvidia-smi` + `awk` to fetch real-time VRAM usage and Core Frequency, bypassing standard sensor limitations.
* **Storage Visuals:** Displays usage bars, percentage, and filesystem type (ext4/btrfs) for Root, Games, and Backup mounts.
* **Split Package Management:** Separates **Pacman**, **Flatpak**, and **AUR** counts (via `pacman -Qm`) for a cleaner software overview.
* **Gold Master Layout:**
    * **Header:** Cyan & Magenta styling.
    * **Hardware:** Green section with accurate memory/swap percentages.
    * **Misc:** Blue section including Local IP, Theme info, and the custom **Cursor** module.
* **Zero "Chartjunk":** Optimized format strings to remove redundant text while keeping essential data visible.

## 📦 Requirements

* **Fastfetch** (latest version recommended)
* **Nvidia Drivers** (with `nvidia-smi` available in PATH)
* **Nerd Font** (e.g., JetBrainsMono NF) for correct glyph rendering.
* `pacman` (for package counting logic).

## 📥 Installation

### Method 1: Manual Copy (Safe)
Backup your current config and copy the file:

```bash
mkdir -p ~/.config/fastfetch
cp config.jsonc ~/.config/fastfetch/config.jsonc
