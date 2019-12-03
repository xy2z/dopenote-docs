---
description: The Dopenote Docker image is automatically updated on every release.
---

# Install using Docker

Docker is the only recommended way of setting up your own Dopenote instance.  
If you still aren't familiar with Docker, now is the time to start.

### 1. Environment file

First you have to create a `.env` file with the database settings:  
Remember to set a random password for `DB_PASSWORD` and `DB_ROOT_PASSWORD`.

```yaml
DB_HOST=db
DB_DATABASE=app
DB_USER=app
DB_ROOT_PASSWORD=
DB_PASSWORD=
```

### 2. Docker-compose.yml file

In the same directory as your `.env` file, add a new `docker-compose.yml` file:

{% tabs %}
{% tab title="docker-compose.yml" %}
```yaml
version: '3'

services:
  web:
    image: dopenote/dopenote:1.0.0-alpha.2
    restart: always
    ports:
      - 82:80
    environment:
      - DB_HOST=db
      - DB_DATABASE=${DB_DATABASE}
      - DB_USERNAME=${DB_USER}
      - DB_PASSWORD=${DB_PASSWORD}

  db:
    image: mariadb:10.4
    restart: always
    environment:
      - MYSQL_DATABASE=${DB_DATABASE}
      - MYSQL_ROOT_PASSWORD=${DB_ROOT_PASSWORD}
      - MYSQL_USER=${DB_USER}
      - MYSQL_PASSWORD=${DB_PASSWORD}
    volumes:
      - "./db:/var/lib/mysql"
```
{% endtab %}
{% endtabs %}

Run `docker-compose up -d` and go to `http://[YOUR_SERVER_IP]:82`

### Upgrading

1. Edit your `docker-compose.yml` file, and change `image: dopenote/dopenote:X.X` to the latest release.
2. Run `docker-compose up -d` and you're done.

