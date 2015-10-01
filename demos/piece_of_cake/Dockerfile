FROM debian:latest

MAINTAINER diego.lendoiro@openhost.es

ENV DESTINATION /var/www/my_awesome_app
ENV COMPOSER_URL https://getcomposer.org/installer
ENV LISTEN 0.0.0.0
ENV CAKE_PORT 5673

RUN apt-get update && \
    apt-get install -y --force-yes \
    php5-fpm \
    php5-intl \
    php5-mysql \
    curl \
    git

RUN curl -s $COMPOSER_URL | php &&\
    php composer.phar create-project --no-interaction \
      --prefer-dist cakephp/app $DESTINATION && \
    chmod 755 $DESTINATION/bin/cake

CMD [ "$DESTINATION/bin/cake", "server", "-H", "$LISTEN", "$CAKE_PORT" ]
