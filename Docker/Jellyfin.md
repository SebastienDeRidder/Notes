#  Set custom banner image

^9a8d4e

1. [[docker#edit files in docker container | enable bash in the container to allow commands]]
2.  in the container, navigate to path /jellyfin/jellyfin-web/assets/img/ 
3.  remove both images
4. disconnect from container
5. put [[attachments/banner-dark.png | banner-dark.png]] & [[attachments/banner-light.png | banner-light.png]] in a location accessible to the host that runs docker
8. cd to the location where you put the images
9. copy both images into the container using the following command:
   `docker cp banner-dark.png jellyfin:/jellyfin/jellyfin-web/assets/img/ && docker cp banner-light.png jellyfin:/jellyfin/jellyfin-web/assets/img/`
10. restart container