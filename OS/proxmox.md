# change proxmox repository
1. `nano /etc/apt/sources.list`
2. add the following line:
```shell
deb http://download.proxmox.com/debian/pve bullseye pve-no-subscription
```
3. ctrl + o > ctrl + x
4. `nano /etc/apt/sources.list.d/pve-enterprise.list`
5. comment out the line in this file
6. ctrl + o > ctrl + x
7. run [[scripts#updater.sh | update script]]
	
# install dark/discord theme
```shell
bash <(curl -s https://raw.githubusercontent.com/Weilbyte/PVEDiscordDark/master/PVEDiscordDark.sh ) install
```

# display temps on summary page
1. `apt-get install lm-sensors`
2. `nano /usr/share/perl5/PVE/API2/Nodes.pm`
3. ctrl + w > my $dinfo
4. paste following line before my $dinfo:
```shell
$res->{thermalstate} = `sensors`;
```
5. ctrl + o > ctrl + x
6. `nano /usr/share/pve-manager/js/pvemanagerlib.js`
7. ctrl + w > widget.pveNodeStatus
8. change height to `350` and bodyPadding to `'20 15 20 15'`
9. ctrl + w > PVE Manager Version
10. after
```shell
		{
            itemId: 'version',
            colspan: 2,
            printBar: false,
            title: gettext('PVE Manager Version'),
            textField: 'pveversion',
            value: '',
        },
```
paste
```shell
        {
            itemId: 'thermal',
            colspan: 2,
            printBar: false,
            title: gettext('CPU Thermal State'),
            textField: 'thermalstate',
            renderer:function(value){
                const c0 = value.match(/Package id 1.*?\+([\d\.]+)Â/)[1];
                const c1 = value.match(/Package id 0.*?\+([\d\.]+)Â/)[1];
                const c2 = value.match(/temp1.*?\+([\d\.]+)Â/)[1];
                return `CPU 1: ${c0} ℃ | CPU 2: ${c1} ℃ | GPU: ${c2} ℃`
            },
        },
```
This part reads out the temps of both cpu's and gpu in my system and displays them in real time on the summary page.
11. ctrl + o > ctrl + x
12. finally, reload pveproxy: `systemctl restart pveproxy`

# gpu-passthrough
1. download nvidia drivers:
```shell
apt install nvidia-driver
```
2. load nvidia drivers on boot
```shell
cat >> /etc/modules-load.d/modules.conf << EOF
# Nvidia modules
nvidia
nvidia_uvm
EOF
```
3. `update-initramfs -u -k all`
4. add udev rule to create required device files for the nvidia driver.
```shell
cat /dev/null > /etc/apt/sources.list
cat >> /etc/udev/rules.d/70-nvidia.rules << EOF
KERNEL=="nvidia", RUN+="/bin/bash -c '/usr/bin/nvidia-smi -L && /bin/chmod 666 /dev/nvidia*'"
KERNEL=="nvidia_modeset", RUN+="/bin/bash -c '/usr/bin/nvidia-modprobe -c0 -m && /bin/chmod 666 /dev/nvidia-modeset*'"
KERNEL=="nvidia_uvm", RUN+="/bin/bash -c '/usr/bin/nvidia-modprobe -c0 -u && /bin/chmod 666 /dev/nvidia-uvm*'"
EOF
```
5. reboot and verify if the gpu driver is working
```shell
nvidia-smi
```
# force shutdown container
 if [[scripts#ct-restart.sh||restart script]] doesn't work, kill the container process
 1. `ps aux | grep {CTID}`
 2. search for `/usr/bin/lxc-start -F -n {CTID} in the last column`
 3. take not of the process ID in the second column
 4. `kill -9 {process ID}`