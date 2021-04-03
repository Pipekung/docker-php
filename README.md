Docker: PHP and extensions
==========================

Official [PHP docker image](https://hub.docker.com/_/php/) with additional extensions.

Supported tags
--------------

- [`7.4-fpm-alpine`, `latest`](7.4/Dockerfile)
- [`7.2-fpm-alpine`](7.2/Dockerfile)

Extensions enabled
------------------

| Extension   | PHP 7.2 | PHP 7.4 |
| ----------- | ------- | ------- |
| mcrypt      | &check; | &check; |
| iconv       | &check; | &check; |
| intl        | &check; | &check; |
| mbstring    | &check; | &check; |
| gd          | &check; | &check; |
| curl        | &check; | &check; |
| dom         | &check; | &check; |
| simplexml   | &check; | &check; |
| xmlreader   | &check; | &check; |
| xmlwriter   | &check; | &check; |
| sockets     | &check; | &check; |
| zip         | &check; | &check; |
| pdo_pgsql   | &check; | &check; |
| pdo_mysql   | &check; | &check; |
| pdo_sqlite  | &check; | &check; |
| redis       | &check; | &check; |

Extras
------

- [x] composer
- [x] fxp/composer-asset-plugin:^1.4
