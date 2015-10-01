FROM debian:latest

MAINTAINER diego.lendoiro@openhost.es

RUN apt-get update && \
      apt-get install -y --force-yes \
      git \
      nginx-full

CMD [ "nginx", "-g", "daemon off;"]
