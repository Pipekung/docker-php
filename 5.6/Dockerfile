FROM php:7.2-fpm-alpine

LABEL maintainer="Channarong Janpanich <cj.pipekung@gmail.com>"

ENV COMPOSER_ASSET_PLUGIN_VERSION ^1.4
ENV REDIS_VERSION 5.3.4
ENV MCRYPT_VERSION 1.0.4

RUN set -ex \
  && apk --no-cache add composer postgresql-dev git php7-dev libmcrypt-dev icu-dev freetype-dev libjpeg-turbo-dev libpng-dev \
  && docker-php-ext-install pdo_mysql pdo_pgsql iconv \
  && docker-php-ext-configure intl \
  && docker-php-ext-install intl \
  && docker-php-ext-configure gd --with-freetype-dir=/usr/include/ --with-jpeg-dir=/usr/include/ --with-png-dir=/usr/include/ \
  && docker-php-ext-install -j$(nproc) gd \
  && docker-php-source delete

RUN curl -L -o /tmp/redis.tar.gz https://github.com/phpredis/phpredis/archive/$REDIS_VERSION.tar.gz \
    && tar xfz /tmp/redis.tar.gz \
    && rm -r /tmp/redis.tar.gz \
    && mkdir -p /usr/src/php/ext \
    && mv phpredis-* /usr/src/php/ext/redis
RUN docker-php-ext-install redis

COPY php.ini /usr/local/etc/php/php.ini

RUN composer global require "fxp/composer-asset-plugin:$COMPOSER_ASSET_PLUGIN_VERSION"