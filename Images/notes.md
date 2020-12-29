# wyszukiwanie obrazu

- docker search python:3.6
- docker search registry
- docker search --filter "is-official=true" registry
- docker search --format "table {{.Name}}\t{{.Description}}\\t{{.IsOfficial}}" registry

# wyświetlanie obrazów

- docker images
- docker images ubuntu
- docker images ubuntu:16.04

# pobieranie obrazu z docker-hub do hosta

- docker image pull nginx:latest

# wypychanie na docker-hub

- docker login
- docker tag [nazwa_obrazu] [użytkownik]/[nazwa_repo]:[tag]
- docker image push [użytkownik]/[nazwa_repo]:[tag]

# inspect

- docker images ubuntu
- docker image inspect ubuntu:[tag]
- docker image inspect --format "{{.RepoTags}} : {{.RepoDigests}}" ubuntu:[tag]

# zapis do pliku

- docker image inspect --format "{{json .Config}}" ubuntu:[tag] > inspect_report_ubuntu.txt

# wyświetlanie historii

- docker image history ubuntu:[tag]
- docker image history img_apache

# usuwanie obrazów

- docker image rm [nazwa_kontenera]
- docker rmi [id]
Jeśli pojawi się error, że jest kilka takich dodajemy flagę --force