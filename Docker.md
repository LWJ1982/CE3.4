docker ps
docker images
docker build . -t <image_name>

docker run -dp 8080:80 httpd
curl http://localhost:8080
sudo systemctl status docker /// check if docker is running
docker exec -it <container id> sh

docker image pull <image_name>:<image_tag>
docker run -dp 9090:80 httpd:2.4-alpine

docker stop <container_id>
docker rm <container_id>
docker rm -f $(docker ps -aq) // stop and remove all docker

docker rmi <image id> //remove docker image