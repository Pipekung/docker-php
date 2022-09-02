FROM php:7.4-fpm-alpine

LABEL maintainer="Channarong Janpanich <cj.pipekung@gmail.com>"

ENV COMPOSER_ASSET_PLUGIN_VERSION ^1.4
ENV REDIS_VERSION 5.3.4
ENV MCRYPT_VERSION 1.0.4

RUN set -ex \
  && apk --no-cache add composer postgresql-dev git php7-dev libmcrypt-dev icu-dev freetype-dev libjpeg-turbo-dev libpng-dev libxml2-dev \
  && docker-php-ext-install pdo_mysql pdo_pgsql iconv \
  && docker-php-ext-configure intl \
  && docker-php-ext-install intl \
  && docker-php-ext-configure gd --with-freetype --with-jpeg \
  && docker-php-ext-install -j$(nproc) gd \
  && pecl install mongodb \
  && docker-php-ext-configure mongodb \
  && docker-php-ext-enable mongodb \
  && docker-php-source delete

RUN curl -L -o /tmp/redis.tar.gz https://github.com/phpredis/phpredis/archive/$REDIS_VERSION.tar.gz \
  && tar xfz /tmp/redis.tar.gz \
  && rm -r /tmp/redis.tar.gz \
  && mkdir -p /usr/src/php/ext \
  && mv phpredis-* /usr/src/php/ext/redis
RUN docker-php-ext-install redis \
  && docker-php-ext-enable redis
