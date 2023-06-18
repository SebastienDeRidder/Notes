# updater.sh
```shell
#!/bin/bash
apt-get update -y && apt-get upgrade -y && apt dist-upgrade -y &&
apt autoremove -y && apt autoclean -y
echo "_________________________________________________________________________"
echo "update en upgrade completed"
```

# vm-restart.sh
```shell
#!/bin/bash
rm /var/lock/qemu-server/lock-$1.conf
qm stop $1 && qm shutdown $1
```

# ct-restart.sh
```shell
#!/bin/bash
rm /run/lock/lxc/pve-config-$1.lock
pct unlock $1 && lxc-stop $1
```

# docker-compose-latest.sh
```shell
#!/bin/bash
compose_version=$(curl https://api.github.com/repos/docker/compose/releases/latest | jq .name -r)
output='/usr/local/bin/docker-compose'
curl -L https://github.com/docker/compose/releases/download/$compose_version/docker-compose-$(uname -s)-$(uname -m) -o $output
chmod +x $output
echo $(docker-compose --version)
```