# tworzenie woluminu

- docker volume create vol-busybox
- docker run -d --volume vol-ubuntu:/tmp ubuntu
- docker volume ls

# usuwanie

- docker volume create vol-ubuntu
- docker volume ls


# montowanie woluminu

- docker run -itd --name cont-ubuntu --volume vol-ubuntu:/var/log ubuntu:latest
- docker volume ls
- docker ps -a
- docker exec -it cont-ubuntu bash
- apt-get update
- cd /var/log --> ls
- docker stop cont-ubuntu
- sudo su -
- cd /var/lib/docker/volumes/ --> ls