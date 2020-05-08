# backup
Simple bash scripts to backup and restore partitions. To backup current operation system reboot to another operation system. For example into [Arch](https://www.archlinux.org/download/) USB flash drive.

## Backup

`sudo ./backup sda3 [subvol]`

Creates `label.tar.gz` with `label` of selected partition or of btrfs `subvol` if it present.

## Restore

`sudo ./restore sda3 label.tar.gz [subvol]`

Formats selected partition to ext4 or recreate btrfs `subvol` if it present, then writes content of `label.tar.gz`.

## Recreate btrfs subvolume

`sudo ./recreate-subvol sda3 subvol`

Recreates btrfs `subvol` on selected partition.

## Dependance

Install multi core archiver `pigz`

### Debian

`sudo apt install pigz -y`

### Centos

`sudo yum install pigz -y`

### Arch

`sudo pacman -Sy --noconfirm pigz`
