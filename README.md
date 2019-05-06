# Apache-php docker image

## Supported tags

* latest, 2.4

## How to use this image

### Volumes

* /var/www/html is the DocumentRoot for the project.
* /etc/apache2/sites-enabled is the directory for the vhost.

### Use from cli
```console
docker run --volume </local/code/path>:/var/www/html --volume </local/vhost/directory/path>:/etc/apache2/sites-enabled hlacos/apache-php[:tag] [<options>] <container-name>
```

Example:
```console
docker run --volume /local/code/path:/var/www/html --volume /local/vhost/directory:/etc/apache2/sites-enabled hlacos/apache-php apache-php
```

### Use with compose
```
version: '3'
services:
  apache-php:
    image: hlacos/apache-php
    container_name: apache-php
    volumes:
      - /local/code/path:/var/www/html
      - /local/vhost/directory:/etc/apache2/sites-enabled
```
