# install docker
1. install prerequisites:
```shell
sudo apt-get install \
   ca-certificates \
   curl \
   gnupg \
   lsb-release
```
2. add docker's official GPG key:
```shell
sudo mkdir -p /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/debian/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
```
3. set up the repo:
```shell
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/debian \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```
4. `sudo apt-get update`
5. install docker:
```shell
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-plugin docker-compose
```

## Install latest version of docker-compose
run [[scripts#docker-compose-latest.sh | script]]

# edit files in docker container
1. log in to the container:
   `docker exec -it <container name> bash`
2. connect to the container through portainer and run:
   `apt-get update`
   `apt-get install nano`

# See what service is using port x
```bash
lsof -n -i :{port} | grep LISTEN
```

