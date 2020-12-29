# docker build -t img_run-env .
# docker images
# docker run -itd --name cont_run-env img_run-env
# check localhost:8080
# docker ps -a
# docker exec -it cont_run-env bash

FROM ubuntu:16.04

LABEL Creator: "Cerulean Canvas"

RUN apt-get update && apt-get install -y curl \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

RUN mkdir /home/Codes

ENV USER Cerulean-Canvas
ENV SHELL /bin/bash
ENV LOGNAME Cerulean-Canvas

CMD ["bash"]
