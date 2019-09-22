---
description: The Dopenote Docker image is automatically updated every release.
---

# With Docker

Docker is the only recommended way of setting up your own Dopenote instance.  
If you still aren't familiar with Docker, now is the time.

### Basic example

{% code-tabs %}
{% code-tabs-item title="docker-compose.yml" %}
```yaml
version: '3'

services:
  web:
    image: dopenote:1.0
    restart: always
    ports:
      - 82:80
    environment:
      - MYSQL_DATABASE=${MYSQL_DATABASE}
      - MYSQL_USER=${MYSQL_USER}
      - MYSQL_PASSWORD=${MYSQL_PASSWORD}

  db:
    image: mariadb:10.4
    restart: always
    environment:
      - MYSQL_DATABASE=${MYSQL_DATABASE}
      - MYSQL_ROOT_PASSWORD=${MYSQL_ROOT_PASSWORD}
      - MYSQL_USER=${MYSQL_USER}
      - MYSQL_PASSWORD=${MYSQL_PASSWORD}
    volumes:
      - "./db:/var/lib/mysql"
```
{% endcode-tabs-item %}
{% endcode-tabs %}

Run `docker-compose up -d` and check `http://[YOUR_SERVER_IP]:82`

### Upgrading

Edit your `docker-compose.yml` file, and update `image: xy2z/dopenote:X.X` to the latest release.  
Run `docker-compose up -d` and you're done.

