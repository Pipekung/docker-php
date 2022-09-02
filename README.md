Docker: PHP and extensions
==========================

Official [PHP docker image](https://hub.docker.com/_/php/) with additional extensions.

Supported tags
--------------

- [`7.4-fpm-alpine`, `latest`](7.4/Dockerfile)
- [`7.2-fpm-alpine`](7.2/Dockerfile)

Extensions enabled
------------------

| Extension   | PHP 5.6 | PHP 7.2 | PHP 7.4 |
| ----------- | ------- | ------- | ------- |
| mcrypt      | &check; | &check; | &check; |
| iconv       | &check; | &check; | &check; |
| intl        | &check; | &check; | &check; |
| mbstring    | &check; | &check; | &check; |
| gd          | &check; | &check; | &check; |
| curl        | &check; | &check; | &check; |
| dom         | &check; | &check; | &check; |
| simplexml   | &check; | &check; | &check; |
| xmlreader   | &check; | &check; | &check; |
| xmlwriter   | &check; | &check; | &check; |
| sockets     | &check; | &check; | &check; |
| zip         | &check; | &check; | &check; |
| pdo_pgsql   | &check; | &check; | &check; |
| pdo_mysql   | &check; | &check; | &check; |
| pdo_sqlite  | &check; | &check; | &check; |
| redis       | &check; | &check; | &check; |

Extras
------

- [x] composer
- [x] fxp/composer-asset-plugin:^1.4
