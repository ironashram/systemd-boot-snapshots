# File: CHANGELOG.md
# Project Path: ./CHANGELOG.md
# Installation Path: /usr/share/doc/systemd-boot-snapshots/CHANGELOG.md
#
# Version history for systemd-boot-snapshots

# Changelog

All notable changes to the systemd-boot-snapshots project will be documented in this file.

## [0.2.2] - 2025-11-20
### Fixed
 - Fix integer validation

## [0.2.1] - 2025-11-20
### Fixed
 - Fixed kernel detection if /boot is fat32 and not in btrfs snapshots

## [0.1.1] - 2025-04-23

### Added
- Support for reading configuration from both `/etc/systemd-boot-snapshots.conf` and `/etc/default/systemd-boot-snapshots.conf`
- Automatic detection of EFI partition mount point (supports /boot/efi, /boot, and /efi)
- Automatic detection of Timeshift and Snapper snapshot paths
- Automatic copying of configuration from /etc/default to /etc on installation or update

### Fixed
- Fixed path assumptions for different Arch Linux configurations
- Better handling of snapshot tool detection and initialization
- Improved error handling when EFI partition or snapshots are not found

## [0.1.0] - 2025-04-22

### Added
- Initial release for Arch Linux
- Support for both mkinitcpio (Arch Linux) and dracut (EndeavourOS, Garuda Linux)
- Automatic detection of BTRFS snapshots from Timeshift and Snapper
- Automatic addition of snapshots to systemd-boot menu
- Desktop notifications when booting into a snapshot
- Automatic overlay configuration for snapshot protection
- Automatic mounting of kernel modules from parent volume when needed
- Path monitors for detecting new snapshots
- AUR package support

### Changed
- Adapted from the original Ubuntu/Fedora implementation
- Restructured to follow Arch Linux paths and conventions
- Removed initramfs-tools dependencies
- Added support for multiple notification systems for Arch desktop environments

### Fixed
- Correct handling of systemd paths for Arch Linux
- Proper detection of boot partition path
- Safe handling of read-only snapshots

## [0.0.1] - 2023-07-22

### Added
- Original implementation for Ubuntu by Usarin Heininga
