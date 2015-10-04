FROM debian:latest

MAINTAINER diego.lendoiro@openhost.es

RUN apt-get update && \
      apt-get install -y --force-yes \
      git \
      nginx-full

COPY files/index.html /var/www/html/index.html
COPY files/deal_with_it.gif /var/www/html/deal_with_it.gif
RUN chmod 755 /var/www/html/deal_with_it.gif

CMD [ "nginx", "-g", "daemon off;"]
