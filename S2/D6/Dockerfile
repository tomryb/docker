# docker build -t img_expose .
# docker images
# docker stop [previous_container]
# docker run -itd --rm --name cont_expose -p 8080:80 img_expose
# check localhost:8080
# docker ps -a
# docker container stop cont_expose

FROM ubuntu:16.04

RUN apt-get update && apt-get install nginx -y \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]
