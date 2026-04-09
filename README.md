# Docker NGINX Demo


## Steps

## if nginx & docker not installed
sudo apt-get update
sudo apt-get install nginx -y
sudo apt-get install docker.io -y

## create dockerifle
vim Dockerfile

## dockerfile >> docker image
docker build -t docker-nginx-demo .
 (Here is "docker-nginx-demo" is dockerimage name ) 

## any error occurred 
(you have to add user to docker group)
sudo usermod-aG docker $USER
newgrp docker 
(refresh docker group)

## docker image >> container
docker run -d -p 80:80 docker-nginx-demo

## website can be accessible at
localhost://80 (if you use docker desktop)
OR
ip address paste in browser



