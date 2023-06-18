# clone git repo
https://github.com/zabbix/zabbix-docker.git

# get docker-compose file
cd zabbix-docker
cp docker-compose_v3_alpine_mysql_latest.yaml docker-compose.yml

# change env variables
cd env_vars
ls -al
change password in files:
- nano .MYSQL_PASSWORD
- nano .MYSQL_ROOT_PASSWORD
change username in file (not root):
- nano .MYSQL_USER

# change ports in docker-compose
check ports that are in use by other services:
`lsof -i -P -n | grep LISTEN`
`cd ..`
`nano docker-compose.yml`
go through the file and change the left value of the ports for the services if those ports are already in use by other services.

# Start container
`docker-compose --profile all up -d && docker-compose logs -f`
wait a minute
once finished, head to {ip}:}{port} of 'zabbix-docker-zabbix-web-nginx-mysql-1'
if the login page doesn't appear after a minute, run previous command again and retry

### permission error
if you get a permission error after running the docker-compose, under zabbix-agent, comment out 'privileged: true' and try again

# Login to zabbix
to log in, enter Admin and zabbix as username and password respectively

# Configure zabbix
## change password
User settings > Profile > Change password
## add hosts
Configuration > Hosts > Create host
ssh into the host and add the zabbix-agent:
	1. `apt install zabbix-agent -y`
	2. `nano /etc/zabbix/zabbix_agentd.conf` 
	3. under 'Option: SourceIP', uncomment SourceIP and input the IP of the host that needs to be monitored
	4. under 'Option: Server', change the IP to the IP of the server that has the Zabbix server installed, uncomment 'ListenPort=10050' and 'ListenIP=0.0.0.0'
	5. under 'Option: Server', change the IP to the IP of the server that has the Zabbix server installed, uncomment Hostname and input the hostname of the host
	6. systemctl start zabbix-agent
	7. systemctl enable zabbix-agent
	8. systemctl status zabbix-agent