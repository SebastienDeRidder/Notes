# Enable root login for ssh
```bash
sudo sed -i "/Authentication:/a\
PermitRootLogin yes" /etc/ssh/sshd_config\
&& sudo systemctl restart ssh```

# Create NFS share
```bash
# 1. install NFS
sudo apt-get install -y nfs-kernel-server
# 2. Create shared directory
sudo mkdir /mnt/shared
sudo chmod -R 777 /mnt/shared
# 3. Configure NFS to share that directory
sudo nano /etc/exports
 Add the following line:
 /mnt/shared *(rw,all_squash,insecure,async,no_subtree_check,anonuid=1000,anongid=1000)
# 4. Update the NFS active exports
sudo exportfs -ra
```

# Make an alias/custom command
```bash
# 1. edit bashrc
nano ~/.bashrc
# 2. format
 alias aliasname='commands'
# 3. example
 alias dcup='docker-compose up -d'
# 4. save and exit
# 5. load the command
 source ~/.bashrc
```