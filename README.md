# ⚡ Gold Fastfetch Nvidia Config
A highly customized, performance-oriented **Fastfetch** configuration file (`fastfetch.jsonc`).
Designed for **Arch Linux / EndeavourOS** users with **Nvidia GPUs**, focusing on data density, visual hierarchy, and hardware monitoring accuracy.

![Preview](https://github.com/fastfetch-cli/fastfetch/raw/dev/doc/fastfetch.svg)

*(Replace this line with your own screenshot later.)*

---

## 🚀 Key Features
- **Nvidia SMI-based monitoring:** Uses `nvidia-smi` + `awk` to fetch real-time VRAM usage and core frequency, bypassing standard sensor limitations.
- **Storage visuals:** Displays usage bars, percentage and filesystem type (ext4/btrfs) for Root, Games and Backup mounts.
- **Split package management:** Separates **Pacman**, **Flatpak** and **AUR** counts (via `pacman -Qm`) for a cleaner software overview.
- **Gold master layout:**
  - **Header:** Cyan & magenta styling.
  - **Hardware:** Green section with accurate memory/swap percentages.
  - **Misc:** Blue section including local IP, theme info and the custom **Cursor** module.
- **Zero "chartjunk":** Optimized format strings to remove redundant text while keeping essential data visible.

---

## 📦 Requirements
- **Fastfetch** (latest version recommended)
- **Nvidia drivers** (with `nvidia-smi` available in `PATH`)
- A **Nerd Font** (e.g. *JetBrainsMono Nerd Font*) for correct glyph rendering
- `pacman` (for package counting logic)

---

## 📥 Installation
### Method 1: Manual copy (recommended)
This is the safest method. It creates a standalone copy of the config.

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Lucenx9/Gold-Fastfetch-Nvidia.git
   cd Gold-Fastfetch-Nvidia
   ```

2. **Back up your existing config (if any):**
   ```bash
   mv ~/.config/fastfetch/config.jsonc ~/.config/fastfetch/config.jsonc.bak 2>/dev/null
   ```

3. **Install the new config:**
   ```bash
   mkdir -p ~/.config/fastfetch
   # We rename fastfetch.jsonc to config.jsonc during the copy
   cp fastfetch.jsonc ~/.config/fastfetch/config.jsonc
   ```

### Method 2: Symlink (for dotfiles managers)
Advanced users can link the file directly to receive updates via git pull.
```bash
ln -sf ~/path/to/Gold-Fastfetch-Nvidia/fastfetch.jsonc ~/.config/fastfetch/config.jsonc
```

---

## 🔧 Customization Notes
### Disk mounts
The config is hardcoded for a specific mount setup.
Edit the disk modules in fastfetch.jsonc to match your lsblk / actual mount points:
```json
// Change "/mnt/games" to your actual mount point
{
  "type": "disk",
  "key": "│ 󰋊 Games",
  "folders": "/mnt/games",
  ...
}
```
Repeat the same pattern for your Root, Backup or any additional custom mounts.

---

## 📜 License
Unlicense / Public Domain.
Feel free to fork, modify and steal parts of this config for your own setup.
Feel free to open an issue or PR if you want to extend support to other distros, layouts or GPU vendors.


