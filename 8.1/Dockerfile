FROM php:8.1-fpm-alpine

RUN set -ex \
  && apk --no-cache add \
    composer \
    postgresql-dev \
    # git \
    # php-dev \
    # libmcrypt-dev \
    # icu-dev \
    # freetype-dev \
    # libjpeg-turbo-dev \
    # libpng-dev \
  && docker-php-ext-install pdo_mysql pdo_pgsql \
  && docker-php-ext-configure intl \
  && docker-php-ext-install intl \
  # && docker-php-ext-configure gd --with-freetype-dir=/usr/include/ --with-jpeg-dir=/usr/include/ --with-png-dir=/usr/include/ \
  # && docker-php-ext-install -j$(nproc) gd \
  && docker-php-source delete

# RUN curl -L -o /tmp/redis.tar.gz https://github.com/phpredis/phpredis/archive/$REDIS_VERSION.tar.gz \
#   && tar xfz /tmp/redis.tar.gz \
#   && rm -r /tmp/redis.tar.gz \
#   && mkdir -p /usr/src/php/ext \
#   && mv phpredis-* /usr/src/php/ext/redis
# RUN docker-php-ext-install redis
