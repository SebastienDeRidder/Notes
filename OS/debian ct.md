# mount nfs drives on boot
```shell
apt install nfs-common
cat >> /etc/fstab << EOF
192.168.0.100:/mnt/ZFSA /mnt/ZFSA/ nfs auto 0 0
192.168.0.100:/mnt/ZFSB /mnt/ZFSB/ nfs auto 0 0
192.168.0.100:/mnt/4TB_SSD /mnt/4TB_SSD/ nfs auto 0 0
EOF
```

# enable gpu passthrough
1. follow [[proxmox#gpu-passthrough | gpu passthrough in proxmox]] first
2. change repository
   In order to enable gpu passthrough to the debian container, the container needs the same driver versions as the proxmox host. Therefore we remove the default repositories and add the same repositories as proxmox.
```shell
cat /dev/null > /etc/apt/sources.list
cat >> /etc/apt/sources.list << EOF
deb http://ftp.us.debian.org/debian bullseye main contrib non-free
deb http://ftp.us.debian.org/debian bullseye-updates main contrib non-free
deb http://security.debian.org bullseye-security main contrib non-free
deb http://ftp.us.debian.org/debian bullseye-backports main contrib non
free
deb http://download.proxmox.com/debian/pve bullseye pve-no-subscription
EOF
```
3. verify kernel version and available headers, these must be the same on proxmox and the container.
```shell
uname -r  
apt-cache search pve-header
```
4. on the proxmox host, run the following command to get the appropriate cgroups we will need. 
   `ls -l /dev/nvidia*`
   Take note of the 5th value that corresponds to nvidia-nvm(-tools) and the 5th value that corresponds to the other 3. In my case, it is 511 and 195 respectively.
5. add the following lines at the end of the container config file located at /etc/pve/lxc/{id}.conf :
```shell
# Allow cgroup access
lxc.cgroup.devices.allow: c 195:* rwm
lxc.cgroup.devices.allow: c 511:* rwm

# Pass through device files
lxc.mount.entry: /dev/nvidia0 dev/nvidia0 none bind,optional,create=file
lxc.mount.entry: /dev/nvidiactl dev/nvidiactl none bind,optional,create=file
lxc.mount.entry: /dev/nvidia-uvm dev/nvidia-uvm none bind,optional,create=file
lxc.mount.entry: /dev/nvidia-modeset dev/nvidia-modeset none bind,optional,create=file
lxc.mount.entry: /dev/nvidia-uvm-tools dev/nvidia-uvm-tools none bind,optional,create=file
```
5. install drivers: `apt install nvidia-driver -y`
6. press enter on the prompt and reboot container
7. verify if the gpu driver is working
```shell
nvidia-smi
```

# install docker
1. enable nesting: options > features > nesting
2. follow [[docker#install docker | docker installation]]