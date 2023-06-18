# install portainer
1. `docker volume create portainer`
2. download and run portainer image:
```yaml
  portainer:
    image: portainer/portainer-ce:latest
    container_name: portainer
    restart: unless-stopped
    volumes:
      - /etc/localtime:/etc/localtime:ro
      - /var/run/docker.sock:/var/run/docker.sock:ro
      - ./portainer-data:/data
    ports:
      - 8000:8000
      - 9000:9000
      - 9443:9443
```
3. in browser, go to: https://localhost:9443
4. create user
5. go to environments > local and set Public IP
6. go to settings and change App Templates url to:
   [https://raw.githubusercontent.com/SelfhostedPro/selfhosted_templates/master/Template/portainer-v2.json](https://raw.githubusercontent.com/SelfhostedPro/selfhosted_templates/master/Template/portainer-v2.json "https://raw.githubusercontent.com/SelfhostedPro/selfhosted_templates/master/Template/portainer-v2.json")