# Instalacja nginx

- wget http://nginx.org/keys/nginx_signing.key
- cd /etc/apt/
- apt-get remove nginx-common
- apt-get update
- cd ../..
- apt-get install nginx

# Instalacja Dockera

- sudo apt-get update
- sudo apt-get install apt-transport-https ca-certificates curl software-properties-common
- sprawdzenie czy ok sudo apt-key fingerprint i sudo docker run hello-world
- sudo docker image pull nginx:latest
- sudo docker images
- sudo docker container run -itd --name web-server-nginx -p 8080:80 nginx:latest
- sudo docker ps -a
- sudo groupadd docker
- sudo usermod -aG docker ${nazwa_użytkownika}