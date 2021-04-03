Docker: PHP and extensions
==========================

Official [PHP docker image](https://hub.docker.com/_/php/) with additional extensions.

Supported tags
--------------

- [`7.4-fpm-alpine`, `latest`](7.4/Dockerfile)
- [`7.2-fpm-alpine`](7.2/fpm/Dockerfile)

Extensions enabled
------------------

| Extension   | PHP 7.2 | PHP 7.4 |
| ----------- | ------- | ------- |
| mcrypt      |    x    |    x    |
| iconv       |    x    |    x    |
| intl        |    x    |    x    |
| mbstring    |    x    |    x    |
| gd          |    x    |    x    |
| curl        |    x    |    x    |
| dom         |    x    |    x    |
| simplexml   |    x    |    x    |
| xmlreader   |    x    |    x    |
| xmlwriter   |    x    |    x    |
| sockets     |    x    |    x    |
| zip         |    x    |    x    |
| pdo_pgsql   |    x    |    x    |
| pdo_mysql   |    x    |    x    |
| pdo_sqlite  |    x    |    x    |
| redis       |    x    |    x    |

Extras
------

- composer
- fxp/composer-asset-plugin:^1.4
