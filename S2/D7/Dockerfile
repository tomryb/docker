# docker build -t img_apache .
# docker images
# docker run -itd --rm --name cont_apache -p 8080:80 img_apache
# check localhost:8080
# docker ps -a
# docker container stop cont_apache

FROM ubuntu:12.04

LABEL Creator: "Cerulean Canvas"

RUN apt-get update && apt-get install -y apache2 \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

ENV APACHE_RUN_USER www-data
ENV APACHE_RUN_GROUP www-data
ENV APACHE_LOG_DIR /var/log/apache2

EXPOSE 80

CMD ["/usr/sbin/apache2", "-D", "FOREGROUND"]



