# [[docker]]
|                                   | Container               | Description                                                                   | URL                                                                      | Port  |
| --------------------------------- | ----------------------- | ----------------------------------------------------------------------------- | ------------------------------------------------------------------------ | ----- |
| <input type="checkbox" checked>   | [[Portainer]]           | Manage docker containers from a web interface                                 | [web interface](https://portainer.sebas-tien.com/#!/2/docker/containers) | 9000  |
| <input type="checkbox" checked>   | Radarr                  | Search torrent trackers for torrents and send them to qBitTorrent             | [web interface](https://radarr.sebas-tien.com/)                          | 7878  |
| <input type="checkbox" checked>   | Sonarr                  | Search torrent trackers for torrents and send them to qBitTorrent             | [web interface](https://sonarr.sebas-tien.com/)                          | 8989  |
| <input type="checkbox" checked>   | Bazarr                  | Download subtitles for movies and shows                                       | [web interface](https://bazarr.sebas-tien.com/)                          | 6767  |
| <input type="checkbox" checked>   | Prowlarr                | Manage torrent trackers to use with Radarr and Sonarr                         | [web interface](https://prowlarr.sebas-tien.com/)                        | 9696  |
| <input type="checkbox" checked>   | Tdarr                   | Strip down and transcode media files to decrease disk usage                   | [web interface](https://tdarr.sebas-tien.com/#/)                         | 8265  |
| <input type="checkbox" checked>   | qBitTorrent             | Torrent media files sent by Radarr and Sonarr                                 | [web interface](https://qbit.sebas-tien.com/)                            | 8080  |
| <input type="checkbox" checked>   | Plex                    | Media server to playback movies and shows with a nice interface               | [web interface](https://app.plex.tv/desktop/#!/)                         | 32400 |
| <input type="checkbox">            | Jellyfin                | Open source media server to playback movies and shows with a nice interface   | [web interface](http://sebflix.sebas-tien.com/)                          | 8096  |
| <input type="checkbox">            | Spigot_1.19.2           | Minecraft server with plugins 1.19.2                                          | [server ip](http://192.168.0.110:25565/)                                 | 25565 |
| <input type="checkbox">            | Jellyfin_accounts       | Web app to create invites and register accounts for Sebflix                   | [web interface](https://register.sebas-tien.com/)                        | 8056  |
|                                   | Dashy                   | Dashboard for all self-hosted services                                         | [web interface](https://dash.sebas-tien.com/)                            | 4000  |
|                                   | Code-server             | Visual Studio Code server                                                     | [web interface](https://vs.sebas-tien.com/?folder=/docker)               | 8443  |
|                                   | Requestrr               | Discord bot to send requests to overseer to be downloaded                     | [web interface](https://requestrr.sebas-tien.com/)                       | 4545  |
|                                   | Overseerr               | Web interface to request movies/shows to be downloaded with Radarr and Sonarr | [web interface](https://overseerr.sebas-tien.com/)                       | 5055  |
|                                   | changedetection         | Monitor changes to tracked webpages                                           | [web interface](https://webwatch.sebas-tien.com/)                        | 5000  |
|                                   | TubeArchivist           | Web-based tool for archiving YouTube videos                                   | [web interface](http://tube-archivist.sebas-tien.com/)                   | 8001  |
|                                   | Chatpad                 | OpenAI chatbot client                                                         | [web interface](https://ai.sebas-tien.com/)                              | 8200  |
| <input type="checkbox">            | Uptime-Kuma             | Monitor uptime and response time of websites                                  | [web interface](http://monitor.sebas-tien.com/)                      | 3001  |
|                                   | Readarr                 | Manage and organize your book collection                                      | [web interface](https://readarr.sebas-tien.com/)                         | 8787  |
|                                   | NZBGet                  | Usenet downloader                                                             | [web interface](https://nzbget.sebas-tien.com/)                          | 6789  |
|                                   | Projectsend             | Secure file sharing and document management system                            | [web interface](https://projectsend.sebas-tien.com/)                     | 8100  |
|                                   | Archivebox-Archivebox-1 | Self-hosted internet archiving tool                                           | [web interface](http://archivebox.sebas-tien.com:8300/)                  | 8300  |
|                                   | Semaphore-MySQL         | MySQL database for Semaphore                                                  | -                                                                        | -     |
|                                   | Ansible-Semaphore       | Ansible playbook deployment with Semaphore UI                                 | [web interface](http://ansible-seb.semaphore-tien.com/)                  | 3000  |
|                                   | Habe-Web                | Web application for managing home automation and IoT devices                  | [web interface](http://habe-web.sebas-tien.com/)                         | 81    |
|                                   | Habe-DB                 | MySQL database for Habe-Web                                                   | -                                                                        | -     |
|                                   | Redis                   | In-memory data structure store                                                | -                                                                        | -     |
|                                   | Cadvisor                | Analyzes resource usage and performance characteristics of running containers | -                                                                        | -     |
|                                   | Prometheus              | Monitoring and alerting toolkit                                               | [web interface](http://prometheus.sebas-tien.com/)                       | 9090  |
|                                   | InfluxDB                | Time series database                                                          | -                                                                        | -     |
|                                   | Telegraf                | Plugin-driven server agent for collecting and reporting metrics               | -                                                                        | -     |
|                                   | Node-Exporter           | Exposes hardware and OS metrics of a host system                              | -                                                                        | -     |
| <input type="checkbox" checked>   | Grafana                 | Observability platform for metrics, logs, and traces                          | [web interface](http://grafana.sebas-tien.com:3002/)                     | 3002  |
| <input type="checkbox" checked>   | immich                  | Photo and video library                                                       | [web interface](https://immich.sebas-tien.com/)                          | 2283  |
|                                   | Nginx                   | Personal website                                                              | [web interface](https://sebas-tien.com/)                                 | 2080  |
|                                   | Wishlist                | Website to create and share wishlists                                         | [web interface](https://wishlist.sebas-tien.com/)                        | 80    |





# [[proxmox]]
| ID  | Device              | URL                                                                                     |
| --- | ------------------- | --------------------------------------------------------------------------------------- |
| 100 | Proxmox main server | [web interface](https://proxmox.sebas-tien.com/) |
| 101 | Proxmox HP server   |   [web interface](https://192.168.0.101:8006/#v1:0:=node%2Fpve:4:5:::::=consolejs:)                                                                                      |

# [[homeassistant]]
| ID  | Device            | URL                                    |
| --- | ----------------- | -------------------------------------- |
| 112    |  haos9.2                 |  [web interface](http://192.168.0.112:8123/)                                      |
| 210 | TasmotaServer1    | [web interface](http://192.168.0.210/) |
| 211 | TasmotaServer2    | [web interface](http://192.168.0.211/) |
| 212 | TasmotaDesk       | [web interface](http://192.168.0.212/) |
| 213 | TasmotaWindow     | [web interface](http://192.168.0.213/) |
| 214 | TasmotaPowerstrip | [web interface](http://192.168.0.214/) |

# network devices
| ID  | Device              | URL                                                                                     |
| --- | ------------------- | --------------------------------------------------------------------------------------- |
| 254 | Cisco SG300 28p switch | [web interface](http://192.168.0.254/csd12a1516/home.htm)|
| 253 | TP-link Archer AX50 router   |[web interface](https://192.168.0.253/webpages/index.1627628878582.html)  |

#ref - [ ] 

