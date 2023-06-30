# Installation
## networking
### connect to wifi
- `iwctl`
- `device list`
- `device {Name} set-property Powered on`
- `station {Name} scan`
- `station {Name} get-networks`
- `station {Name} connect {SSID}`
- `device {Name} show`
- `station {Name} show`
- `known-networks list`

### enterprise network
https://wiki.archlinux.org/title/Iwd#iwctl
3.2

### set static ip
- set relevant values: for ip configuration
- `echo -e "[IPv4]\nAddress=192.168.1.10\nNetmask=255.255.255.0\nGateway=192.168.1.1\nBroadcast=192.168.1.255\nDNS=192.168.1.1" >> /var/lib/iwd/{SSID}.psk`

## set timezone
- `nano /etc/systemd/timesyncd.conf`
- uncomment NTP=
- add the correct time-server from [this website](https://www.ntppool.org/zone/europe)

## partition disk
- `lsblk`
- `cfdisk /dev/{disk}`
- select 'gpt'
- 'new' > enter '16G' with type 'swap'
- 'new' > enter '300M' with type 'EFI system'
- 'new' > leave default to use remaining disk space
- 'write'
- 'quit'
- `mkfs.fat -F 32 /dev/{partition1}`
- `mkswap /dev/{partition2}`
- `mkfs.ext4 /dev/{partition3}`
- `mount /dev/{partition3} /mnt`
- `mkdir /mnt/boot`
- `mkdir /mnt/boot/efi`
- `mount /dev/{partition1} /mnt/boot/efi`
- `swapon /dev/{partition2}`

## further configuration
- `pacstrap /mnt base base-devel linux linux-firmware vim nano`
- `genfstab -U /mnt >> /mnt/etc/fstab`
- `arch-chroot /mnt /bin/bash`
- `pacman -S NetworkManager grub efibootmgr`
- `systemctl enable NetworkManager`
- `grub-install /dev/{partition1}`
- `grub-mkconfig -o /boot/grub/grub.cfg`
- `passwd`
- `nano /etc/locale.gen`
- uncomment both 'en_US'
- `locale.gen`
- `echo "LANG=en_US.UTF-8" >> /etc/locale.conf`
- `echo {hostname} >> /etc/hostname`
- `ln -sf /usr/share/zoneinfo/Europe/Brussels /etc/localtime`
- `exit`

