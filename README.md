**Description**

This is a simple docker setup packed with some goodies for **Raspberry Pi A**.
This configuration was successfully tested with the **Raspbian Stretch on Raspberry Pi A**.

**Docker installation**

`````
install-docker.sh
`````

**Run the app**

`````
cd docker
docker-compose up -d 
`````

**Access the app**

`````
IP:80 = phpMyAdmin (https://www.phpmyadmin.net/)
IP:81 = Hypriot Docker UI (https://blog.hypriot.com/post/new-docker-ui-portainer/)
IP:3306 = MySQL server (https://www.mysql.com/)
`````

**Clean up ALL containers/images**
`````
docker kill $(docker ps -q)
docker rm $(docker ps -a -q)
docker rmi -f $(docker images -q)
`````

**(Optional) Build phpmyadmin image for RPI**
`````
cd rpi-phpmyadmin-image
docker build . -t chieftainy2k/rpi-phpmyadmin
`````
