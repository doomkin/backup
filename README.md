# backup
Simple bash scripts to backup and restore partitions. To backup current operation system reboot to another operation system. For example into [Arch](https://www.archlinux.org/download/) USB flash drive.

## Backup

`sudo ./backup sda3`

Creates `label.tar.gz`, where `label` is label of selected partition.

## Restore

`sudo ./restore sda3 label.tar.gz`

Formats selected partition to `ext4` and writes content of `label.tar.gz` with new partition `label`.

## Dependance

Install multi core archiver `pigz`

### Debian

`sudo apt install pigz -y`

### Centos

`sudo yum install pigz -y`

### Arch

`sudo pacman -Sy --noconfirm pigz`
