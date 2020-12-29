# tworzenie sieci

- docker network create --driver bridge my-bridge
- docker network create --driver bridge --subnet=192.168.0.0/16 --ip-range=192.168.5.0/24 my-bridge1
- docker network ls
- docker container start [nazwa_kontenera]
- docker network connect my-bridge1 tr-busybox-A
- docker container inspect tr-busybox-A --> Networks

# odpalenie kontenera i podłączenie do sieci

- docker container run -itd --network host --name cont_nginx nginx:latest

# odłączenie z sieci

- docker network disconnect my-bridge1 tr-busybox-A