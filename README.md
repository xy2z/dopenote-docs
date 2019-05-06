---
description: Self-hosted webapp for notes
---

# Dopenote

## Project is still a work in progress.

Expected release is summer 2019.

```yaml
version: 3

services:
  web:
    image: dopenote:1.0.0-alpha1
    restart: always
    ports:
      - 8015:80
    volumes:
      - ./config:/app/custom/config

  db:
    image: mariadb:10.4
```

\# Using Traefik



