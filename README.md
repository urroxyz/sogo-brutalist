# sogo-brutalist
Brutalist theme for SOGo webmail client used in Mailcow: Dockerized.

## Installation
### Step 1
Download the theme to `/opt/mailcow-dockerized/data/conf/sogo/`:
``` bash
cd /opt/mailcow-dockerized/data/conf/sogo/
wget https://github.com/urroxyz/sogo-brutalist/raw/refs/heads/main/custom-theme.css
```

### Step 2
Create and populate `/opt/mailcow-dockerized/docker-compose.override.yml`:
```bash
sudo nano /opt/mailcow-dockerized/docker-compose.override.yml
```
```yml
version: '2.1'

services:
  sogo-mailcow:
    volumes:
      - ./data/conf/sogo/custom-theme.css:/usr/lib/GNUstep/SOGo/WebServerResources/css/theme-default.css:z
```

### Step 3
Use `docker compose` or `docker-compose` to `down` and/or `up` the containers:
```bash
cd /opt/mailcow-dockerized/ && sudo docker compose up -d
```
— or —
```bash
cd /opt/mailcow-dockerized/ && sudo docker-compose up -d
```

Restart your browser and clear the cache.

## Configuration
Please create a pull request if you have any suggestions and I will commit it.
