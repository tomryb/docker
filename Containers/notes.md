# tworzenie kontenera

- docker container create -it --name tr-busybox-A busybox:latest
- docker ps -a

# uruchamianie i zatrzymywanie kontenera

- docker container run -itd --rm --name tr_busybox_B busybox:latest
- docker ps -a
- docker container start tr-busybox-A
- docker ps -a
- docker container stop tr_busybox_B
- docker ps -a

# restart kontenera

- docker container restart --time 5 tr-busybox-A
- docker ps -a

# zmiana nazwy

- docker container rename tr-busybox-A my-busybox
- docker ps -a

# podłączenie do sesji w kontenerze

- docker container attach my-busybox

# wykonanie polecenia

- docker container start my-busybox
- docker exec -it my-busybox pwd

Różnica między attach a exec jest taka, że po wyjściu z attach kontener jest zatrzymany, po exec nie

# mapowanie po kontenerach

- docker container run -itd --name cont_nginx2 -p 8080:80/tcp img_expose
- docker ps -a
- docker container run -itd --name cont_nginx3 -P img_expose
- docker ps -a


# usuwanie kontenerów

- docker container rm [nazwa]

Kontenery odpalone usuwamy z flagą --force