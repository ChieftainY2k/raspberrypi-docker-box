**Init**

`````
cd docker
docker-compose up -d phpmyadmin
`````


**Docker: clean up**
`````
docker kill $(docker ps -q)
docker rm $(docker ps -a -q)
docker rmi $(docker images -q)
`````

