## My Dotfiles and System Configurations
Hello to my repo that have dotfiles. currently the repo focuses on **Nixos**, and It can be expanded to include other systems and tools.

### Repository Structure
```
.
|- nixos/
|    |- configuration.nix
```
**Note**: The hardware-configuration.nix file is not included because it depends entirely on your hardware. Be sure to keep your original file.

### NixOS Config Highlights
These are the main features and settings found in the current **configuration.nix**.
**DE**: *KDE Plasma 6* via *SDDM*
**Sound and Graphics**: Activated using *PipeWire*, with full support for *intel* graphics drivers (Intel VAAPI/Media Drivers) and support for 32-bit game packages.
**Dev tool**: GCC, Make, QtCreator, SDL3, Git
**Games and Compatibility**: Wine, Bottles, Steam-run, Appimage-run
**System Maintenance**: Weekly Automated Garbage Collector

## Installation
**⚠️ Warning:** Do not blindly copy these settings. Recommended to review the settings to ensure compatibility. It is assumed that you know what you are doing before you use the file.
### To apply NixOS settings:
1. Clone the repo
```bash
git clone https://github.com/floweysensie/My-Dotfiles-and-System-Configurations.git
cd My-Dotfiles-and-System-Configurations
```
2. Move the files to the system directory
```bash
# Backup your current configuration just in case
sudo cp /etc/nixos/configuration.nix /etc/nixos/configuration.nix.bak

# Copy the new configuration
sudo cp nixos/configuration.nix /etc/nixos/configuration.nix
```
3. Build the system and update it
```bash
sudo nixos-rebuild switch
```
and done
