[homeassistant web interface](http://192.168.0.112:8123/)

# install script
```shell
bash -c "$(wget -qLO - https://github.com/tteck/Proxmox/raw/main/vm/haos-vm-v4.sh)" 
```

# change VM ip
settings > system > network > IPv4 > static > {ip}

# setup MQTT + [[Tasmota]] integration
1. add/start 'mosquito broker' from add-on store
2. add new 'Tasmota' user
3. configure mqtt integration > finish
4. add 'Tasmota' integration
5. [[Tasmota#configure mqtt | configure Tasmota devices]]

# setup cloudflared for reverse proxy
https://github.com/brenner-tobias/addon-cloudflared/blob/main/cloudflared/DOCS.md#configurationyaml
```yml
additional_hosts:
  - hostname: tasmota.sebas-tien.com
    service: http://192.168.0.112:9541
    disableChunkedEncoding: true
external_hostname: ha.sebas-tien.com
```