**Init**

`````
install-docker.sh
`````

**Run the app**

`````
cd docker
docker-compose up -d 
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
